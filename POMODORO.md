# Pomodoro Timer[^1]
| A web-based timer designed to curb procrastination. |
| -------- |

![Desktop with many windows open and timer in corner](public/pomodoro/pomodoro-preview.png)


## Table of Contents
1. [Problem](#problem)
2. [Background](#background)
3. [Research](#research)
4. [Approach](#approach)
5. [Design](#design)
6. [Final Result (Demo)](#final-result)
7. [Insights](#insights)

## Problem
Engineering students need to complete giant programming assignments without getting overwhelmed or burnt out. Without a way to break up work into smaller tasks and work for shorter periods of time, engineering students will suffer from a lack of productivity and, potentially, fail to complete assignments.

## Background
In **CSE 110: Software Engineering**, my team had one job: build a web-based Pomodoro timer that _honors_ (not hacks) the official technique[^2]. Everything else—feature set, visual style, code base—was on us.

## Research
### Market & Method Crash-Course
Before we started thinking of what our timer would look like, we needed to analyze the competition for pitfalls and understand the needs of our users _directly_.

| What we looked at | Why it mattered | What we learned |
| ----------------- | --------------- | --------------- |
| 6 popular Pomodoro apps | Benchmark UX patterns, failures | - Pause buttons break the “no interruptions” rule. <br/> - Salient colors & gamification fights focus. <br/> - Several apps buried basic feedback (how long is left?) |
| Our own homework sprints | Empathy & obvious pain points | - Need to toggle between code, docs, and Slack often. <br/> - Dark rooms + late-night coding → dark-mode <br/> - Keyboard + mouse both needed |
| Technique literature review	| Decide on rules | - 25 min work / 5 min break default <br/> - No pausing; restarting forfeits the round |

<p id="bad-pomos-section" style="display:flex;">
  <img src="/public/pomodoro/pomofocus.png" alt="Red pomodoro timer with pause button" style="width:49%;">
  <img src="/public/pomodoro/tomatotimer.png" alt="Red pomodoro timer with cartoons and ads" style="width:49%;">
</p>

**Figure 1:** _Typical competitor interfaces: bright colors, pause icon, and distractions._

## Approach
What we decided to do before designing:
1. **Market Scan & Rapid Persona:** A six-app competitive audit plus first-hand sprints told us where existing timers stumble (pausing, visual noise).
1. **Success Criteria:** If engineering students can't forget the timer exists until it reminds them, we failed.
2. **Design Principles:** Simplicity • Distraction-free • Multi-modal feedback • Abuse-proof • Inclusive layout
3. **Storyboard & Usage Scenarios:** Where, when, and how the timer surfaces during a real coding day (see next section).

### Storyboard & Usage Scenarios
Before locking UI, we sketched four “day-in-the-life” frames to test how, where, and how visible the timer actually is. Each frame triggered concrete design rules.

![4 examples: first has timer as a small window, second has timer as a tab, third has timer on a mobile device, fourth has it hidden by full-screen code editor](/public/pomodoro/scenes-light.png#gh-light-mode-only)
![4 examples: first has timer as a small window, second has timer as a tab, third has timer on a mobile device, fourth has it hidden by full-screen code editor](/public/pomodoro/scenes-dark.png#gh-dark-mode-only)

**Figure 2:** _(Left to right) Timer as tile, as a tab, on a mobile device, and hidden by a full-screen editor._

| Frames | Reality Check | Design Moves |
| ----- | ------------- | ------------ |
| **A. Screen tile** | Only a 500 px-wide sliver shows | - Oversized digits readable even at the minimum width. <br/> - Calm mode so countdown less stressful |
| **B. One tab in a sea** | Tiny bit of text shows + user may forget which tab | - Dynamic tab title shows time left <br/> - Favicon badge represents mode |
| **C. Mobile quick-check** | Portrait mode on a small screen | - Single column with info <br/> - Haptic vibration on break |
| **D. VS Code full-screen** | Timer is completely hidden | - Audio notification <br/> - Quick keyboard toggle |


> **Insight.** Visibility is situational ⇒ build redundant channels (visual, auditory, haptic).


![Example of user using timer as a tab](/public/pomodoro/storyboard.jpeg)

**Figure 3:** _Example of part of the storyboard for (B) the timer as just a tab._

## Design
### Design Goals
| Goal | How We Addressed It |
| ---- | ------------------- |
| Honor technique | No _pause_. Durations clamped to 5–59 min. |
| Absolute focus | Distractions (stats, settings) lock during a countdown. No bright colors. | 
| Effortless glanceability | Timer numbers = billboard; everything else secondary. |
| Zero-friction setup | Sensible defaults (25/5/15, dark mode, sound on). One-click start | 
| Misuse proofing | Input bounds, inline validation, Jest/Cypress tests. |
| Accessible | Keyboard shortcuts, ARIA labels, fluid layout ≥ 500px. |

### Process Highlights
#### Sketch → Wireflow
Low-fi sketches let us debate _control density_ (one dual-state button vs two) and _information scent_ (sidebar vs modal settings). A clickable Figma wireflow exposed friction early—it was confusing having both a Start and Restart button when only one action is possible at a time.

![Wireframe of user interactions with site](/public/pomodoro/wireframe_1.png)
**Figure 4:** _Timer interrupt vs successful work session._

#### Simplicity is Key
Any feature had to answer five W’s (who, what, when, where, why). If it didn’t enforce focus or reduce friction, we cut it.

![Initial design for timer with restart and finish buttons](/public/pomodoro/roadmap_features.png)
**Figure 5:** _P0 features that passed the test._


#### Color & Salience Tests
A/B tests showed that the bright-teal looked "fun" but was distracting and didn't mesh well with the late-night coding sessions. _Plus, everyone liked a dark-mode IDE._

<p id="colors-section" style="display:flex;">
  <img src="/public/pomodoro/ui_v1_pomo_reset.png" alt="Original teal work mode mockup" style="width:39%;">
  <img src="/public/pomodoro/darkmode.png" alt="Dark and light modes of final app" style="width:59%;">
</p>

**Figures 6 & 7:** _Initial teal work mode → final dark & light work modes._


#### Interaction Guardrails
We thought about all the ways people might misuse the site, from inputing nonsense to button mashing, and made sure we had [test cases covered](https://github.com/ntrappe/cse110-w21-group33/blob/main/testing/cypress/test-pomo-settings.js).

![List of bad behaviors a user might perform](/public/pomodoro/badbehavior.png)
**Figure 8:** _List of bad behaviors we had to cover._


#### Responsive + Component Architecture
Because students might resize the timer to fit their work environment, each feature—timer, settings, etc.—had to be a flexible and modular. 
- [Each feature is a component](https://github.com/ntrappe/cse110-w21-group33/wiki/component): `<Timer>`, `<Settings>`, `<Info>`, etc.
- `<Control>` orchestrates state, syncs to `localStorage`, and exposes a tiny API (`start()`, etc.).
- **Result:** teammates worked in parallel, tests ran in isolation, and changes could be made with minor collisions.

![Examples of application with different widths and heights](/public/pomodoro/resized.png)
**Figure 9:** _Various widths and heights._

### Key UI Decisions

| UI Choice | Rationale |
| --------- | --------- |
| Dark mode default	| Developers already live in dark IDEs; reduces luminance contrast jumps. |
| Timer > everything | Primary task is see remaining minutes. Oversized, bold digits win. |
| Context-aware disabling	| During a work sprint, settings close (other than sound), stats gray out, and break-length inputs lock—pre-commitment.
| Inline error recovery | Bad numbers flip inputs red and auto-correct (<= 0 → 1, > 60 → 60) | Keyboard shortcuts | `S` start/`R` restart. Keeps hands on keys. | 

<br/>

![Invalid number of work minutes highlighted in red](/public/pomodoro/invalidinput.png)
**Figure 10:** _Invalid number of work minutes gets highlighted in red and reset._


## Final Result
https://vimeo.com/909267598

**Demo of the App.** See the pomodoro timer in action as we work, take breaks, modify settings, and explore features. For the purposes of the demonstration, we've sped up the timer. If you'd prefer to try it out yourself, find it [here](https://cse110team33.netlify.app/).

<details style="border: 1px solid #bbb; border-radius:8px; padding:7px 15px;"> 
<summary> Transcript</summary>
When we first open the app, we see a dark screen with 6 features. From left to right, we have a button for settings, a label indicating a work session, a timer with 25 minutes, a button to start the timer, a button for information, and a button for statistics.

When we click **Start**, the timer immediately starts to tick down from 25 minutes. The button that previously said **Start** has now changed to **Restart**. Note that we did speed up this timer for the demo.

At 23 minutes or so, we click **Restart** to stop the timer and set it back to 25 minutes. This is considered an interruption and we have forfeited this pomodoro.

We then open up settings, navigate to the time section and adjust the length of a work session from 25 to 2. The timer now shows 2 minutes.

We click **Start** and the timer begins to tick down from 2 minutes. While the timer is running, we click the settings button to open the sidebar and see that all options, except volume, are greyed out and cannot be clicked. No distractions are allowed.

When the timer runs out, the label for work turns to short break and we have five minutes on the timer. There are 4 squares below this label that previously were greyed out. One of these squares is now a bright green indicating one successful pomo--or work session.

We open settings again, this time to adjust the length of a short break to 1 minute. Note that settings does not allow you to input less than 1 minute or more than 60 minutes because it would go against the pomodoro technique.

We click Start and let the short break timer run down. Once complete, we click statistics to open up a display of four blocks. From left to right, the first block represents work sessions, then short breaks, then long breaks, and, finally, interruptions. Here, we see 1 square block indicating a work session, 1 square block for a short break, and 1 red square for an interruption.

We open up setting again and navigate to the display section. Here, we click the toggle button to turn off dark mode. Now, the screen is white and the timer numbers are black. We start the timer to complete our second pomo--or work session.

When the timer runs out, we have successfully finished that pomo and we should go into our second short break. We now have 2 green squares on the screen representing our work sessions.

We open settings again and navigate to the display section. This time we click the toggle for calm mode, turning it on. Instead of showing minutes and seconds on the timer, the calm mode shows only minutes. This is supposed to reduce further distractions by displaying fewer changes.

With '2m' representing 2 minutes on the timer, we click **Start** and and complete our second break. The video ends after this.↔︎
</details>

## Insights
- **Simplicity is Hard!** You can't hide behind your features so you have to completely understand your user, prioritize the features they need, and perfect it.
- **Usage Before Construction.** Understand when, how, and when your users will be using your tech before you start designing your architecture. Even knowing that the app would be minimizing the forced into different dimensions informed us early on that we needed a component architecture and lots of flex box.
- **It's Never Finished.** Looking back on this app years later, I see so many more improvements we could make now that I've had much more experience in web development and fresh eyes. It's a good reminder that your projects are never completely done, there's always opportunities for improvement.

[^1]: **Project Details:** Took 2 months to develop. Worked in a team of 11 as the lead and architect. Used JavaScript, Jest, Cypress, and Netlify. Try it [here](https://cse110team33.netlify.app/).
[^2]: **The Pomodoro Technique:** (A) Work for a “pomodoro” (typically 25 minutes). (B) Take a 5 minute break after the "pomodoro". (C) After 3 “pomodoros", take a longer 15 minute break. (D) If a “pomodoro” is interrupted, it is forfeited and must be restarted.
# Rock[^1]
| An app to explore national parks and find the ideal hike. |
| --- |

![3 phone screen displaying the entrypoint, home page, and a park page of the app](/public/rock/rock-preview.png)

## Table of Contents
1. [Problem](#problem)
2. [Background](#background)
3. [Research](#research)
4. [Approach](#approach)
5. [Design](#design)
6. [Final Result (Demo)](#final-result)
7. [Insights](#insights)

## Problem
Millennials visit U.S. National Parks **less** than any previous generation, jeopardising long-term NPS funding. Interviews revealed they feel _overwhelmed_ by choosing a park, finding a trail, and knowing what to bring.

## Background
For **COGS 100: Prototyping**, our objective was to build an interactive and innovative mobile information system to address a user problem. We were allowed to chose any problem of interest so long as we employed moodboards, wireframes, prototypes, and syle guides.

Two months before this project began, I was waiting in line for the shuttle at Pinnacles National Park. It’s a park full of towering cinnamon-colored talus rocks, hidden caves, deep gulches, and enormous condors. I ended up speaking to a park ranger and learned that there was an _enormous problem_ with park visitation. _How could I not try to tackle that?_ 

> “If we were a business and [millennials were] our clientele, then over the long term, we would probably be out of business.” — Jonathan Jarvis (NPS director).

## Research
To determine whether there was a clear problem to be solved, my team and I dove into research. 

| Method | Sample | Take-away |
| ------ | ------ | --------- |
| Lit scan | NPS reports & news articles | Visitation skew = iconic parks (Yosemite) crowded, other parks (Pinnacles) ignored. |
| [Survey](https://forms.gle/h2bxRMqGSMJAn3pt6) | 50 millennials | 77% want to visit a park; 80% not confident choosing one. _Quotes below._ |
| [Survey](https://forms.gle/h2bxRMqGSMJAn3pt6) | 12 park rangers | People that grew up hiking (were shown how) will visit the parks. |
| Follow-up interviews | 5 survey volunteers | Want to visit parks but are frustrated by process: _where to go?, what hike?, what to bring?_ → overwhelmed. |
| [Competitive audit](https://docs.google.com/document/d/1eKqaEfm-ZcYMHUdmKS3_RhwLTFxx08vJjQCDKVrxwAA/edit?usp=sharing) | 10 apps (AllTrails, NPS.gov..) | Great for experts; not beginner-friendly; lacking necessary features. |

> “I’m not confident in my ability to go to a national park by myself (driving, planning, directions, packing, etc.)” — Daniel Wang[^2]
>
> “I’m confused on the process of going. I believe you may have to book in advance to go to Yosemite? I know there’s more steps to the process but I’m not sure how to start.” — Melissa Roberts[^3]


![Table of all apps on the market compared across features like operating hours and maps](/public/rock/MarketResearch.png)
**Figure 1:** _Competitors compared across features._



## Approach
We framed every design trade-off with five questions:

| Lens | Why? | Design Implication |
| ---- | ---- | ------------------ |
| ⭐️ Fun | Users are overwhelmed & stressed | Color pops & photography to spark wanderlust | 
| ✌️ Broad appeal | Large demographic across genders, SEO, etc. | Neutral core palette, minimalist |
| 💡 Show, don't tell | Sell a park by showing it | Hero park photo, not walls of text |
| ℹ️ Right info, right depth | Balance education w/o overwhelming them; get novices informed | Progressive disclosure | 
| 📅 Offline contexts | Used on road, in park w/o service | Cache maps, trail details, recent alerts | 

## Design
### Design-System Snapshot
| Token | Value | Details |
| ----- | ----- | ------- |
| Components | HikePreview, ParkPreview, InfoBanner, etc. | Built in Figma; each with styling |
| Font | `SF Pro` main, `SF Mono` accent | General text is clean & bold; links & stats stand out |
| Colors | `#F2F2F7` background, `#619784` accent, `#000` primary text, `#7B7B7B` secondary text | Neutral base; color reserved for labels & status |

<p id="design-system-section" style="display:flex;">
  <img src="/public/rock/design_sys1.png" alt="Components including hike previews, park previews, etc." style="width:49%;">
  <img src="/public/rock/design_sys2.png" alt="Rules for buttons and banners" style="width:48%;">
</p>

**Figure 2:** _Design system with components._

### Iteration & Test Cycles
Our initial challenge in design was to find a balance between minimalism and fun. We relied on high-fi mockups to nail the look and feel.

| Round | Goal | What we changed | Evidence |
| ----- | ---- | --------------- | -------- |
| A/B #1 – “Fun vs Minimal” | Balance color & photography | Compared pastel card fills, borders vs shadows. Feedback: pastel blocks compete with photos. | Photo width 100%. **Fig 3.** |
| A/B #2 - "Light vs Dark" | Readability | Light-mode for readability + images | Light. **Fig 4.** |
| A/B #3 - "Icons" | Scan speed | Icons next to info like elevation gain clarify meaning | Icons on stats. |
| A/B #4 - "Photo vs Text" | Progressive disclosure | Tested amount of text on preview. Feedback: keep it to the minimum needed. | Different levels of previews. **Fig 5.** |
| High-Fidelity Pass | Validate app | Feedback: loved look, move settings, improve filters | **Fig 6.** |

_(Full critique notes ommited for brevity.)_

![First round of A/B testing had hike previews with pastel colors and some with borders, others with shadows, etc.](/public/rock/PreviewTestA.png)
**Figure 3:** _Hike previews with pastels, borders vs shadows._

![Second round of A/B testing had hike previews in dark and light modes](/public/rock/PreviewTestB.png)
**Figure 4:** _Variety of previews in light vs dark mode._

![After a round of feedback, hike previews would showcase as much of the image as posssible](/public/rock/PreviewTestC.png)
**Figure 5:** _One of the levels of previews. These should be the fastest to scan (like on a feed) so most minimal info._

<p id="feedback-section" style="display:flex;">
  <img src="/public/rock/feedback1.png" alt="Feedback to improve filters" style="width:49%;">
  <img src="/public/rock/feedback2.png" alt="Feedback to move settings" style="width:49%;">
</p>

**Figure 6 & 7:** _Feedback from peers on settings & filters._

## Final Result
**Download & watch the demo:** https://github.com/ntrappe/CMU_portfolio/blob/main/public/rock/rock_demo.mov

**Demo of the App.** See the app in action as we browse parks and hikes and set filters to narrow our options. If you'd prefer to try it out yourself, find it [here](https://www.figma.com/proto/ywP4mSyfwGENQ4pwyzv1vW/A4-National-Park-App?type=design&node-id=580-4846&t=g8QpYQoQiVCjQTzi-1&scaling=scale-down&page-id=580%3A4841&starting-point-node-id=580%3A4846&show-proto-sidebar=1).

## Insights
- **Design for Context, Not Just Content.** Anticipating where and how people use the app—at home, on the road, or in the park—drove our decision to include full offline maps and downloadable trail data. Designing around real‑world constraints (spotty cell service, on‑trail reference) made the experience reliable and trustworthy.
- **Let the Experience Shine.** Removing extraneous color blocks and leaning into immersive park photography kept the UI minimal yet evocative. When your content is stunning visuals of Yosemite or Pinnacles, clean layouts amplify the user's sense of wonder.
- **A/B Testing is King.** Every round of A/B testing or critique pointed out new things we hadn't considered and made our app better each time. It's never something to discount!

[^1]: **Project Details:** Took 2 months to develop. Worked in a team of 3 as the lead. Used Keynote and Figma.
[^2]: **Privacy:** This is not the participant's actual name to preserve privacy.
[^3]: **Privacy:** This is not the participant's actual name to preserve privacy.
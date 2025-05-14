# Museum Poster[^1]
| A poster to encourage the public to learn about unique architecture. |
| --- |

![Final poster framed on a wall](public/museum/museum-wall.png)

## Table of Contents
1. [Problem](#problem)
2. [Background](#background)
3. [Research](#research)
4. [Approach](#approach)
5. [Design (+ grid)](#design)
6. [Final Result](#final-result)
7. [Insights](#insights)

## Problem
The Canadian Centre for Architecture would like to encourage people to visit their newest exhibit: The Origins of the Avant-Garde in America. The event is free on a first-come, first-serve basis. Ideally, it will inspire novel forms of architecture in the community, provide more support for the Centre, and be accessible to a broad audience.

## Background
Our first assignment in **DSGN 100: Prototyping** was a crash-course in grid systems. The brief was simple on paper but harder in practice:

- Static digital poster (1024 × 1600 px)
- Must sit on an underlying grid
- At least one image from a supplied folder (edits allowed)
- **Every. Single. Word.** of the provided copy goes on the canvas

Four pages of text? Challenge accepted.

![3 sheets of paper with text to showcase how much content needs to be included](/public/museum/content-req-light.png#gh-light-mode-only)
![3 sheets of paper with text to showcase how much content needs to be included](/public/museum/content-req-dark.png#gh-dark-mode-only)

## Research
### Reverse-Engineering the Audience
The spec never said _who_ the poster was for, so I had to make some assumptions from the schedule:

| Day | Blocks |
| --- | ------ |
| Thu | 5:30-7:30 PM |
| Fri | 9 AM-12:15 PM, 2–4:45 PM, 5:30–6:30 PM |
| Sat | 9 AM-12:30PM |

We got **zero** input on audience or goals. All we received was that wall of text and a folder of photos. So I reverse-engineered a likely viewer:

- **Schedule clues:**
  - Thu 5:30 – 7:30 PM
  - Fri 9 AM – 12:15 PM, 2 – 4:45 PM, 5:30 – 6:30 PM
  - Sat 9 AM – 12:30 PM

Weekday, work-hour slots ≠ 9-to-5 crowd → likely retirees with daytime freedom. That hunch drove every design decision.

## Approach
Before mocking up anything, I distilled the brief into five concrete design goals. This quick-hit table shows what I chose to focus on and how I tackled each item.

| Goal | Tactic |
| ---- | ------ |
| Legibility for aging eyes | Large font, high contrast, sans-serif for easy scanning. |
| Inject warmth (kill the "modern cold" sterotype) | Earth-tone palette adds approachability without sacrificing sophistication |
| Make the avant-garde photos support, not hijack | Converted hero image to low-opacity line art that doesn't detract. |
| Break content into chunks | Three slender schedule columns plus full-bleed map block create natural pauses. |
| Way-finding | Navigating campuses is challenging, lets give them a campus map. |

## Design
### Hero Image
To weave the required photo into the layout without letting it shout over the text, I turned it into architectural line work:

1. Placed the image in Keynote, dropped opacity to 20 %.
2. Traced main edges with the pen tool.
3. Removed the image and added additional detail to line drawing.

Result: it whispers “architecture” while letting typography lead.

<p id="render-photo-section" style="display:flex;">
  <img src="/public/museum/HouseOriginal.png" alt="Original photograph of an avant-garde building" style="width:32%;">
  <img src="/public/museum/HouseLines.png" alt="Lower opacity version of photo with outlines laid down" style="width:32%;">
  <img src="/public/museum/HouseRender.png" alt="MRender of the photograph with just lines" style="width:32%;">
</p>

**Figures 1-3:** _Original photo → line overlay → final line-only render._

### Grid: Content-First, Then Formalized
I actually started with about **ten super-rough grid doodles** in my sketchbook just to see if anything jumped out. They didn't. Every sketch felt like I was _forcing_ the content to fit my design when I should let the content dictate its own design. So I pivoted:
1. **Dumped everything in Keynote** at true scale—four pages of text, hero line art, and a campus map.
2. **Shuffled** the pieces in grayscale through seven passes, watching how much breathing room the text truly needed.
3. **Reverse‑engineered the emerging structure** into a formal grid I could defend.

<p id="bw-mockup" style="display:flex;">
  <img src="/public/museum/BWMockup1.png" alt="Mockup 1 has the itinerary as two columns in the center and the map centered at the bottom" style="width:32%;">
  <img src="/public/museum/BWMockup2.png" alt="Mockup 2 has the itinerary as two columns with the map as part of the columns" style="width:32%;">
  <img src="/public/museum/BWMockup3.png" alt="Mockup 3 has the itinerary as three columns with the map as its own section on the bottom half" style="width:32%;">
</p>

**Figures 4-6:** _Testing different columns and map placements for Step 2._

#### Why This Grid Works
- **Reliable rhythm, familiar frame:** A uniform margin wraps the entire poster and sits between each of the three body columns. That consistent negative space creates a steady visual cadence—readers always know where a block starts and ends.
- **Clear semantic zones:**
  - Header, three-column body, and footer all live neatly inside the margin rails, signalling _“core content—start reading here.”_
  - Map / event-details band throws the rulebook out the window: it ignores the side margins and bleeds edge-to-edge. That break in the rhythm instantly tells viewers, _"different kind of information—pause and orient yourself.”_
- **Attention by controlled disruption:** Two hero photos deliberately pierce the column grid. Their overshoot grabs the eye, but because everything else stays disciplined, the disruption feels intentional, not chaotic.
- **Built-in scan paths:** The tight columns encourage a top-to-bottom “newspaper” read. Full-bleed map section interrupts this flow with two boxes. This results in a natural zig-zag.

<p id="grid-mockup" style="display:flex;">
  <img src="/public/museum/RoughMockups.png" alt="Sheets of paper with different layouts for the poster" style="width:49%;">
  <img src="/public/museum/poster-grid.png" alt="Final grid with 3 columns and map in its own section" style="width:49%;">
</p>

**Figures 7 & 8:** _Rough grid doodles → refined, final grid._

### Typography Experiments

Avant-garde letter-forms looked cool but tanked legibility. Big, bold, and boring won the usability test. 
I flirted with avant-garde title treatments (photo-filled letters, buildings forming glyphs) before reality—“retirees need clarity”—won. The final title is big, bold, and dead simple.

![Versions of the title with images as the background of the text and buildings forming the letters](/public/museum/TitleMockup.png)

**Figure 9:** _Typography experiments._

### Color Play
Tested a family of warm reds, russet browns, and muted oranges against a cool ash background. Landed on a deep terra-cotta for call-outs and a softer clay for accents—inviting, but calm enough for coffee-shop bulletin boards.

<p id="color-test-section" style="display:flex;">
  <img src="/public/museum/ColorMockup1.png" alt="Ash poster with map section in a dark grey" style="width:49%;">
  <img src="/public/museum/BWColorMockup2ockup2.png" alt="Ash poster with map section in a orange" style="width:49%;">
</p>

**Figure 7-8:** _The tonal range I explored._

## Final Result
- **Audience-first:** Every choice stems from the retiree assumption—legible type, accessible palette, friendly tone.
- **Hierarchy on lock:** Grid + chunking guides the eye: what, when, and where.
- **Balanced personality:** Architectural, warm, and restrained.

![Poster in shades of orange and peach with images of avant-garde building, a map with the location of the event, and the itinerary](/public/museum/poster-official.png)

## Insights
I learned a number of things from this project both in terms of how to structure a poster but also

- **Audience.** It's really hard to know how to choose colors, styles, layouts, and sizes without really knowing who your audience is. I made quite a few assumptions when doing this so I may have targeted completely different people than the intended audience.
- **More is More?** It's also so challenging trying to find a balance of providing details or information but also keeping the product streamlined and comprehensive. I still go back and forth whether the map is adding value or making the layout weird, if the photos didn't have to be renders, or if I shouldn't have included stats like nationality.
- **Grid-ing.** Using a grid as the basis of all design is super helpful. It allows you to be more creative, bucket information together, divide sections, and direct attention.

[^1]: **Project Details:** Took 1 week to develop. Worked solo. Used Keynote to mock up.
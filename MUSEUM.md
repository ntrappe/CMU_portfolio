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
The first assignment in my Prototyping course at UC San Diego was to understand how to use underlying grid systems. We were told to create a digital poster with the following requirements:

- Must be a static digital dislay
- Dimensions must be 1024px wide and 1600px tall
- Must use an underlying grid system
- Use at least one image from a folder (modifications allowed)
- Have to use all of the text provided


This initially was a major challenge for the vast amount of text we would _HAVE_ to incorporate:

![3 sheets of paper with text to showcase how much content needs to be included](/public/museum/content-req.png)

## Research
We got **zero** input on audience or goals. All we received was that wall of text and a folder of photos. So I reverse-engineered a likely viewer:

- **Schedule clues:**
  - Thu 5:30 – 7:30 PM
  - Fri 9 AM – 12:15 PM, 2 – 4:45 PM, 5:30 – 6:30 PM
  - Sat 9 AM – 12:30 PM

Those weekday, business-hour slots rule out 9-to-5 folks. I’m betting on retirees who have free daytime hours.

## Approach
Given that this was going to be a poster for retirees to get them interested in learning about architecture I had 5 things to keep in mind:

### 👀 Legibility for aging eyes
Large type, high contrast, and a workhorse sans-serif. Easy to read from across a lobby. _Not the simplest task with 3 pages worth of content to fit._

### 🖼️ Integrate Images
Avant-garde buildings are gorgeous—but noisy. I needed them to support the message and mesh with my poster, not distract from it.

### ☀️ Warmth over “Modern Cold”
A rich, warm palette counters the usual steel-and-glass chill of architecture posters.

### 📏 Chunking the Content
Three pages of copy feels like fifty. I broke the poster into bite-size blocks so the eye can hop instead of slog.

### ✨ Useful Extras
- **Way-Finding:** Campuses are hard enough to navigate, let alone in NYC. We need a map.
- **Representation Check:** Highlight speakers’ range of backgrounds where possible.

## Design
### The Photos
I dropped a hero image into Keynote, dropped opacity, then traced major lines. The resulting drawing lets me weave the architecture into the layout without taking attention from the text or design schema.

<p id="render-photo-section" style="display:flex;">
  <img src="/public/museum/HouseOriginal.png" alt="Original photograph of an avant-garde building" style="width:32%;">
  <img src="/public/museum/HouseLines.png" alt="Lower opacity version of photo with outlines laid down" style="width:32%;">
  <img src="/public/museum/HouseRender.png" alt="MRender of the photograph with just lines" style="width:32%;">
</p>

**Figures 1-3:** _Original photo → line overlay → final line-only render._

### Layout Iterations
We were required to generate as many layout ideas as possible. I roughly sketched out different grids.

![Sheets of paper with different layouts for the poster](/public/museum/RoughMockups.png)

I'll be honest: _I didn't want to sketch or do lo-fi mockups_. When content volume is predetermined, I'd rather let _it_ steer my design rather than forcing it to fit into mine. Instead of starting with abstract boxes, I placed the full text, images, and map at scale in Keynote. Through seven monochrome passes I adjusted positioning, spacing, and visual weight until the reading flow felt intuitive. 

Only then did I derive the formal grid: three narrow schedule columns and a dedicated map section.

<p id="black-white-mockup-section" style="display:flex;">
  <img src="/public/museum/BWMockup1.png" alt="Mockup 1 has the itinerary as two columns in the center and the map centered at the bottom" style="width:23.5%;">
  <img src="/public/museum/BWMockup2.png" alt="Mockup 2 has the itinerary as two columns with the map as part of the columns" style="width:23.5%;">
  <img src="/public/museum/BWMockup3.png" alt="Mockup 3 has the itinerary as three columns with the map as its own section on the bottom half" style="width:23.5%;">
  <img src="/public/museum/poster-grid.png" alt="Mockup 3 has the itinerary as three columns with the map as its own section on the bottom half" style="width:23.5%;">
</p>

<div style="display:flex;">
  <img src="/public/museum/BWMockup1.png" alt="Mockup 1 has the itinerary as two columns in the center and the map centered at the bottom" style="max-width:50%;">
  <img src="/public/museum/BWMockup2.png" alt="Mockup 2 has the itinerary as two columns with the map as part of the columns" style="max-width:50%;">
  <img src="/public/museum/BWMockup3.png" alt="Mockup 3 has the itinerary as three columns with the map as its own section on the bottom half" style="max-width:50%;">
  <img src="/public/museum/poster-grid.png" alt="Mockup 3 has the itinerary as three columns with the map as its own section on the bottom half" style="max-width:50%;">
</div>

**Figures 4-7:** _Two columns (center) + map (center, bottom) → two columns + map (in columns) → three columns + map (own section) → grid._

Only then did I derive the formal grid: 
- Three narrow schedule columns
- Consistent margins anchoring the title, footer, and body
- A full-bleed map/info section to break it up
- Two photo blocks that pop outside the grid to catch the eye

### Typography Experiments
I flirted with avant-garde title treatments (photo-filled letters, buildings forming glyphs) before reality—“retirees need clarity”—won. The final title is big, bold, and dead simple.

![Versions of the title with images as the background of the text and buildings forming the letters](/public/museum/TitleMockup.png)

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
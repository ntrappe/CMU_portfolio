# Tesla Vacuum[^1]
| A lightweight, powerful, and portable vacuum. |
| -------- |

![Orange vacuum with bad signifiers and affordances vs the redesign with better icons and usability](public/vacuum/vacuum-preview.png)


## Table of Contents
1. [Problem](#problem)
2. [Background](#background)
3. [Research](#research)
4. [Approach](#approach)
5. [Design](#design)
6. [Final Result](#final-result)
7. [Insights](#insights)



## Background
In DSGN 1—grounded in _The Design of Everyday Things_—we set out to redesign a common student tool or appliance. Through an initial mind‑mapping exercise, we identified everyday objects that every college student encountered, from water bottles and iClickers to car fobs. Vacuums emerged as a clear candidate: nearly every dorm room needed one, yet conventional models were heavy, noisy, and awkward to operate. Our goal was to apply core principles of affordances, signifiers, feedback, and discoverability to redesign a student vacuum.

![Mind map of possible student appliances and tools to redesign](/public/vacuum/mind_map.png)

## Problem
How might we design a cordless vacuum for students that feels lightweight, is easy to empty, and stays quiet enough to use in shared spaces?

## Research
### Quantitative Evaluation
We sourced 15 different vacuums—ranging from bulky upright models to lightweight sticks—and scored each on:

- **Suction vs. Noise:** Measured peak suction power alongside decibel readings at one meter.
- **Durability vs. Portability:** Assessed build materials and failure reports against weight and form factor.

Plotting these axes revealed clear trade‑offs: high‑suction models were too loud for shared suites, while the quietest were flimsy and difficult to maneuver.

![Two axis, one for noise (i.e. when the vacuum is on) and the other for suction (i.e. how strongly it pulls up debris)](/public/vacuum/suction_noise.png)

**Figure 1:** Suction (↑) vs. Noise (↓) across a subset of vacuums. Vacuums with powerful suction often were noisy.

![Two axis, one for portability (i.e. ease of carrying) and the other for durability (i.e. lifespan)](/public/vacuum/durability_portability.png)

**Figure 2:** Durability (↑) vs. Portability (↑) across a subset. Vacuums with high portability often had low durability.

### Contextual Inquiry
Next, we invited the 15 vacuum owners to demonstrate their devices in situ. As they navigated carpet-to‑tile transitions, untangled cords, and emptied dustbins, we:

1. 🔬 Observed use patterns—particularly cable snags around furniture legs and corners.
2. ⏱️ Timed routine tasks to gauge efficiency bottlenecks.
3. 📋 Interviewed each participant about likes, dislikes, and workarounds.

Our affinity mapping distilled three dominant pain points:
- **Trip Hazards & Cord Management:** Users repeatedly tripped or stopped to rewind cables.
- **Complex Emptying Process:** Buttons were hard to find; reseating bins required extra force and guesswork.
- **Non‑Intuitive Controls:** Power and suction adjustments lacked obvious signifiers, leading to fumbling and wasted time.

## Approach
### Defining the "Worst" Baseline
By overlaying our quantitative plots with the qualitative themes, we pinpointed the single underperforming model that combined excessive noise, poor portability, and confusing emptying. This “worst” vacuum became our redesign canvas, maximizing the opportunity to demonstrate improved user experience.

### Ideation & Feature Prioritization
Focused on the top pain points, we sketched dozens of concepts before converging on four pillars:

1. **Portability & Affordances**
- An articulating swivel joint—modeled on bus‑accordion connectors—lets the wand bend under low furniture.
- A pistol‑grip handle with a molded cradle makes it unmistakable where to hold.
2. **Quiet, Powerful Suction**
- Inspired by Tesla’s silent electric motors, we specified a brushless digital motor with acoustic insulation.
- A graded suction dial—complete with detents and an LED ring—lets users feel and see each setting.
3. **Clear Signifiers & Controls**
- **Power Button:** Red, with the classic ⏻ icon and haptic click.
- **Empty Button:** Magenta, embossed with a disposal icon.
- **Release Button:** Blue, marked with a chamber‑detach graphic.
4. **Rich Feedback Loops**
- Haptic pulses when powering on/off.
- Tactile “snap” when the dustbin locks.
- Charging LEDs on the handle: green (>20%), yellow (10–20%), red (<10%).

## Design
In our redesign, every element was driven by Norman’s key principles: **affordances**, **signifiers**, **feedback**, **mapping**, and **discoverability**. Here’s how each principle shaped the “Tesla Vacuum.”

### Affordances
> **Definition:** The physical form suggests how it's used.

- **Articulating Connector (“Bus Joint”)**
  - _Why?_ Users repeatedly tripped over rigid wands or couldn’t reach under low furniture.
  - _Principle:_ The accordion‑style joint naturally bends when you press it under a couch. Its shape invites flexing—no instructions needed.
- **Ergonomic Pistol‑Grip Handle**
  - _Why?_ Students struggled to find a comfortable place to hold, leading to wrist strain.
  - _Principle:_ A molded grip cradles the palm and fingers; its silhouette screams “grab me here.”

![Grey vacuum with articulated connector between base and body. Obvious buttons on handle and dirt chamber. No cords.](/public/vacuum/tesla-vacuum.png)
**Figure 3:** The "Tesla" Vacuum. Our redesign is portable, with powerful suction, and maneuverability.

### Signifiers
> **Definition:** Cues that indicate where and how actions should occur.

- **Red Power Button**
  - High‑contrast red and the universal “power” symbol make startup/shutdown immediately obvious.
- **Magenta “Empty” Button**
  - A salient color indicating a major action will occur and a symbol with the bottom of the bin open signal “this is how you release debris.”
- **Blue “Release” Button**
  - Distinct hue and a dirt-chamber removed graphic clearly differentiate “remove chamber” from “empty chamber.”
- **LED Ring Around Suction Dial**
  - Illuminated segments correspond to each suction level, inviting users to twist the dial.

![](/public/vacuum/buttons.png)
**Figure 4:** Iterating over the "empty" and "release" buttons. 

### Feedback
> **Definition:** Immediate, perceivable response to user actions.

- **Haptic Pulse on Power On/Off**
  - Confirms the button press even in noisy environments.
- **Tactile Detents & Light on Dial**
  - Each suction‑level click is felt and seen via LED segment lighting.
- **Audible “Snap” on Chamber Lock**
  - A crisp click lets users know the bin is secured before they resume cleaning.
- **Charging Indicator LEDs**
  - While plugged in, a small lightning‑bolt icon glows: green (>20% charge), yellow (10–20%), and red (< 10%).

### Mapping
> **Definition:** Relationship between controls and their effects.

- **Dial-to-Suction Correlation**
  - Turning the dial clockwise increases suction in predictable, linear increments, reinforced by equally spaced LED segments.
- **Color-to-State Mapping**
  - Intuitive traffic‑light color scheme (green→yellow→red) for battery status.

### Discoverability
> **Definition:** Essential functions must be obvious without a manual.

- **Visible Button Placement**
  - Power button is near the handle. Empty and release are grouped on the dirt chamber.
- **Iconography & Contrast**
  - High‑contrast symbols on each control surface make their purpose legible at a glance.
- **Translucent Dirt Chamber**
  - Transparency ets users see dirt level before it overflows.

[^1]: **Project Details:** Took 3 weeks to develop. Worked in a team of 4. Mocked up designs in Keynote.
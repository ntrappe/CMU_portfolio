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
Millennials visit national parks less than any other previous generation. Because of this, the National Park System (NPS) is concerned about securing enough funding (as most is generated through visitation). Millennials are overwhelmed with the process of selecting a national park to visit. They don’t know how to select a park, what to look for, and which hikes are suitable.

## Background
This project was part of my Prototyping course at UC San Diego. Our objective was to build an interactive and innovative mobile information system to address a user problem. We were allowed to chose any problem of interest so long as we employed moodboards, wireframes, prototypes, and syle guides.

Two months before this project began, I was waiting in line for the shuttle at Pinnacles National Park. It’s a park full of towering cinnamon-colored talus rocks, hidden caves, deep gulches, and enormous condors. I ended up speaking to a very chatty Park Ranger about the state of affairs at Pinnacles. Here, I learned two things. First, the few very well recognized parks (e.g. Yosemite) were getting the bulk of visitors, leaving lesser-known parks (e.g. Pinnacles) with less visitation (and therefore less funding). Second, there was a clear generation gap in that most of the visitors were older folks who’d grown up hiking.

![Cinnamon-colored talus rocks of Pinnacles National Park](/public/rock/pinnacles.jpg)

## Research
### Articles & Interviews
When I was presented with the opportunity to create an app for anything, I knew I had to dig deeper into that conversation. To determine whether there was a clear problem to be solved, my team and I dove into research. We sifted through news articles and interviews to understand whether (a) the parks were suffering financially and (b) if a lack of millennials was the problem. No quote could better back this up than one given by the National Park Service (NPS) director.

> “If we were a business and [millennials were] our clientele, then over the long term, we would probably be out of business.” — Jonathan Jarvis

All the evidence we collected indicated that (a) millennials were visiting parks less than baby boomers and (b) visiting national parks were the best ways to support the parks. So, now we knew that there was definitely a problem. But what was causing it? _Why weren’t millennials visiting National Parks?_

### Surveys
To investigate this, we surveyed 50 millennials across a variety of demographics. You can check out our survey [here](https://forms.gle/h2bxRMqGSMJAn3pt6). Four key trends emerged when we analyzed the data:

- **77%** of respondents had a desire to go to a National Park
- **74%** of respondents agreed more people should visit National Parks
- **55%** of respondents had not visited a Park in the past 12 months
- **80%** of respondents were not confident in their knowledge of the Parks nearest to them

Now, this was more confusing. Millennials cared about the environment and wanted to go to National Parks but … weren’t? We had to dig a little deeper and interview respondents about what was motivating them or discouraging them from visiting the parks. While time was often a consideration, a major trend emerged: planning. They didn’t know where to start. What park? What to bring? What to see?

> “I’m not confident in my ability to go to a national park by myself (deriving, planning, directions, packing, etc.)” — Daniel Wang[^2]

Our key findings suggested that millennials want to visit parks but are frustrated with the process of how to do so. They both needed lots of information—where to go, what hike to do, what to bring, what weather conditions—but not enough to be overwhelmed.

> “I’m confused on the process of going. I believe you may have to book in advance to go to Yosemite? I know there’s more steps to the process but I’m not sure how to start.” — Melissa Roberts[^3]

### Market Research
Millennials were clearly asking for a centralized hub of information. Before we built our own, we wanted to see what the market had to offer. Maybe this was just a problem of awareness? Did an app already exist that could support planning visits to National Parks?

Kinda? We compared the 10 most popular apps and websites and found that many provided lists of hikes, directions, and photos, but weren’t solving our problem. The majority lacked a comprehensive guide for each park geared towards a novice who didn’t know what to look for. Many didn’t provide pertinent information on conditions, closures, filters for difficulty, equipment requirements, and more. If you’d like to see our full breakdown, you can find it on this [Google Doc](https://docs.google.com/document/d/1eKqaEfm-ZcYMHUdmKS3_RhwLTFxx08vJjQCDKVrxwAA/edit?usp=sharing).

![Table of all apps on the market compared across features like operating hours and maps](/public/rock/MarketResearch.png)

## Approach
When thinking about designing the app, I focused on five questions:

1. ⭐️ How do we make it fun?
2. ✌️ How do we appeal across millennials?
3. 💡 How do we get people interested in a park?
4. ℹ️ How much information do we want to provide?
5. 📅 When will they be using this?

### Hiking is Fun
First, millennials were feeling overwhelmed and stressed so we wanted our app to evoke the opposite feelings. We wanted them to feel excited, adventurous, and happy. We wanted them to be in awe of the parks not in dread. The first concept of fun was color. How could we bring in pops of color to the app?

### Broad Appeal
Second, we had a broad audience. We were targeting a large demographic across genders, socioeconomic statuses, and races. For that reason, we also wanted the app to feel minimalist, modern, and fairly neutral in its core color scheme. We wanted it to feel familiar and intuitive.

### Show Don't Tell
Third, the best way to sell a park is to show a park. The National Parks are gorgeous and impressive and we were going to lean heavily into photography.

### The Challenge
Fourth, the most challenging part—and arguably most important part—of this application would be how much information to provide and how to display it. We needed to find a balance of educating our audience without overwhelming them. We had to provide novices they might not know to check without making them feel uncomfortable.

### Set the Scene
Fifth, as a Software Engineer, I always ask the context around the use of an application. This app could be used at home while debating on going to a National Park, on the drive to a Park checking conditions, or even in the Park while on a hike. Given that National Parks rarely have good cellular connection, our app would have to provide all the information someone might need without network. This meant we would want to have offline maps, trail details, and more.

## Design
# ⭐️ Designing the Fun
Our initial challenge in design was to find a balance between minimalism and fun. The bulk of our mockups were actually high-fidelity because we wanted to nail the look and feel of our previews. We needed to find a balance of how much color to use to make it fun but not distract from the parks. To determine our design, we conducted three rounds of A/B testing and iterated through a number of designs.

![First round of A/B testing had hike previews with pastel colors and some with borders, others with shadows, etc.](/public/rock/PreviewTestA.png)

We also played around with the size of the previews, what information to display, and a light vs dark mode.

![Second round of A/B testing had hike previews in dark and light modes](/public/rock/PreviewTestB.png)

With the feedback we received from users, we decided that the photo of the National Park should take up the full width of the preview. While having colorful backgrounds—even half-height colorful backgrounds—were fun, we didn’t want to take away from the parks. Those photos had enough color and we wanted them to be the focal point. So we increased the size of the photos and removed the unnecessary colorful additions.

![After a round of feedback, hike previews would showcase as much of the image as posssible](/public/rock/PreviewTestC.png)

## Final Result
<video controls src="https://github.com/ntrappe/CMU_portfolio/blob/main/public/rock/rock_demo.mov" title="rock app demo video"></video>

**Demo of the App.** See the app in action as we browse parks and hikes and set filters to narrow our options. If you'd prefer to try it out yourself, find it [here](https://www.figma.com/proto/ywP4mSyfwGENQ4pwyzv1vW/A4-National-Park-App?type=design&node-id=580-4846&t=g8QpYQoQiVCjQTzi-1&scaling=scale-down&page-id=580%3A4841&starting-point-node-id=580%3A4846&show-proto-sidebar=1).

## Insights
- **Design for Context, Not Just Content.** Anticipating where and how people use the app—at home, on the road, or in the park—drove our decision to include full offline maps and downloadable trail data. Designing around real‑world constraints (spotty cell service, on‑trail reference) made the experience reliable and trustworthy.
- **Let the Experience Shine.** Removing extraneous color blocks and leaning into immersive park photography kept the UI minimal yet evocative. When your content is stunning visuals of Yosemite or Pinnacles, clean layouts amplify the user's sense of wonder.
- **A/B Testing is King.** Every round of A/B testing or critique pointed out new things we hadn't considered and made our app better each time. It's never something to discount!

[^1]: **Project Details:** Took 2 months to develop. Worked in a team of 3 as the lead. Used Keynote and Figma.
[^2]: **Privacy:** This is not the participant's actual name to preserve privacy.
[^3]: **Privacy:** This is not the participant's actual name to preserve privacy.
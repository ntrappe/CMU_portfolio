# Pomodoro Timer
A web-based timer designed to curb procrastination.

![Desktop with many windows open and timer in corner](public/pomodoro/pomodoro-preview.png)

| Duration | Team Size | Role | Domain | Try It |
| -------- | --------- | ---- | ------ | ------ |
| 2 months | 11 members | Lead | Web Dev | [Netlify](https://cse110team33.netlify.app/) |

## Table of Contents
1. Problem
2. Background
3. Research
4. Approach
5. Design
6. Final Result
7. Insights

## Problem
Engineering students need to complete giant programming assignments without getting overwhelmed or burnt out. Without a way to break up work into smaller tasks and work for shorter periods of time, engineering students will suffer from a lack of productivity and, potentially, fail to complete assignments.

## Background
At UC San Diego, in my Software Engineering course, we were told to create a pomodoro timer. We had full control over the design and implementation but it had to abide by the Pomodoro Technique. The technique is as follows:

- Work for a “pomodoro” (a period of 25 minutes)
- After a “pomodoro” — take a 5 minute break
- After 3 “pomodoros" — take a longer 15 minute break
- If a “pomodoro” is interrupted, it is forfeited and must be restarted

## Research
### Analyze the Competition
If we had been hired to create a timer—rather than assigned it in class—we would want customers to use our product. To do this, we would have to position ourselves uniquely on the market and find ways to prove that our solution was superior. As a team, we investigated the 6 most popular timers.

![Popular pomodoro timer website](/public/pomodoro/pomofocus.png)

A number of problems emerged:
- Most timers had a pause/stop button during a “pomodoro” which violated the technique (it should be forfeited).
- All the timers had salient colors, gamification, or notifications—all of which were distracting (another violation).
- Some timers lacked clear signifiers or feedback which reduced usability.

### Try the Technique
While it would be better design practice to source a group of engineering students and conduct a survey or user experience data, we were not afforded the time to do so. Instead, we—engineering students—tried the Pomodoro Technique while completing assignments in our other engineering classes to analyze how the Technique would work for this audience.

## Approach
### Simplicity is Key
As engineers, we'd rather drown in a sea of features than restrain ourselves to work on something as "simple" as a timer (the horror). As a result, this project was a humbling reminder that we design for users and not ourselves. We distilled our initial pile of features down to a handful by asking five questions about each:

- Who does this benefit?
- What is the context?
- When would the answer work?
- Where would the answer work?
- Why is this a problem?

### Sketch it Out
Next, we drew some mockups to visualize how a user might interact with our app. This helped us simplify the controls, improve the layout, and make sure the timer truly was the star of the show.
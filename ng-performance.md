# Intro
## Techniques for performance
- Reduce work
- Distribute Work
- Priortize work

# Angular Performance enhancements


## RAIL Model - https://web.dev/articles/rail
- for load - 300ms
- Human eyes do well on 60 fps and above

# Angular performance
- Appref will call tick
- Settimeout causes a tick to happen

## Manual change detection
- markForCheck 
- detectChanges
## CD with async pipe
- marks the component
- informs the appRef to do tick
## CD with Signals

## Zoneless
- ChangeDetectionScheduler
- It is currently theta phase 
	- Its theta coz you can't use your keyboard to type
- markForCHeck is the way to go and will not a problem even if you call it multiple times
	- detectChanges can be avoided	

# Framework Agnostic enhancements

## Browser Render Pipeline
- Purple is coordinate and green is color
- Look at https://github.com/nuxt/nuxt.com/pull/1476

## Core web vitals
### LCP - https://web.dev/lcp
- Should be under 2.5
- Image Text, block level elements, video
- Browers evaluates all the candidates and whichever is largest is considered LCP
- Only at bootstrap
### INP
- should be under 200ms 
- Happens constantly
- Input delay as browser is doing something else before it can pick up current event
### CLS - Visual Stablity
- Should be under 0.1 - 0.25
- It measures visual ability of the app, jumpiness of the app
- It generates trust to users if CLS is good
## Other Vitals
- TTFB, FCP, TBT, TTI

# Performance
## Lanes
- Flimstrip
- Network 
- Experience
- Main Thread
- Search Pane
## Flame Chart Analysis
- Long tasks are >= 50ms
- W, A, S, D keys can help in browing around the chart
- Shift to select a frame
- When done with search, close as it slows down dev tool
- Frame rendering stats in more tools

# Concurrency Model & Event Loop - Basics of scheduling tasks
## Event Loop
- Macrotask - Timer, IdleCallback, MessageCHannel, rAF
	- rAF forces app to repaint
	- If multiple rAF is requested then will be executed in same task
- Microtask - Promise, queueMicroTask - Always follow the sequence of code

# Master the Single Thread
- Heaviest task - Evaluating templates aka rendering aka CD
## Split template work
- rxLet - Distribute template work with structutal directives
- rxFor 
	- downside 

#### Notes
- https://github.com/push-based/user-flow
- https://github.com/code-pushup/cli
- Knip

### Questions
- https://www.rx-angular.io/docs/eslint-plugin/rules

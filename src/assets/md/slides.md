# Lessons Learned 2017

## ... an epic tale of struggle, heroism, battle with dragons

### ... and rescuing princesses
![rescuing-princesses](./assets/img/rescuing-princesses.png)

## Motivation

### Technical Debt
![technical-debt](./assets/img/technical-debt.png)

### Reflection
![reflection](./assets/img/tree.png)

### Connect some dots
![connecting-dots](./assets/img/connecting-dots.jpg)

### Jeet Kune Do
![bruce-lee](./assets/img/bruce-lee.png)

### A -> B

### Kai Zen (Change + Good)
![kaizen](./assets/img/kaizen.svg)

### Iteration

## The story so far

### Late 2013 FOSS & Full-Stack JS Focus

### 2015 SPA Architecture Lessons (vol. 1)
- Brokered a domain name -> $$
- Creative Coding Projects (based on Three.js Arch)
- OOP was not dead, but hit a wall

### 2016 Arch Lessons Learned (vol. 2)
- Discovered functional programming
- Cycle.js -> initial proto-framework formations
- First prototypes -> Jam Station, MongoAdmin, 2D Side Scroller

## 2017

### Jan: 1st Music Hackathon
![rc505](./assets/img/rc-505.jpg)

### Feb: A first attempt at teaching Functional Programming
![attempt](./assets/img/attempt.jpg)

### Mar: Startup Weekend Plovdiv
![musevis](./assets/img/musevis-getting-ready.jpg)

### Musevis
Grow your audience or land a record deal with kick ass visualizations


![logo](./assets/img/musevis-logo.png)

### ... The team
![musevis](./assets/img/musevis-team.jpg)

### Mar: Pimpin' the feedback loop
![75prc](./assets/img/pimp-my-spectrum.jpg)

### May: A bit on modeling data
![pandora](./assets/img/pandora.jpg)

### ... CQRS / CQS
![cqrs](./assets/img/cqrs.png)

### ... Event Sourcing
![event-sourcing](./assets/img/event-sourcing.png)

### Sonar Innovation Challenge 2017

![sonar](./assets/img/sonar.png)

1 month prep + 4 days hackathon

### ... I had to apply
![sonar](./assets/img/sonar-challengers.png)

### ... Detection model
![sonar](./assets/img/sonar-detection-model.png)

### ... Devices & Tech Stack
![sonar](./assets/img/sonar-devices-tech-stack.png)

### Nov: 2nd Music Hackathon
![star-trak](./assets/img/star-trak.png)


## So what's in the box
![app-architecture](./assets/img/app-architecture.png)

### ... get ready for
![inception](./assets/img/inception.gif)

### ... Inception
```js
// actions
const actions$ = new Rx.Subject();
const actions = {
	incr: () => actions$.onNext(
		state => ({num: state.num + 1})),
	initial: {num: 0}
};

// ui (hyperscript)
const {div, span, button} = vdom;
const ui = ({state, actions}) => div('#ui', [
	button({on:{click: () => actions.incr()}}, 'Incr'),
	span(`Num: ${state.num}`)
]);

// reducing the stream of actions to the app state
const state$ = actions$
	.startWith(() => actions.initial)
	.scan((state, reducer) => reducer(state), {})
	.share();

// mapping the state to the ui
const ui$ = state$.map(state => ui({state, actions}));

vdom.patchStream(ui$, document.querySelector('#ui'));
```

## Case Studies


## Live coding


## Questions

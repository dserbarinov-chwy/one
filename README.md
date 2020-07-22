# One
_Micro-Frontends POC with React and Vue_

The goal here is to use multiple frameworks in a single-page application.

## Design Decisions

### Switching between micro-frontends via a JS router

We need a top-level router to load different micro-frontends.
Luckily, it's a solved problem.
For this POC, I am using [single-spa](https://single-spa.js.org/) to provide this top-level router.
It's features are compelling:
- When a route is active, it downloads and execute the code for that route.
- Each route's application can (optionally) be in its own git repository, have its own CI process, and be separately deployed.
- The applications can all be written in the same framework, or they can be implemented in different frameworks.

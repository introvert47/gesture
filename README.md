Here's a README-ready description you can drop straight in:

Particle Nexus — Gesture-Driven 3D Particle Field
A real-time, gesture-controlled particle system built with Three.js and MediaPipe Hands. Show your hand to the camera to morph, expand, recolor, and burst a field of thousands of GPU-rendered particles across 12 different shapes — no controllers, no keyboard required.
Features

12 morphable particle shapes: Nebula, Heart, Flower, Saturn, Firework, Torus, Butterfly, Star, Spiral, Wave, DNA, Globe — each particle smoothly morphs into the next rather than cutting between shapes.
Live hand tracking via MediaPipe Hands, with a mirrored camera preview and real-time hand-skeleton overlay so you can see exactly what's being tracked.
Custom GLSL shader particles — soft circular sprites, per-particle color, GPU-side hue rotation — tuned to avoid the washed-out/blurry look of naive additive blending.
FPS-based auto quality scaling: silently reduces particle count once if sustained frame rate drops, so it stays smooth on lower-end hardware.
Full fallback controls: works without a camera via mouse drag / touch (custom lightweight orbit controller, no external dependency), plus on-screen shape buttons — nothing breaks if camera access is denied.

Gestures
GestureEffectHold up 1–5 fingers (~0.35s)Quick-select one of the first 5 shapesOpen hand ↔ fistExpand ↔ contract the particle fieldHand left ↔ rightShift the color hueSwipe upOne-shot burst pulseSwipe left / rightCycle through all 12 shapes
Tech stack

Three.js r128 — WebGL rendering, custom ShaderMaterial
MediaPipe Hands — real-time hand landmark detection (loaded from CDN, degrades gracefully if unavailable)
Vanilla JS, no build step — single self-contained HTML file

Running it
Just open the HTML file in a browser. Camera access is optional — the app works fully with mouse/touch if declined or unavailable.

🌌 Particle Nexus

Welcome to Particle Nexus, a real-time, gesture-controlled 3D particle system built with Three.js and MediaPipe Hands. Show your hand to the camera to morph, expand, recolor, and burst a field of thousands of GPU-rendered particles — no controllers, no keyboard required.

Whether you're shaping a glowing nebula, a beating heart, or a firework burst, Particle Nexus tracks your hand in real time and reads it into fluid, continuous motion.


⚡ Features


12 Morphable Shapes: Nebula, Heart, Flower, Saturn, Firework, Torus, Butterfly, Star, Spiral, Wave, DNA, and Globe — each one smoothly morphs into the next instead of cutting between them.
Live Hand Tracking: Real-time gesture detection via MediaPipe Hands, with a mirrored camera preview and a live hand-skeleton overlay so you can see exactly what's being tracked.
Custom GLSL Shader Particles: Soft circular sprites with per-particle color and GPU-side hue rotation, tuned to avoid the washed-out, blurry look of naive additive blending.
FPS-Based Quality Scaling: Silently reduces particle count once if the frame rate drops and stays low, keeping things smooth on lower-end hardware.
Full Fallback Controls: Works with no camera at all — drag/touch to orbit, pinch or scroll to zoom, and tap the on-screen shape buttons. Nothing breaks if camera access is denied.



🖐️ Gestures

GestureEffectHold up 1–5 fingers (~0.35s)Quick-select one of the first 5 shapesOpen hand ↔ fistExpand ↔ contract the particle fieldHand left ↔ rightShift the color hueSwipe upOne-shot burst pulseSwipe left / rightCycle through all 12 shapes


🚀 Getting Started

You can run Particle Nexus instantly with no installation, build step, or dependencies to set up. Follow these simple steps:

Step 1: Download the File


Download particle_nexus.html from this repository.
Save it anywhere on your computer.


Step 2: Open It in Your Browser


Double-click the file, or drag it into any modern browser (Chrome, Edge, or Firefox recommended).
The particle field will load immediately in auto-idle mode.


Step 3: Enable Gesture Control (Optional)


Click Enable Camera when prompted.
Allow camera access when your browser asks.
Show your hand to the camera and start gesturing — no calibration needed.



Camera access is entirely optional. If you skip it or your browser denies it, the app falls back to mouse drag / touch controls automatically.




🛠️ Tech Stack


Three.js (r128): WebGL rendering with a custom ShaderMaterial for all particle rendering.
MediaPipe Hands: Real-time hand landmark detection, loaded from CDN and degrading gracefully if unavailable.
Vanilla JavaScript: No build step, no framework — a single self-contained HTML file.



📄 License

Free to use, modify, and share.

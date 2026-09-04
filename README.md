# ⚽ Free Kick Master — 3D Aerodynamic Physics Simulation

> 3D Freekick Sim with different Camera angle views.

![Free Kick Master Banner](https://img.shields.io/badge/Physics-Magnus%20Effect%20%26%20Drag-brightgreen)
![Three.js](https://img.shields.io/badge/Render-Three.js%20WebGL-blue)
![Hack Club](https://img.shields.io/badge/Hack%20Club-YSWS%20%26%20Arcade-red)
![License](https://img.shields.io/badge/License-MIT-purple)

---

## 🌟 What is Free Kick Master?
A freekick sim Browser based dont have to download.
**Free Kick Master** is built differently: it is a **physics-first, mouse-driven set-piece simulator**. You control the player directly. When you swipe and release your mouse,to Shoot the ball.Current Football techniques added Curve,Power,Knuckle

Whether you're bending a 25m finesse curler around a 4 man wall,Or just smashing the ball behind the wall.

---

## 💡 Why I Built This (Motivation)

Every freekick sim is either needs to be downloaded or does not meet the requirments So i decided to take matters in my own hands.
I set out to build a pure, zero-install WebGL simulation that captures the magic of world-class free kicks.
---

## 🚀 Key Features
### 1. 🎯 Multi-Distance Set-Piece Presets
- **25m Standard Free Kick**: Perfect for bending finesse curlers over or around a 4-man wall.
- **40m Long-Range Screamer**: Power shots around the wall.
- **50m Rocket**: Missile Shots over the walls.

### 2. 🎬 Broadcast Instant Replay System
- **Keyframe Trajectory Recorder**: Buffers 60 FPS state data during run-up, ball flight, goalkeeper dive, and wall jump.
- **Slow-Motion Playback**: Switch between **0.25x Super Slow-Mo**, **0.5x Slow-Mo**, and **1.0x Real-Time** speeds.
- **Interactive Scrubber Controls**: Play/Pause (`Space`), Rewind (`R`), and Next Kick (`Enter`).
- **Multi-Angle Replay**: Review the goal or save from any camera perspective while replaying in slow-mo!

### 3. 🎥 5 Dynamic Camera Angles
- Third Person
- First Person
- TV Broadcast
- Goalkeeper POV
- Defender View (Wall POV)
---

## 🎮 How to Play & Controls

### ⌨️ Keyboard & Mouse Reference Table

| Action | Control | Description |
| :--- | :--- | :--- |
| **Aim Target** | **Mouse Movement** | Move mouse horizontally & vertically across screen to aim reticle at goal mouth |
| **Wind Up & Charge** | **Click & Hold** / **Spacebar** |  The longer you hold, the higher the strike power (up to 100%) |
| **Execute Kick** | **Release Mouse** / **Release Space** | Leg whips forward and strikes the ball with your selected power and curve |
| **Boot Spin / Curve** | **`←` `→`** / **`A` `D` Keys** | Adjust foot contact angle: Inside Curler (negative), Straight (0.0), Outside Trivela (positive) |
| **Shot Type** | **HUD Buttons** | Toggle between **⚡ Power**, **🌀 Finesse**, and **↩ Trivela** |
| **Knuckleball Mode** | **⚡ Knuckle Button** | Striking laces through the center of the ball with near-zero spin for chaotic wobble |
| **Cycle Camera** | **`C` Key** | Cycle between Third Person, First Person, TV Broadcast, Keeper POV, and Defender View |
| **Instant Replay** | **`R` Key** / **HUD Button** | Review the last shot in slow motion |
| **Replay Controls** | **`Space`** (Pause), **`Enter`** (Next Kick) | Scrub, pause, change replay speeds (0.25x / 0.5x / 1.0x), and switch camera angles |
| **Sound Toggle** | **Speaker Icon** | Mute or unmute turf cleat footsteps, boot thumps, crowd roars, and woodwork chimes |

---

## 💻 How to Run Locally

This project requires **zero build steps, zero npm installations, and zero compilers**. Everything runs natively in any modern web browser via WebGL.

### Method 1: Direct File Opening
1. Clone or download this repository:
   ```bash
   git clone https://github.com/NEXWEB-dot/Freekick-Sim.git
   

---

## 🛠️ Tech Stack & Architecture

- **Core Rendering**: [Three.js](https://threejs.org/) (r128) WebGL Scene Graph, custom standard PBR shaders, shadow mapping, dynamic procedural turf grass textures.
- **Physics**: Custom pure JavaScript numerical integrator (Verlet / 120Hz sub-stepping) for trajectory, Magnus aerodynamics, bouncing restitution, and net collision.
- **Audio**: Web Audio API procedural sound synthesis (cleat turf impact, leather boot strike thud, metallic post resonant ping, crowd ambient murmur, and goal roar).
- **Styling**: Vanilla CSS3 Glassmorphism (`backdrop-filter: blur()`), responsive flexbox & CSS grid, hardware-accelerated animations.
- **No External Bundler**: Single clean, self-contained architecture for lightning-fast loads.

---

## 📁 Repository Structure

```
├── index.html        # Complete standalone application (Three.js 3D game, styles & logic)
├── README.md         # Documentation & Hack Club submission guide
```

---

## 🏅 Hack Club YSWS & Arcade Compliance

- **Shippable & Playable**: Completely functional end-to-end game with full physics, replay system, and multiple camera views.
- **Original Codebase**: Built ground-up with custom physics solver and procedural 3D humanoids.
- **No Build Friction**: Zero dependencies to configure; runs immediately on any computer with a browser.

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

*Made with ❤️ for football lovers, physics nerds, and Hack Club.*

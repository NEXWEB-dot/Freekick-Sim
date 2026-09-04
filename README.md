# ⚽ Free Kick Master — 3D Aerodynamic Physics Simulation

> An authentic 3D free-kick simulation where you control the kicker's run-up, swing trajectory, boot contact angle, and aerodynamic spin in real-time. Built from scratch with Vanilla JavaScript, Three.js, and Web Audio.

![Free Kick Master Banner](https://img.shields.io/badge/Physics-Magnus%20Effect%20%26%20Drag-brightgreen)
![Three.js](https://img.shields.io/badge/Render-Three.js%20WebGL-blue)
![Hack Club](https://img.shields.io/badge/Hack%20Club-YSWS%20%26%20Arcade-red)
![License](https://img.shields.io/badge/License-MIT-purple)

---

## 🌟 What is Free Kick Master?

Most soccer games reduce set pieces to a generic direction arrow and a timing bar. You tap a button, and a pre-baked canned animation plays. 

**Free Kick Master** is built differently: it is a **physics-first, mouse-driven set-piece simulator**. You control Spain's sensation **Lamine Yamal (#19)** directly. When you swipe and release your mouse, your physical kicking boot connects with the ball mesh at that exact vector and contact point. The ball's flight is solved in real time using true fluid dynamics equations—accounting for turbulent air resistance, top-spin downward dip, lateral Magnus banana bends, and chaotic knuckleball vortex shedding.

Whether you're bending a 25m finesse curler around a 4-man wall, drilling a 40m outside-of-the-boot Trivela, or unleashing a 140 km/h Roberto Carlos-style rocket from 50 meters, every kick feels distinct, weighty, and physical.

---

## 💡 Why I Built This (Motivation)

Ever since watching Roberto Carlos score his impossible banana free kick against France in 1997 and Cristiano Ronaldo's dipping knuckleball against Portsmouth in 2008, I’ve been fascinated by the physics of soccer balls in flight:
- Why does a spinning ball curve in mid-air? (The Magnus effect: asymmetric boundary layer separation causes a lateral pressure differential).
- Why does a ball hit with zero spin wobble erratically? (Unsteady vortex shedding causes fluctuating asymmetric drag forces, making the ball dip and swerve unpredictably).
- Why do almost no browser games let you *feel* the boot striking through the ball?

I set out to build a pure, zero-install WebGL simulation that captures the magic of world-class free kicks. I wanted tactile mouse-foot mechanics, authentic pitch aesthetics, a reactive defensive wall, intelligent goalkeeper AI, and a TV broadcast-style instant replay suite so you can admire your top-corner screamers from multiple camera angles in slow motion.

---

## 🚀 Key Features

### 1. 🌪️ Aerodynamics & Ball Physics Engine
- **Magnus Effect**: Computes cross-product aerodynamic force $\vec{F}_M = C_M (\vec{\omega} \times \vec{v})$, curving the ball laterally or dipping it downward.
- **Turbulent Drag Regime**: Decelerates the ball realistically according to Reynolds number air drag $F_D = \frac{1}{2} \rho C_D A v^2$.
- **Chaotic Knuckleball Dynamics**: Multi-frequency lateral and vertical turbulent wobble simulates unpredictable vortex shedding when spin is near zero.
- **Goal Netting & Woodwork Physics**: Physical netting reacts elastically with localized mesh deformation and sound synthesis upon ball entry; posts and crossbars rebound with restitution physics.

### 2. 🎯 Multi-Distance Set-Piece Presets
- **25m Standard Free Kick**: Perfect for bending finesse curlers over or around a 4-man wall.
- **40m Long-Range Screamer**: High-velocity strikes (95–133 km/h) requiring dip and curve past a 3-man wall.
- **50m Rocket**: Unbelievable long-range thunderbolts (105–150 km/h) with high apex launch velocity and late drop.
- *Distance can be selected on the Home Screen before playing or switched on the fly in-game.*

### 3. 🎬 Broadcast Instant Replay System
- **Keyframe Trajectory Recorder**: Buffers 60 FPS state data during run-up, ball flight, goalkeeper dive, and wall jump.
- **Slow-Motion Playback**: Switch between **0.25x Super Slow-Mo**, **0.5x Slow-Mo**, and **1.0x Real-Time** speeds.
- **Interactive Scrubber Controls**: Play/Pause (`Space`), Rewind (`R`), and Next Kick (`Enter`).
- **Multi-Angle Replay**: Review the goal or save from any camera perspective while replaying in slow-mo!

### 4. 🎥 5 Dynamic Camera Angles
- **Third Person**: Over-the-shoulder chase camera tracking behind Lamine Yamal and following the curling ball.
- **First Person**: Immersive kicker POV looking down the boots at the pitch and goal mouth.
- **TV Broadcast**: Elevated sideline broadcast camera that dynamically pans and scales with set-piece distance.
- **Goalkeeper POV**: Stand on the goal line between the posts, watching a 130 km/h strike curve toward you.
- **Defender View (Wall POV)**: Stand directly in the defensive wall! Watch Yamal sprint up, feel the wall leap into the air, and turn around to watch the ball plunge into the top bins!
- *Cycle cameras anytime with the **`C`** key or camera button.*

### 5. 🤖 Goalkeeper AI & Wall Mechanics
- **Trajectory Interception Solver**: Goalkeeper reads the initial velocity and Magnus spin vector to predict the net intersection point.
- **Difficulty Tuning**:
  - *Casual*: Slower keeper dive speed, smaller wall (1–3 defenders).
  - *Pro*: Realistic human reaction delay (~140ms), athletic diving saves.
  - *Legend*: Elite reflexes, full fingertip saves into top corners, 5-man jumping wall.
- **Wall Coordination**: Defenders execute a timed 20cm jump with slight human delay variations as the kicker strikes.

### 6. 🏆 World Cup Final Scenario (90+7' Minute)
- Sudden-death set-piece to win the World Cup for Spain! Complete with crowd roar, gold trophy presentation cutscene, celebrating teammates, and 3D fireworks.

---

## 🎮 How to Play & Controls

### ⌨️ Keyboard & Mouse Reference Table

| Action | Control | Description |
| :--- | :--- | :--- |
| **Aim Target** | **Mouse Movement** | Move mouse horizontally & vertically across screen to aim reticle at goal mouth |
| **Wind Up & Charge** | **Click & Hold** / **Spacebar** | Cock the kicking leg back. The longer you hold, the higher the strike power (up to 100%) |
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
   ```
2. Double-click `index.html` to open it in Chrome, Edge, Firefox, or Safari.

### Method 2: Local Static Server (Recommended)
Running via a local HTTP server ensures proper audio context permissions and asset performance:

**Using Python 3:**
```bash
cd Freekick-Sim
python -m http.server 8000
```
Then open `http://localhost:8000` in your browser.

**Using Node.js:**
```bash
npx serve .
```

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

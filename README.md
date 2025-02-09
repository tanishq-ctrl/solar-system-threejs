# Enhanced Solar System – Improved Fly-Through & Clamped Sun

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Three.js](https://img.shields.io/badge/Three.js-%23007ACC.svg?style=flat&logo=three.js&logoColor=white)](https://threejs.org/)
[![dat.GUI](https://img.shields.io/badge/dat.GUI-333333.svg?style=flat)](https://github.com/dataarts/dat.gui)
[![Tween.js](https://img.shields.io/badge/Tween.js-FFDD00.svg?style=flat)](https://github.com/tweenjs/tween.js)

Welcome to the **Enhanced Solar System** project – an immersive, interactive simulation built using Three.js. Explore a dynamic solar system featuring a custom sun simulation, realistic planetary orbits, smooth camera fly-throughs, and audio-reactive visual effects, all adjustable through an integrated GUI.

---

<p align="center">
  <img src="https://github.com/tanishq-ctrl/solar-system-threejs/blob/main/solar.gif" alt="Solar System">
</p>

[![Solar System Demo](path/to/your-image.png)](https://tanishq-ctrl.github.io/solar-system-threejs/)

## Table of Contents

- [Features](#features)
- [Screenshots](#screenshots)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
  - [Interacting with the Scene](#interacting-with-the-scene)
  - [dat.GUI Controls](#datgui-controls)
- [Project Structure](#project-structure)
- [Customization](#customization)
- [Credits](#credits)
- [License](#license)

---

## Features

- **Dynamic Sun Simulation:**  
  The sun uses a custom shader combined with a cellular automata (similar to Conway's Game of Life) rendered on a canvas texture. It dynamically reacts to audio input for distortion and scaling effects.

- **Realistic Planetary System:**  
  Eight planets orbit a central sun with unique textures, sizes, orbit speeds, and visual orbit rings for context.

- **Multiple Camera Modes:**  
  - **Orbit Mode:** Enjoy a smooth circular view around the center of the solar system.
  - **Fly-Through Mode:** Follow a predefined Catmull–Rom curve that takes you past each planet for an immersive experience.

- **Interactive Zoom:**  
  Double-click a planet to zoom in, or double-click empty space to zoom back out. Use the GUI for quick selection and zoom to a specific planet.

- **Audio Integration:**  
  Background audio is played using Three.js’s audio system and influences the sun’s appearance in real time via an audio analyser.

- **Stunning Post-Processing:**  
  Enhanced with Unreal Bloom Pass to create a glowing, atmospheric effect.

- **Live Controls via dat.GUI:**  
  Adjust simulation parameters on the fly, including bloom strength, sun simulation speed, rotation, distortion, camera settings, and audio playback.

---

## Getting Started

### Prerequisites

- A modern web browser with WebGL support (e.g., Chrome, Firefox, Edge).
- An active Internet connection (to load external libraries and textures via CDN).

### Installation

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/yourusername/enhanced-solar-system.git
   cd enhanced-solar-system

2. **Run the Project:**

   Open the `index.html` file directly in your web browser, or serve it locally using a web server. For example, with Python:

   ```bash
   python -m http.server
   ```

   Then navigate to `http://localhost:8000` in your browser.

---

## Usage

### Interacting with the Scene

- **Orbit Controls:**  
  Use your mouse to rotate, pan, and zoom around the scene. The camera automatically orbits or follows a fly-through path based on the selected mode.

- **Camera Modes:**  
  - **Orbit Mode:** The camera continuously circles the center of the solar system.
  - **Fly-Through Mode:** Enjoy a guided tour along a predefined spline path, showcasing each planet up close.
  
- **Interactive Zoom:**  
  - **Double-Click:** Double-click on any planet to zoom in; double-click on an empty area to zoom out.
  - **GUI Zoom:** Select a planet from the dropdown in the GUI and click "Execute Zoom" to focus on it.

- **Audio Playback:**  
  Simply click anywhere on the page to initiate audio playback, which will dynamically alter the sun’s visual effects.

### dat.GUI Controls

The integrated dat.GUI panel (typically displayed on the top-right) allows you to modify various simulation parameters:

- **Bloom Strength:** Adjust the intensity of the bloom effect.
- **Sun Simulation Speed (ms):** Control the update frequency of the sun’s cellular automata.
- **Sun Rotation Speed:** Set the rotation speed of the sun.
- **Sun Distortion:** Adjust the distortion level of the sun’s shader.
- **Camera Animation & Speed:** Toggle and set the speed of the camera’s movement.
- **Camera Mode:** Switch between "orbit" and "flyThrough" modes.
- **Play Audio:** Manually trigger audio playback.
- **Zoom To Planet:** Choose a planet from the dropdown to zoom in on.
- **Execute Zoom:** Apply the zoom effect based on your selection.

---

## Project Structure

```
enhanced-solar-system/
├── index.html           # Main HTML file containing all the code
├── README.md            # This file
├── LICENSE              # Project license (MIT)
└── assets/
    ├── textures/        # Planet texture images
    └── audio/           # Audio files (if stored locally)
```

- **HTML & CSS:**  
  Contains the structure, styling (including a radial gradient background and custom dat.GUI styles), and canvas element for rendering.

- **JavaScript Modules:**  
  - **Scene Setup:** Initializes Three.js scene, camera, renderer, and controls.
  - **Solar System Objects:** Creates the sun (with animated canvas texture), planets, and orbit rings.
  - **Animation Loop:** Updates planetary orbits, sun simulation, camera movements, and audio reactivity.
  - **Event Handling:** Manages window resize events, double-click zoom actions, and audio play triggers.

- **External Libraries:**
  - **Three.js**
  - **dat.GUI**
  - **Tween.js**
  - **UnrealBloomPass (for post-processing)**

---

## Customization

Feel free to extend or modify the project:

- **Replace Textures & Assets:**  
  Update the URLs in the `planetsData` array or store your own textures locally.

- **Modify Simulation Parameters:**  
  Tweak the grid dimensions, cell size, or rules of the sun’s cellular automata to experiment with different visual effects.

- **Adjust Shader Effects:**  
  Experiment with the vertex and fragment shaders to alter the distortion, color ramp, and overall look of the sun.

- **Customize Camera Paths:**  
  Modify the control points of the Catmull–Rom spline to create a unique fly-through experience.

- **Audio:**  
  Swap out the audio source URL or adjust the analyser settings for different reactive effects.

---

## Credits

- **Three.js:** [three.js](https://threejs.org/)
- **dat.GUI:** [dat.gui](https://github.com/dataarts/dat.gui)
- **Tween.js:** [Tween.js](https://github.com/tweenjs/tween.js/)
- **Planet Textures:** Sourced from various public repositories.
- **Audio Sample:** [Kendrick Lamar - tv off](https://tanishq-ctrl.github.io/solar-system-threejs/Kendrick-Lamar-tv-off.mp3)

---

## License

This project is open source and available under the [MIT License](LICENSE).

---

Enjoy exploring the enhanced solar system! Contributions, suggestions, and improvements are warmly welcomed. If you find this project interesting or useful, please consider starring the repository and sharing it with others.

```


---

Feel free to update the placeholder image links with your actual screenshots, and adjust the repository URL and any other details to match your project. Enjoy building and sharing your immersive solar system simulation!


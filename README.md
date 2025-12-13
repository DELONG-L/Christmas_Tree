# Grand Luxury Tree - Christmas Edition 🎄

An immersive, interactive 3D Christmas experience powered by **Three.js** and **MediaPipe**. This project visualizes a luxury particle tree that transforms into a photo gallery, controlled entirely by hand gestures via your webcam.

  

## ✨ Features

  * **3D Particle System:** A dynamic tree composed of thousands of glowing particles, snow, and ornaments.
  * **Gesture Control:** Use hand gestures (via Webcam) to control the animation states (Tree, Scatter, Focus).
  * **Photo Integration:**
      * Upload local files or folders directly via the UI.
      * Automatically scans a local `./images/` directory.
  * **Visual Effects:** High-end post-processing including Unreal Bloom, cinematic lighting, and atmospheric fog.
  * **Responsive Design:** Adapts to window resizing automatically.

## 🚀 Getting Started

### Installation & Running

1.  **Download the project:**
    Save the file as `Christmas_Tree.html` in your project folder.

2.  **Open the File:**
    Simply **double-click** `Christmas_Tree.html` to launch it in your default web browser.
    *(Note: An active internet connection is required to load the 3D engine and AI models).*

3.  **Grant Permissions:**
    Allow camera access when prompted to enable gesture controls.

## 🖐️ Gesture Controls

This project uses **MediaPipe Hand Landmarker** to track your hand in real-time. Ensure your hand is visible in the webcam preview (bottom left).

| Gesture | Action | Description |
| :--- | :--- | :--- |
| **Fist ✊** | **Tree Mode** | Particles assemble into the Christmas tree shape. |
| **Open Hand ✋** | **Scatter Mode** | Particles and photos explode outward and rotate with your hand. |
| **Pinch 👌** | **Focus Mode** | (Thumb & Index) Selects a random photo and brings it to the front. |

  * **Keyboard Shortcut:** Press `H` to hide/show the UI and Webcam overlay.
  * **Mouse:** Left-click and drag to rotate the view (OrbitControls).

## 🖼️ Adding Photos

### Method 1: UI Upload

Click the **"Select Files"** or **"Select Folder"** buttons in the top-right corner to load images immediately.

### Method 2: Local Directory

Create a folder named `images` in the same directory as the HTML file. Rename your photos numerically (e.g., `(1).jpg`, `(2).png`). The system is configured to scan for:

  * `./images/(1).jpg` to `./images/(200).jpg`
  * `./images/(1).png` to `./images/(200).png`

## ⚙️ Configuration

You can customize the visual parameters by editing the `CONFIG` object inside the `<script>` tag in `Christmas_Tree.html`:

```javascript
const CONFIG = {
    colors: {
        bg: 0x050d1a,         // Background color
        champagneGold: 0xffd966,
        // ...
    },
    particles: {
        count: 1500,          // Number of ornaments
        snowCount: 1000,      // Snow density
        treeHeight: 24,
        // ...
    },
    // ...
};
```

## 🛠️ Tech Stack

  * **Three.js:** 3D Rendering, Geometry, Materials.
  * **Post-processing:** UnrealBloomPass for the glowing effect.
  * **MediaPipe:** Real-time AI hand tracking.
  * **HTML5/CSS3:** UI overlay and styling.

## 📝 Credits

  * **Original Concept:** Grand Luxury Tree
  * **Modifications & Refactoring:** Delong-L
  * **Assets:** Unsplash (Demo Images)

-----

*Merry Christmas\!* 🎅

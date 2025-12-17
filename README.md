# Grand Luxury Tree - Christmas Edition V1.1🎄

An immersive, interactive 3D Christmas experience powered by **Three.js** and **MediaPipe**. This project visualizes a luxury particle tree that transforms into a photo gallery, controlled entirely by hand gestures via your webcam.

## 📂 Versions Included

This project comes with two interaction variations. Choose the one that feels most natural to you:

1.  **`Christmas_Tree_Point.html` (Recommended)**
    * **Control Style:** Uses **Index Finger Pointing** to select photos.
    * **Best for:** Intuitive selection, feels like "touching" the air. Cursor tracks the index fingertip.

2.  **`Christmas_Tree_Pinch.html` (Classic)**
    * **Control Style:** Uses **Thumb & Index Pinch** to select photos.
    * **Best for:** Precise "grabbing" actions. Cursor tracks the center of the hand/pinch.

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
    Ensure you have `Christmas_Tree_Point.html` and `Christmas_Tree_Pinch.html` in your folder.

2.  **Open a File:**
    Double-click either **`Christmas_Tree_Point.html`** OR **`Christmas_Tree_Pinch.html`** to launch it in your default web browser.
    *(Note: An active internet connection is required to load the 3D engine and AI models).*

3.  **Grant Permissions:**
    Allow camera access when prompted to enable gesture controls.

## 🖐️ Gesture Controls

This project uses **MediaPipe Hand Landmarker** to track your hand in real-time. Ensure your hand is visible in the webcam preview (bottom left).

### Common Gestures (Both Versions)

| Gesture | Action | Description |
| :--- | :--- | :--- |
| **Fist ✊** | **Tree Mode** | Particles assemble into the Christmas tree shape. |
| **Open Hand ✋** | **Scatter Mode** | Particles and photos explode outward and rotate with your hand. |

### Focus Mode (Version Specific)

How you select and focus on photos depends on which file you opened:

| Version | File | Gesture | Description |
| :--- | :--- | :--- | :--- |
| **Point Ver.** | `Christmas_Tree_Point.html` | **Point ☝️** | **Extend Index Finger** (keep others closed). <br> Cursor tracks your fingertip. |
| **Pinch Ver.** | `Christmas_Tree_Pinch.html` | **Pinch 👌** | **Pinch Thumb & Index Finger**. <br> Cursor tracks the pinch point. |

---

### Other Controls
* **Keyboard Shortcut:** Press `H` to hide/show the UI and Webcam overlay.
* **Mouse:** Left-click and drag to rotate the view (OrbitControls).

## 🖼️ Adding Photos

### Method 1: UI Upload
Click the **"Select Files"** or **"Select Folder"** buttons in the top-right corner to load images immediately.

### Method 2: Local Directory
Create a folder named `images` in the same directory as the HTML files. Rename your photos numerically (e.g., `(1).jpg`, `(2).png`). The system is configured to scan for:
* `./images/(1).jpg` to `./images/(200).jpg`
* `./images/(1).png` to `./images/(200).png`

## ⚙️ Configuration

You can customize the visual parameters by editing the `CONFIG` object inside the `<script>` tag in the HTML files:

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

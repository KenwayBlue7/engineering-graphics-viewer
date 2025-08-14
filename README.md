# 🖊️ Engineering Graphics Viewer (WebGL)

An interactive **3D Engineering Graphics Projection Viewer** built using **Unity WebGL**.  
It allows users to view 3D shapes and see their **orthographic projections** on:
- HP (Horizontal Plane — Top View)
- VP (Vertical Plane — Front View)  
…with **hidden lines automatically shown in lighter shades**.

---

## 📌 Features

- **3D Shape Rendering** — Procedurally generated Cube, Cylinder, Pyramid (extendable).
- **Orthographic Projection** — Automatic projection of vertices and edges onto HP and VP.
- **Hidden Line Visualization** — Visible lines in black, hidden lines in grey.
- **Dynamic Position & Rotation** — Shapes positioned based on user parameters (distances from HP/VP, rotation angles).
- **Automatic Plane Sizing** — HP and VP resize based on shape dimensions.
- **No Shadows** — Clean diagram-like rendering for clarity.
- **Web-Ready** — Built with Unity WebGL for browser viewing.

---

## 🎯 Goals of the Project

The project is designed to **aid Engineering Graphics learning** by allowing students to:
1. View 3D models of solids.
2. Understand how these shapes project onto reference planes.
3. Visualize hidden and visible edges clearly.
4. Experiment with different distances and inclinations.

---

## 🛠️ Technologies Used

- **Unity 2022+** (WebGL build target)
- **C#** for procedural shape generation & projection logic
- **LineRenderer API** for drawing edges and projections
- **GitHub Pages** for hosting the WebGL build

---

## 🚀 How to Run Locally

1. **Clone the Repository**
   ```bash
   git clone https://github.com/KenwayBlue7/engineering-graphics-viewer.git
   cd engineering-graphics-viewer
   ```

2. **Open in Unity**
   - Open Unity Hub
   - Click **Add Project**
   - Select this project folder

3. **Switch to WebGL Build Target**
   - File → Build Settings → Select **WebGL**
   - Click **Switch Platform**

4. **Build the Project**
   - Click **Build and Run**
   - Open `index.html` in a browser

---

## 🌍 View Online

The latest build is hosted via **GitHub Pages** here:  
🔗 [Engineering Graphics Viewer](https://kenwayblue7.github.io/engineering-graphics-viewer/)

---

## 📂 Project Structure

```
Assets/
 ├── Scripts/
 │   ├── Visualizer.cs        # Generates shapes & projections
 │   ├── ShapeData.cs         # Stores shape parameters
 │   ├── MeshAnalyzer.cs      # Determines faces, edges & hidden lines
 │   └── ProjectionHelper.cs  # Sets up HP & VP views
 ├── Materials/
 │   ├── SolidMaterial.mat
 │   └── LineMaterial.mat
 └── Scenes/
     └── MainScene.unity
```

---

## 📜 How It Works

1. **Shape Generation**  
   - User parameters (base length, height, distance from planes, inclination angles) are read from `ShapeData`.
   - Shape is procedurally created and positioned in 3D space.

2. **Projection Logic**  
   - Mesh vertices are projected onto HP (X-Z plane) and VP (X-Y plane).
   - Outlines are drawn using `LineRenderer`.

3. **Hidden Line Detection**  
   - Top face & front face are identified using normals.
   - Vertices under these faces are marked hidden using geometric checks.
   - Hidden edges drawn in **grey**, visible edges in **black**.

---

## 📌 Future Improvements

- Add more shapes (cone, prism, frustum).
- Allow direct parameter input from the web page (HTML → Unity via WebGL).
- Improve hidden line detection for inclined shapes.
- Add interactive rotation & zoom controls in the browser.

---

## 📄 License

This project is released under the **MIT License** — free to use and modify with attribution.

---

## 👤 Author

**KenwayBlue7**  
📧 Contact: _[Your Email Here]_  
🔗 GitHub: [KenwayBlue7](https://github.com/KenwayBlue7)

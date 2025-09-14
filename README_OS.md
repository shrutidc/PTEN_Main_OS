# Smart Pad Layout Optimizer (Implementation)

This is our hackathon implementation of the **Smart Pad Layout Optimizer**, a single-page web application that takes the challenge spec and turns it into a working demo.  

The app allows engineers to **upload drone site imagery**, place and arrange frac equipment interactively on a canvas, check for collisions/zones, and even run **AI-powered optimization** using Google’s Gemini API.

---

## 🎯 Core Features
- **Upload Site Plan**
  - Supports JPEG/PNG images
  - Optional TIFF world file (.wld, .tfw, .jgw, .ftw) for auto-scaling
- **Equipment Library**
  - Frac pumps, blenders, sand equipment, datavan, wireline, manifolds, chemical skids
  - Drag-and-drop placement with correct dimensions
- **Collision Detection**
  - Automatic detection of overlaps and safety clearance violations
- **Zones**
  - Create exclusion zones (safety, buffer, restricted areas)
  - Delete zones or unlock equipment groups
- **AI Optimization**
  - Uses **Gemini API** to generate suggested equipment layouts based on uploaded site imagery
- **Export**
  - Export as **CSV** (with coordinates, sizes, rotations)
  - Export as **PDF** (with a visual layout + equipment index)

---

## 🛠️ Built With
- **HTML5 / CSS3 / TailwindCSS**
- **JavaScript (vanilla)** for all logic
- **Canvas API** for rendering, zoom, rotation, and equipment placement
- **jsPDF + jsPDF-autotable** for PDF export
- **CSV export** via in-browser JavaScript
- **Google Gemini API** for AI-assisted layout optimization

---

## 📂 Project Structure
Main_File/
│── index.html # main application (open directly in browser)
│── ... # supporting JS & style inlined
drone_scans/ # sample site imagery (plan / actual / planning)
equipment_specifications.json # equipment dimensions & metadata

---

## ⚙️ Getting Started

### Run Locally
1. Clone the repo:
   ```bash
   git clone https://github.com/shrutidc/PTEN_Main_OS.git
   cd PTEN_Main_OS/Main_File
2. Open index.html in your browser.
3. Enable AI Optimization
- Inside index.html, find the apiKey variable in the script section:
    const apiKey = "YOUR_API_KEY_HERE";
- Replace it with your Google Gemini API key.
- Now the AI Optimize Layout button will work.

---

  📖 Usage

Upload a site plan (from /drone_scans or your own).

(Optional) Upload a world file to auto-set scale.

Choose equipment from the library and create groups.

Place equipment onto the canvas — rotate, move, or lock groups.

Add safety exclusion zones if needed.

Use AI Optimize Layout to let Gemini suggest a layout.

Export as CSV or PDF for field use.

---
🔮 Future Work

3D visualization of layouts

Smarter AI with reinforcement learning for optimization

Planned vs. actual comparison using follow-up drone scans 
---
🙌 Credits

Implementation in HackWesTX @ Texas Tech

Challenge Spec: Patterson-UTI

API : Gemini API, Canvas API

---

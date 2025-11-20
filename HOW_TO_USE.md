# 📖 How to Use - Simple Guide

Quick reference for using the Face Embeddings Visualizer.

---

## 🚀 **Quick Start (3 Steps)**

### **Step 1: Start Server**
```bash
npm run serve
```

### **Step 2: Open in Browser**
```
http://localhost:8080/example/face-embeddings-demo.html
```

### **Step 3: Upload & Visualize**
1. Drag your JSON file to the upload area
2. Watch animated progress ⏳ → ✅
3. Click "▶️ Run t-SNE"
4. Explore your face clusters!

---

## 📁 **Your Data Format**

```json
{
  "embeddings": [
    [0.234, -0.567, 0.891, ...],
    [0.187, -0.523, 0.845, ...],
    ...
  ],
  "labels": ["Alice", "Bob", ...],
  "images": ["base64...", ...]
}
```

**See:** `example/data-format-example.json`

---

## 🎮 **Controls**

### **Navigation:**
- **Scroll** = Zoom
- **Click & Drag** = Pan
- **Arrow Keys** = Move around
- **Hover face** = Show label & preview
- **Click face** = See details

### **Buttons:**
- **+** = Zoom in
- **−** = Zoom out
- **⟲** = Reset
- **📐 Fit to View** = Auto-optimize
- **🎯 Center** = Recenter

---

## ✨ **Key Features**

### **Smart Labels** 
- Auto-hides when 30+ faces
- Shows on hover
- Always shows selected face
- Keeps view clean

### **Animated Upload**
- Real-time progress bar
- Visual feedback
- Success confirmation
- Error handling

### **Large Canvas**
- 1400 x 900 pixels
- 57% more space
- Professional quality
- Clear visualization

---

## 💡 **Tips**

### **For Many Faces (100+):**
1. Leave Smart Labels ON
2. Hover to see names
3. Zoom in to see details
4. Use arrow keys to navigate

### **For Few Faces (<30):**
1. Smart Labels shows all
2. Or turn Smart Labels OFF
3. All names always visible

### **Best Results:**
1. Run t-SNE 2-3 times
2. Pick clearest layout
3. Use Fit to View
4. Export when satisfied

---

## 🐛 **Troubleshooting**

**Can't see labels?**
→ Hover over faces or zoom in

**Upload not working?**
→ Check JSON format matches example

**View looks wrong?**
→ Click "📐 Fit to View"

**Lost position?**
→ Press "C" or click "🎯 Center"

---

## 📚 **More Help**

- **Complete Guide:** `FINAL_FEATURES.md`
- **Navigation:** `ZOOM_AND_VIEW_CONTROLS.md`
- **Script Help:** `FOR_YOUR_SCRIPT.md`
- **Examples:** `example/data-format-example.json`

---

**That's it! You're ready to visualize your face embeddings!** 🎉


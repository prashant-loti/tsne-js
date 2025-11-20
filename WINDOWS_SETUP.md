# Running t-SNE Demo on Windows 11

This guide will help you run the t-SNE demo locally on Windows 11.

## Prerequisites

You need Node.js installed. If you don't have it:
- Download from: https://nodejs.org/
- Install the LTS (Long Term Support) version
- Verify installation by opening PowerShell and running: `node --version`

## Quick Start (Using Pre-built Files)

The project already has built files, so you can run the demo immediately:

### Step 1: Install Dependencies (First Time Only)

Open PowerShell in the project directory and run:

```powershell
npm install
```

Note: If you see warnings about deprecated packages, you can ignore them - they don't affect the demo.

### Step 2: Start the Local Server

```powershell
npm run serve
```

You should see:

```
🚀 t-SNE Demo Server running!

📊 Open your browser to: http://localhost:8080/example/index.html

   Press Ctrl+C to stop the server
```

### Step 3: Open in Browser

Open your web browser and navigate to:

```
http://localhost:8080/example/index.html
```

You should see the interactive t-SNE demo with MNIST digit visualization!

### Step 4: Try the Demo

1. Adjust parameters using the sliders:
   - **# Samples**: How many data points to visualize (100-1000)
   - **Perplexity**: Balance between local and global structure (5-50)
   - **Early Exaggeration**: Cluster spacing (1.1-10.0)
   - **Learning Rate**: Optimization speed (1-1000)
   - **Max Iterations**: How long to run (100-500)
   - **Distance Metric**: How to measure similarity

2. Click the **Run** button

3. Watch as the algorithm arranges the digit images based on their similarity!

### To Stop the Server

Press `Ctrl+C` in the PowerShell window.

## Optional: Rebuilding from Source

If you want to modify the source code and rebuild (now Windows-compatible):

```powershell
# Build everything
npm run build

# Or build just the browser version
npm run build-browser

# Or build just the Node.js version
npm run build-node
```

## Next Steps: Using Your Face Embeddings

The demo currently uses MNIST digits, but you can adapt it for your face embeddings:

1. Your face embeddings should be an array of arrays, where each inner array is a face vector
2. Example format:
   ```javascript
   [
     [0.123, 0.456, 0.789, ...],  // Face 1 embedding
     [0.234, 0.567, 0.890, ...],  // Face 2 embedding
     // ... more faces
   ]
   ```
3. The t-SNE algorithm will reduce these high-dimensional vectors to 2D points for visualization
4. Similar faces will appear close together, making groups visible!

## Troubleshooting

### "Cannot find module" error
Run `npm install` first to install all dependencies.

### Port 8080 already in use
Another application is using port 8080. Either:
- Stop the other application
- Edit `server.js` and change `const PORT = 8080;` to a different number (e.g., 3000)

### Browser shows "Cannot GET /"
Make sure to navigate to: `http://localhost:8080/example/index.html` (not just `http://localhost:8080`)

### The demo is slow or freezes
The computation is CPU-intensive. Try:
- Use fewer samples (100-300 instead of 1000)
- Reduce max iterations (100 instead of 500)
- Wait patiently - it will complete!

## What's Next?

You're now ready to:
1. Explore the demo and understand how t-SNE visualizes high-dimensional data
2. Prepare your face embedding data
3. Modify the demo to visualize your faces instead of digits
4. Adjust parameters to get the best visualization for your data

Happy visualizing! 🎉


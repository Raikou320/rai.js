# 📘 Rai.js Module Documentation

This module provides useful functions to work with an HTML5 canvas. It allows you to create a canvas, draw on it, manage colors, display images, and clear the canvas.

---

## ⚙️ General Overview

The `Rai.js` module is wrapped in an IIFE (Immediately Invoked Function Expression) and is accessible via the global `rai` object in your app.  
It exposes several methods to interact with an HTML5 canvas.

---

## 🧩 Available Methods

### `createCanvas(width, height)`  
Creates a canvas with the given dimensions and adds it to the page.

**Parameters:**  
- `width`: Width of the canvas (in pixels)  
- `height`: Height of the canvas (in pixels)

**Example:**  
createCanvas(800, 600);

---

### `background(r, g, b)`  
Changes the background color of the canvas.

**Parameters:**  
- `r`: Red component (0–255)  
- `g`: Green component (0–255). If not provided, `r` will be used  
- `b`: Blue component (0–255). If not provided, `r` will be used

**Example:**  
background(255, 0, 0); // Red background

---

### `fill(r, g, b)`  
Sets the fill color for future shapes.

**Parameters:**  
- `r`: Red component (0–255)  
- `g`: Green component (0–255). If not provided, `r` will be used  
- `b`: Blue component (0–255). If not provided, `r` will be used

**Example:**  
fill(0, 255, 0); // Green fill

---

### `rect(x, y, w, h)`  
Draws a filled rectangle using the current fill color.

**Parameters:**  
- `x`: X position (top-left corner)  
- `y`: Y position (top-left corner)  
- `w`: Width of the rectangle  
- `h`: Height of the rectangle

**Example:**  
rect(50, 50, 100, 100); // Red square at (50, 50)

---

### `image(src, x, y, width, height)`  
Displays an image at a specific position and size.

**Parameters:**  
- `src`: Image file path  
- `x`: X position  
- `y`: Y position  
- `width`: Width of the image  
- `height`: Height of the image

**Example:**  
image('image.png', 100, 100, 50, 50); // Draws image at (100, 100)

---

## 🧪 Usage Example

```html
createCanvas(800, 600)  
background(0, 0, 255) // Blue background  
fill(255, 0, 0) // Red fill  
rect(50, 50, 100, 100) // Red square  
image('sprite.png', 200, 200, 50, 50) // Display image
```

---

## 💡 Notes

- Images are loaded asynchronously using `onload` to ensure they are drawn after being fully loaded.  
- The canvas and its context (`ctx`) are stored in global variables accessible via `window`.

---

## 📖 Author

Created by **Raikou 320**  
GitHub: [https://github.com/Raikou320](https://github.com/Raikou320)

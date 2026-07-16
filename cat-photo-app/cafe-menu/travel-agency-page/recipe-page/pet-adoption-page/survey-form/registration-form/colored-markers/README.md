# CSS Color Markers

A simple, clean project that demonstrates how to create “marker” elements using only HTML and CSS. The focus is on gradients, shadows, inline-block layout, and mixing color models (`rgb`, hex, and `hsl`).

---

## Project Overview
This project styles three horizontal markers (red, green, blue) using:
- Linear gradients for depth and realistic color transitions
- Box shadows to create subtle glow and separation from the background
- `inline-block` to align the cap and sleeve in a single row
- Mixed color models (`rgb`, hex, `hsl`, and `rgba/hsla`) to practice color precision and opacity

---

## Tech Stack
- **HTML5** for structure  
- **CSS3** for visual design (gradients, shadows, layout)

---

## File Structure


├── index.html
└── styles.css

---

## How to Run
1. Download or clone the repository.
2. Open `index.html` in any modern browser.
3. You should see three color markers (Red, Green, Blue).

---

## Implementation Notes
- Each marker is a `.marker` block with two inline children: `.cap` and `.sleeve`.
- Gradients are applied to the `.marker` itself.
- The `.sleeve` uses a semi-transparent background and a `double` left border to suggest a printed label.
- Box shadows add depth; values are tuned per color to keep a consistent glow.

---

## Accessibility
- The layout is visual-only; no interactive controls.
- Headings are used meaningfully (`<h1>`).
- Consider adding more semantic structure or captions if you expand the project.

---

## Customization
- **Add a new color:** duplicate a `.marker` block and create a new color class with your gradient and shadow.
- **Change sizes:** tweak `.marker`, `.cap`, and `.sleeve` widths/heights in `styles.css`.
- **Glow intensity:** adjust the final alpha channel in `box-shadow` colors.

---

## What I Did — Notes (GitHub Study Format)

**Step 1 — Structure the Markers**  
- ***What I did***: Built a container with three `.marker` elements. Each marker has a `.cap` and a `.sleeve`.  
- ***Why this matters***: Separating cap and sleeve allows horizontal alignment and independent styling (e.g., sleeve border).  
- ***Before***: A single block element per marker without distinct parts.  
- ***After***: Two inline parts (`.cap`, `.sleeve`) per marker for better control of layout and visuals.

**Step 2 — Align Cap and Sleeve Horizontally**  
- ***What I did***: Set `.cap, .sleeve { display: inline-block; }` so they sit on the same line.  
- ***Why this matters***: Avoids default block stacking and mimics a real marker’s continuous body.  
- ***Before***: Cap and sleeve stacked vertically due to default `display: block`.  
- ***After***: Cap and sleeve align in one row; marker looks continuous.

**Step 3 — Add Linear Gradients for Depth**  
- ***What I did***: Applied multi-stop `linear-gradient(...)` backgrounds to `.marker.red`, `.marker.green`, `.marker.blue`.  
- ***Why this matters***: Gradients simulate cylindrical shading and make flat blocks feel 3D.  
- ***Before***: Flat, single-color fills with no depth.  
- ***After***: Smooth transitions that read as rounded surfaces.

**Step 4 — Use Transparent Sleeve and Label Stripe**  
- ***What I did***: Gave `.sleeve` a semi-transparent white `rgba(...)` background and a `border-left: 10px double rgba(0,0,0,.75)`.  
- ***Why this matters***: Creates the illusion of a plastic sleeve and a printed label seam.  
- ***Before***: Solid sleeve with no label detail.  
- ***After***: Subtle translucency and a distinct label edge improve realism.

**Step 5 — Add Box Shadows for Glow/Depth**  
- ***What I did***: Tuned `box-shadow` per color (matching hue and opacity).  
- ***Why this matters***: Shadows separate markers from the background and add a soft glow that matches the ink color.  
- ***Before***: Markers blended into the container; looked flat.  
- ***After***: Clear separation and color-consistent glow enhance polish.

**Step 6 — Mix Color Models Intentionally**  
- ***What I did***: Combined `rgb`, hex, and `hsl` across the markers; used `rgba/hsla` for transparency.  
- ***Why this matters***: Shows fluency with different color systems; `hsl` is great for hue/saturation tweaks, `rgba` for opacity.  
- ***Before***: One color model limits control and learning opportunities.  
- ***After***: Flexible, more predictable color adjustments.

---

# 🎨 CSS Color Markers

## 📄 Project Overview
This project demonstrates CSS color gradients, shadows, and layout by creating colorful markers using HTML & CSS.

---

# 🎨 CSS Color Markers

## 📄 Project Overview
This project demonstrates CSS color gradients, shadows, and layout by creating colorful markers using HTML & CSS.  
It’s part of the **Responsive Web Design Certification** on freeCodeCamp.org.

```css

[index.html]

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Colored Markers</title>
    <link rel="stylesheet" href="styles.css">
  </head>
  <body>
    <h1>CSS Color Markers</h1>
    <div class="container">
      <div class="marker red">
        <div class="cap"></div>
        <div class="sleeve"></div>
      </div>
      <div class="marker green">
        <div class="cap"></div>
        <div class="sleeve"></div>
      </div>
      <div class="marker blue">
        <div class="cap"></div>
        <div class="sleeve"></div>
      </div>
    </div>
  </body>
</html>

[styles.css]

h1 {
  text-align: center;
}

.container {
  background-color: rgb(255, 255, 255);
  padding: 10px 0;
}

.marker {
  width: 200px;
  height: 25px;
  margin: 10px auto;
}

.cap {
  width: 60px;
  height: 25px;
}

.sleeve {
  width: 110px;
  height: 25px;
  background-color: rgba(255, 255, 255, 0.5);
  border-left: 10px double rgba(0, 0, 0, 0.75);
}

.cap, .sleeve {
  display: inline-block;
}

.red {
  background: linear-gradient(rgb(122, 74, 14), rgb(245, 62, 113), rgb(162, 27, 27));
  box-shadow: 0 0 20px 0 rgba(83, 14, 14, 0.8);
}

.green {
  background: linear-gradient(#55680D, #71F53E, #116C31);
  box-shadow: 0 0 20px 0 #3B7E20CC;
}

.blue {
  background: linear-gradient(hsl(186, 76%, 16%), hsl(223, 90%, 60%), hsl(240, 56%, 42%));
  box-shadow: 0 0 20px 0 hsla(223,59%,31%,.8);
}

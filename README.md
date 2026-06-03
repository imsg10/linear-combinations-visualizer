# Linear Combinations Visualizer

## Overview

This is a single-file HTML tool that lets you manipulate the scalars **c** and **d** in the expression **cv + dw** and immediately see the result on a coordinate grid. Every change to a slider redraws the vectors, the parallelogram construction, and the live formula — so the connection between the algebra and the geometry stays visible at all times.

Fixed base vectors:

```
v = [1, 1]      w = [2, 3]
```

The combination **cv + dw** is shown as a green arrow whose tip updates in real time as you drag.

---

## Features

### Interactive canvas
- Coordinate grid with labelled axes
- **Red arrow** — scaled vector cv
- **Blue arrow** — scaled vector dw
- **Green arrow** — the resulting combination cv + dw
- **Dashed parallelogram** — shows the tip-to-tail construction geometrically

### Scalar sliders
| Slider | Range | Controls |
|--------|-------|---------|
| c | −3 to 3 | Scales **v** |
| d | −3 to 3 | Scales **w** |

### Three information tabs

**Result** — live formula display updating as you drag:
```
c·v + d·w = 2·[1,1] + 1·[2,3] = [4, 5]
```

**Intuition** — explains the tip-to-tail construction in plain language, linking the dashed arrows on the canvas to the geometric meaning of addition.

**Span** — explains what happens as c and d range over *all* real numbers, with a **"Show span sweep"** button that animates random combinations to visually demonstrate that two independent vectors fill the entire 2D plane.

---

## How to Use

No installation, no dependencies, no build step.

```bash
# Just open the file in any browser
open linear_combinations.html
```

Or drag the file into a browser window. Everything runs locally — no network requests required (fonts load from Google Fonts if online, and fall back to Georgia if not).

---

## What It Teaches

| Concept | How it's shown |
|---------|---------------|
| Linear combination **cv + dw** | Sliders control c and d; result arrow updates live |
| Scalar multiplication | Each vector scales smoothly as its slider moves |
| Vector addition (parallelogram rule) | Dashed construction lines form the parallelogram |
| Tip-to-tail addition | cv is visibly placed at the tip of dw |
| Span of two vectors | Sweep animation shows combinations filling the plane |
| Negative scalars | Sliders go to −3; arrows reverse direction |

---

## File Structure

```
linear_combinations.html   ← entire app: HTML + CSS + JS in one file
README.md
```

The JavaScript uses only the **Canvas 2D API** — no frameworks, no external libraries beyond the optional Google Fonts import.

Key rendering functions:

```
toCanvas(x, y)          — converts math coordinates to canvas pixels
drawArrow(...)          — draws a vector arrow with arrowhead
draw()                  — full redraw on every slider change
```

---

## Intended Audience

Students working through an introductory linear algebra course The tool is designed as a companion to pencil-and-paper work, not a replacement for it — the goal is to let you test your geometric intuitions quickly.

---

## Browser Compatibility

Works in any modern browser that supports the Canvas 2D API.

| Browser | Supported |
|---------|-----------|
| Chrome / Edge | ✓ |
| Firefox | ✓ |
| Safari (iOS + macOS) | ✓ |
| Samsung Internet | ✓ |

---

## License

MIT — free to use, adapt, and share.

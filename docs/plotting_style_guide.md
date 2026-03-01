# Plotting Style Guide

This document defines the plotting principles that must be followed in this repository.

These are guidelines, not rigid laws. However, they should be respected unless there is a strong technical reason not to.

---

## 1. Clarity and Context

- Axis labels must be descriptive.
- Units must be included when applicable.
- Titles should be concise and informative when needed.
- The plot must communicate a clear message.
- Avoid unnecessary clutter.
- Do not include decorative elements that do not serve the data.

---

## 2. Font and Style Consistency

- Use readable serif fonts for digital and publication outputs. Computer Modern is the preference.
- Maintain consistent font sizes across:
  - Titles
  - Axis labels
  - Tick labels
  - Legends
- The Y-axis label must be written horizontally (rotation = 0).
  - It must not follow the vertical orientation of the axis.
  - Both X and Y labels must be horizontally readable.

---

## 3. Use of Color

- Use perceptually uniform, colorblind-friendly colormaps.
  - Examples: viridis, cmocean, plasma, ColorBrewer palettes.
- Do NOT use rainbow or jet colormaps.
- Use a limited number of colors.
- Maintain strong contrast.
- Prioritize accessibility (colorblind-safe design).

---

## 4. Axis Scaling and Limits

- Use symmetric axis limits when appropriate.
- Avoid misleading truncation.
- Use `axis equal` for geometric or geographic data to preserve proportions.
- Ensure scaling does not distort interpretation.

---

## 5. Line Styles, Thickness, and Layout

- Use sufficiently thick lines for visibility.
- Use clear marker styles when needed.
- Differentiate datasets with distinct line styles if necessary.
- Use grids or bounding boxes only when they improve readability.
- Maintain consistent plot sizing.

---

## 6. Consistent Colormaps and Scales

- When comparing multiple datasets:
  - Use consistent colormaps.
  - Use consistent axis limits.
- Align zero or midpoint values across related plots.

---

## 7. Export Quality

- Save figures in high resolution:
  - PNG at 300+ DPI for raster.
  - SVG/EPS for vector.
- Prefer editable formats when possible.
- Ensure export quality matches publication standards.

---

## HARD RULE

- DO NOT annotate plots under any circumstances.
- No arrows, text labels, highlights, or callouts.
- Annotations are only allowed if explicitly requested in chat.
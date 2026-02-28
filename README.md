# Creating Scientific Plots in Python

This repository contains the **Knowvember 2025** notebook *Creating Scientific Plots in Python*, focused on producing high-quality, readable, and consistent scientific figures using **Python** and **Matplotlib**.

All examples are functional and ready to run. Some blocks are commented for teaching purposes.

---

## Overview

The notebook walks through a full plotting workflow:

0. Environment setup (libraries, imports, datasets)  
1. Start with a basic plot  
2. Titles, axis labels, and units  
3. Fonts and text readability  
4. Axis limits and focus  
5. Figure size and layout  
6. Aspect ratio for spatial / geographic data  
7. Colour scales and colormaps  
8. Colorblind- and grayscale-friendly maps  
9. Consistency across plots  
10. Exporting high-quality figures  

The examples use ERA5 climate data (temperature and rainfall over Scandinavia) and include helper functions for consistent map styling, grayscale colormaps, and color-vision-deficiency simulation.

---

## Quick Start

Run the notebook directly on [Google Colab](https://colab.research.google.com/github/borgesf/scientificPlotsPython_knowvember25/blob/main/2025_11_scientificPlots_Knowvember25_codeOnly.ipynb) or locally with:

```bash
pip install numpy matplotlib pandas geopandas xarray requests cmocean[plots]
```

Then execute the notebook cells in order.  
Datasets and GeoJSON boundaries download automatically.

---

## Binder Launch

You can also open and run this notebook interactively in your browser via **Binder** (no installation required):

[![Launch Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/borgesf/scientificPlotsPython_knowvember25/HEAD)

---

## Helper Functions

- `style_scandinavia_map()` – consistent map styling (axes, title, colorbar, optional markers)  
- `build_grayscale_cmap()` – convert any colormap to a perceptual grayscale (CAM02-UCS J′)  
- `simulate_partial_color_blind()` – partial red-green deficiency (Machado 2009)  
- `simulate_full_color_blind()` – full green-cone loss (Brettel 1997)

---

## Example Topics

- Controlling figure size, fonts, and labels  
- Choosing perceptually uniform colormaps (`cmocean`)  
- Ensuring accessibility (color-blind-friendly, grayscale-friendly)  
- Exporting publication-ready figures (PNG 400 DPI / SVG)  

---

## References

- [nicePythonPlots (GitHub)](https://github.com/borgesf/nicePythonPlots)  
- [Medium: How to Create Professional and Readable Scientific Plots in Python](https://medium.com/@FilipeBorgesBR/how-to-create-professional-and-readable-scientific-plots-in-python-72f1defed8b3)  
- [Matplotlib colormaps](https://matplotlib.org/stable/users/explain/colors/colormaps.html)  
- [cmocean colormaps](https://matplotlib.org/cmocean/)  
- [Copernicus ERA5 monthly means dataset](https://cds.climate.copernicus.eu/datasets/reanalysis-era5-single-levels-monthly-means?tab=download#variable)  
- [Coblis color-blindness simulator](https://www.color-blindness.com/coblis-color-blindness-simulator/)

---

## Key Papers

- **Machado G. M., Oliveira M. M., & Fernandes L. A. F. (2009)**  
  *A Physiologically-based Model for Simulation of Color Vision Deficiency.*  
  *IEEE Trans. Visualization and Computer Graphics*, 15(6), 1291-1298.  
  [https://doi.org/10.1109/TVCG.2009.113](https://doi.org/10.1109/TVCG.2009.113)

- **Brettel H., Viénot F., & Mollon J. D. (1997)**  
  *Computerized Simulation of Colour Appearance for Dichromats.*  
  *Journal of the Optical Society of America A*, 14(10), 2647-2655.  
  [https://doi.org/10.1364/JOSAA.14.002647](https://doi.org/10.1364/JOSAA.14.002647)

- **Li C. et al. (2017)**  
  *Comprehensive Colour Solutions: CAM16, CAT16, and CAM16-UCS.*  
  *Color Research & Application*, 42(6), 703-718.  
  [https://doi.org/10.1002/col.22131](https://doi.org/10.1002/col.22131)

---

## License

MIT License — use, modify, and share freely with proper attribution.

---

## Citation

If you use this material, please cite:

**Filipe Borges (2025).** *Creating Scientific Plots in Python — Knowvember 2025 Workshop.*  
Available at: [https://github.com/borgesf/scientificPlotsPython_knowvember25](https://github.com/borgesf/scientificPlotsPython_knowvember25)

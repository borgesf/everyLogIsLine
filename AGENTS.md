# Agent Instructions

Before generating any plot, you must:

1. Read `docs/plotting_style_guide.md`.
2. Use the style file `style/myStyle.mplstyle`.
3. Ensure all plots comply with the rules defined in the guide.
4. Force Y-axis labels to be horizontal. For example, use

def enforce_horizontal_ylabel(ax):
    ax.yaxis.label.set_rotation(0)
    ax.yaxis.label.set_horizontalalignment('right')
    ax.yaxis.set_label_coords(-0.08, 0.5)

Mandatory constraints:

- Use serif fonts.
- Maintain consistent font sizes.
- Y-axis labels must be horizontal (rotation = 0).
- No rainbow/jet colormaps.
- Use perceptually uniform, colorblind-safe palettes.
- Include axis labels and units when applicable.
- Use sufficiently thick lines.
- Keep export resolution at 300+ DPI.
- Maintain consistent scales across comparable plots.

STRICT RULE:

- DO NOT annotate plots under any circumstances.
  - No arrows
  - No text overlays
  - No highlight markers
  - No callouts
  - No inline labels

Annotations are allowed only if explicitly requested in chat.


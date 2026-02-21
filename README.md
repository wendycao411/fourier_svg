# SVG Fourier Epicycles

Turn an SVG drawing into a Fourier-series epicycle animation using Python and Jupyter.

This project:
- loads an SVG path,
- samples points along the path,
- computes Fourier coefficients,
- reconstructs the curve,
- animates epicycles,
- saves a GIF output.

## Demo

![Epicycle demo](epicycles.gif)

Demo source files in this repo:
- `test_svg.ai` (Adobe Illustrator source)
- `test_svg.svg` (exported SVG)
- `epicycles.gif` (generated animation)

## Quick Start

1. Create and activate a virtual environment (recommended):

```bash
python -m venv .venv
source .venv/bin/activate
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Open the notebook:

```bash
jupyter notebook fourier_svg.ipynb
```

4. Run all cells.

5. In the test block, set your SVG path (for example `test_svg.svg`) and run the animation cell.

## How To Create Your Own SVG (Adobe Illustrator)

1. Draw your shape in Adobe Illustrator.
2. Export as SVG.
   - `File -> Export -> Export As... -> SVG`.
3. Place the SVG file in this project folder.
4. Update the notebook SVG path variable to your file name.
5. Re-run sampling, Fourier, and animation cells.

## Notes

- SVG and plot coordinate systems are different; the notebook flips Y so the drawing is not vertically reflected.
- GIF size/speed are controlled in `animate_epicycles(...)` via `frames` and `gif_seconds`.

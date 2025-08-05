# PyDS

**PyDS** (Python DataSheet) class provides a way to parse SVG files containing line plots and extract path data, transforming it into coordinates. 
It is mainly used for tracing the datasheet curves and converting them in ready-to-use data arrays

---

## 🚀 Features

- Load and parse SVG file containting datasheet curves
- Identify and extract plot paths.
- Scale and transform coordinates to match plot dimensions.
- Visualize individual or all plots.
- Export coordinate values.

---

## 📦 Installation

PyDS relies on the following Python libraries:

- `svgpathtools` - not available in default python installation. Use pip install svgpathtools
- `numpy` - available in default python installation
- `matplotlib` - available in default python installation
- `xml` - available in default python installation

Install the required packages:

```bash
pip install svgpathtools
```
---
## 🧰 Usage
### Initialization
```bash
from pyds import PyDS
svg_plot = PyDS(filename="graph.svg", Npoints=100, x=100, y=0, width=100, height=80)
```
-`filename` - default positional argument (should always be used)
-`NPoints` - default positional argument (should always be used)
-`x` - start x position of the grid box. Keyword argument (can be omitted)
-`y` - start y position of the grid box. Keyword argument (can be omitted)
-`width` - width of the grid box. Keyword argument (can be omitted)
-`height` - height of the grid box. Keyword argument (can be omitted)

### Plot All Paths
```bash
svg_plot.plot_all(labels=["Line A", "Line B"])
```

### Access Path Values
```bash
data = svg_plot.values(0)
print(data['x'], data['y'])
```
---
## 🔗 Dependencies
-`svgpathtools`
-`matplotlib`
-`numpy`
-`xml.etree.ElementTree`

## 📝 License
MIT License. See LICENSE file for details.
## ✍️ Author
Developed by Dr. Anatolii Tcai

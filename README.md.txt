# Sayedpur Land Indices (NDVI, MNDWI, BSI, NDBI)

Google Earth Engine script to compute **four land cover indices** over **Sayedpur** using **Sentinel-2** (2024).

---

## Features

- NDVI (Vegetation)
- MNDWI (Water)
- BSI (Bare Soil)
- NDBI (Built-up)
- RGB composite
- Optional split-panel view
- Clean, modular code

---

## Requirements

1. [Google Earth Engine](https://code.earthengine.google.com)
2. Upload your shapefile as **`sayedpur`** in **Assets**

---

## How to Run

1. Open: [https://code.earthengine.google.com](https://code.earthengine.google.com)
2. Paste `src/sayedpur_indices.js`
3. Ensure `sayedpur` is in your **Assets**
4. Run

---

## Output

- **Map**: 4 individual layers + RGB composite
- **Optional**: 4-panel synchronized view
- **Console**: Image info

---

## Export (Add this to script)

```javascript
Export.image.toDrive({
  image: compositeImage,
  description: 'Sayedpur_Indices_2024',
  folder: 'GEE_Exports',
  region: roi,
  scale: 10,
  maxPixels: 1e9
});
# 🌿 Vegetation Insights

Interactive Earth observation dashboard visualizing vegetation health and land cover across Goa, India, using three satellite remote-sensing datasets — **MODIS NDVI**, **Landsat 9 FCC**, and **Sentinel-2 FCC**.

![status](https://img.shields.io/badge/status-active-brightgreen)
![type](https://img.shields.io/badge/type-single--page%20site-blue)
![license](https://img.shields.io/badge/license-MIT-lightgrey)

---

## 📖 Overview

Vegetation Insights presents interactive visualizations of vegetation products for the Goa talukas of **Mormugao**, **Tiswadi**, and **Bardez** (the Region of Interest, or ROI). Each dataset is rendered through an embedded [Google Earth Engine](https://earthengine.google.com/) app and paired with:

- Satellite/agency metadata and spatial & temporal resolution specs
- A plain-language interpretation of what the imagery shows
- A side-by-side comparison of all three sensors

The goal is to make Earth observation data more approachable — showing how the *same* land area looks different depending on the sensor's resolution, revisit frequency, and band composition, and why that matters for applications like drought monitoring, precision agriculture, and land-use change detection.

## 🛰️ Datasets

| Dataset | Satellite | Agency | Resolution | Revisit | Best For |
|---|---|---|---|---|---|
| MODIS NDVI | Terra/Aqua | NASA | 250 m | Daily | Regional trends, drought & crop monitoring |
| Landsat 9 FCC | Landsat 9 | NASA / USGS | 30 m | 16 days | Long-term change, land cover |
| Sentinel-2 FCC | Sentinel-2 A/B | ESA / Copernicus | 10 m | 5 days | Field-level detail, precision agriculture |

## ✨ Features

- 🗺️ Embedded, interactive Earth Engine maps for all three datasets, each with a fullscreen expand toggle
- 🪟 Glassmorphism UI with a fixed, full-bleed background photograph and blurred glass panels
- 📊 Dataset comparison table (resolution, revisit time, ideal use case)
- 🎬 Animated intro splash, scroll-reveal transitions, ambient particle canvas, and a magnetic back-to-top button
- 📱 Fully responsive layout (desktop, tablet, mobile) with dynamic-viewport-height handling
- ⏳ Loading skeletons for embedded maps and a floating "back to top" button that appears on scroll
- ♿ Respects `prefers-reduced-motion`; keyboard-accessible nav and controls
- 🧱 Single self-contained `index.html` — no build step, no dependencies

## 🧰 Tech Stack

- **HTML5 / CSS3** — CSS custom properties for theming, CSS Grid & Flexbox for layout, `backdrop-filter` for glassmorphism
- **Vanilla JavaScript** — `IntersectionObserver` for scroll reveals, Canvas API for the ambient particle background, Fullscreen API for map expansion
- **Google Earth Engine** — hosted map apps embedded via `<iframe>`
- **Google Fonts** — Space Grotesk (headings) + Inter (body)

No frameworks, bundlers, or package managers required.

## 🚀 Getting Started

This is a static, single-file website — there's no build process.

```bash
git clone https://github.com/<your-username>/vegetation-insights.git
cd vegetation-insights
```

Then simply open `index.html` in a browser, or serve it locally:

```bash
# Python
python3 -m http.server 8000

# Node
npx serve .
```

Visit `http://localhost:8000` in your browser.

## 📁 Project Structure

```
vegetation-insights/
├── index.html      # Entire site — markup, styles, and scripts in one file
└── README.md
```

## 🎨 Customization

- **Background image**: replace the base64-encoded photo in the `.bg-photo` CSS rule, or swap it for a `url('path/to/image.jpg')` reference.
- **Color theme**: all colors are defined as CSS custom properties in `:root` (`--emerald`, `--cyan`, `--ink`, `--glass`, etc.) — update them there to retheme the whole site.
- **Map sources**: update the `src` attributes on the three `<iframe>` elements to point to your own Earth Engine apps.
- **Region of interest**: update the hero stats, dataset notes, and interpretation copy to reflect your own study area.

## 🗺️ Live Demo

> Add your deployed link here (GitHub Pages, Netlify, Vercel, etc.)

## 🙌 Credits

- Vegetation datasets processed and published via [Google Earth Engine](https://earthengine.google.com/)
- MODIS data courtesy of NASA
- Landsat 9 data courtesy of NASA / USGS
- Sentinel-2 data courtesy of ESA / Copernicus

## 📄 License

This project is licensed under the [MIT License](LICENSE).


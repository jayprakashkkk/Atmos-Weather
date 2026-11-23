# ⛅ Atmos — Live Weather & Atmospheric Intelligence

[![Live Demo](https://img.shields.io/badge/Status-Active-success.svg)](#)
[![PWA](https://img.shields.io/badge/PWA-Ready-blue.svg)](#)
[![Zero Dependencies](https://img.shields.io/badge/Dependencies-0%20(Pure%20Vanilla)-brightgreen.svg)](#)
[![License](https://img.shields.io/badge/License-MIT-purple.svg)](#)

**Atmos** is a modern, ultra-lightweight, and visually stunning real-time weather web application built with pure vanilla web technologies (Zero external runtime dependencies). It features live hardware GPS targeting with neighborhood/colony-level accuracy, live radar loops, astronomical tracking of the sun and moon, real-time synthesized ambient soundscapes, and full Progressive Web App (PWA) support.

---

## ✨ Features

- **📍 Precision Live GPS & Local Colony Resolution**
  - Instant hardware-level geolocation (`maximumAge: 0`, high accuracy).
  - Reverse geocoding resolves your exact locality, colony, or sector (e.g., *Sector 62, Noida*, *Bandra West, Mumbai*).
  - High-resolution weather model selection (`models=best_match`) via Open-Meteo.

- **🛰️ Live Weather Radar (RainViewer Integration)**
  - Interactive live precipitation and cloud movement radar map with animated timeline controls.
  - Centered dynamically on your exact coordinates with zoom and layer controls.

- **🎨 Dynamic Atmospheric Scene & Glassmorphism UI**
  - Fluid background that smoothly transitions across conditions: *Clear Sky, Partly Cloudy, Overcast, Rainy, Snowy, Foggy, Sunset, and Thunderstorms with realistic lightning and rain animations*.
  - Clean glassmorphism aesthetic with responsive mobile-first typography and layout.

- **☀️ Sun Tracker & Golden Hour**
  - Real-time SVG celestial arc diagram showing current solar position and time until sunset/sunrise.
  - Solar noon, total daylight length, golden hour timing, and tomorrow's sunrise.

- **🌙 Astronomical Moon Phase Engine**
  - Pure algorithmic calculation of the 8 lunar phases, illumination percentage, and moon age.
  - Accurate moonrise and moonset estimates, next full moon, and next new moon dates.

- **📈 24-Hour Sparkline & 7-Day Outlook**
  - Interactive custom SVG temperature sparkline trend for the next 24 hours.
  - Hourly breakdown of conditions, temperatures, and precipitation probabilities.
  - 7-day extended forecast with visual min/max temperature gradient bars.

- **🏭 Air Quality & Health Metrics**
  - Real-time US AQI index rating and PM2.5 concentration levels.
  - In-depth weather metrics: Relative Humidity, Wind Speed & Direction, Wind Gusts, UV Index, Surface Pressure, Visibility, Dew Point, and Cloud Cover.
  - Smart weather alerts (Umbrella reminder, UV protection advice, Air quality precautions, Heat/cold alerts).

- **🔊 Synthesized Ambient Soundscapes (Native Web Audio API)**
  - 100% native synthesized weather audio with zero MP3 downloads.
  - Procedurally generated soothing rain, wind sweeps, thunder rumbles, and serene atmospheric drones that dynamically match the live weather.

- **📲 Progressive Web App (PWA)**
  - Fully installable on iOS, Android, macOS, and Windows.
  - Offline asset caching with Service Worker (`sw.js`).
  - Standalone app mode with custom SVG branding.

- **📤 Web Share & Smart Search**
  - One-click weather sharing via native Web Share API (or clipboard copy).
  - Debounced autocomplete search for any city or region worldwide.
  - History chips with quick-switch and removal options.
  - One-touch °C / °F unit toggle.

---

## 🚀 Getting Started

Because Atmos uses pure vanilla HTML, CSS, and JavaScript, no build step or package installation (`npm install`) is required!

### Prerequisites

To enable high-accuracy browser GPS geolocation, modern browsers require the app to be served over `http://localhost` or `https://` (direct `file:///` access restricts geolocation permissions).

### Running Locally

1. **Clone the repository:**
   ```bash
   git clone https://github.com/jayprakashkkk/Atmos-Weather.git
   cd Atmos-Weather
   ```

2. **Start a local HTTP server:**

   Using Python 3:
   ```bash
   python3 -m http.server 3000
   ```

   *Or using Node.js:*
   ```bash
   npx serve .
   ```

3. **Open in your browser:**
   ```
   http://localhost:3000
   ```

4. When prompted by your browser, click **"Allow"** for Location Access to instantly view your exact live neighborhood weather and temperature!

---

## 📁 Project Structure

```text
Atmos-Weather/
├── index.html        # Complete application (HTML5, Glassmorphism CSS, and Vanilla JS)
├── manifest.json     # PWA Web App Manifest
├── sw.js             # Service Worker for offline caching & PWA support
├── icon.svg          # Modern vector app icon
└── README.md         # Project documentation and guide
```

---

## 🌐 Data Sources & Attribution

- **Weather Forecast & Air Quality:** [Open-Meteo API](https://open-meteo.com/) (Free, open-source weather API)
- **Live Weather Radar:** [RainViewer API](https://www.rainviewer.com/)
- **Reverse Geocoding:** [BigDataCloud Client API](https://www.bigdatacloud.com/) & [OpenStreetMap Nominatim](https://nominatim.openstreetmap.org/)
- **Network Geolocation Fallback:** [ipwho.is](https://ipwho.is/)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

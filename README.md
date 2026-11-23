<div align="center">

# ⛅ ATMOS — LIVE WEATHER
### Ultra-Responsive, 100% Fullscreen Atmospheric Intelligence & Meteorological Dashboard

[![Status](https://img.shields.io/badge/Status-Production%20Ready-brightgreen.svg?style=for-the-badge)](#)
[![Fullscreen](https://img.shields.io/badge/UI-100%25%20Fullscreen-blueviolet.svg?style=for-the-badge)](#)
[![PWA](https://img.shields.io/badge/PWA-Installable-blue.svg?style=for-the-badge)](#)
[![Dependencies](https://img.shields.io/badge/Dependencies-0%20(Pure%20Vanilla)-orange.svg?style=for-the-badge)](#)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](LICENSE)

<br/>

**Atmos** is a state-of-the-art, zero-dependency, real-time meteorological web application engineered for modern multi-device ecosystems. From mobile smartphones to ultra-wide 4K desktop displays, Atmos transforms raw meteorological telemetry into an immersive, edge-to-edge glassmorphic experience featuring live radar, astronomical tracking, and native Web Audio ambient soundscapes.

[Explore Live Demo](https://jayprakashkkk.github.io/Atmos-Weather/) · [Report Bug](https://github.com/jayprakashkkk/Atmos-Weather/issues) · [Request Feature](https://github.com/jayprakashkkk/Atmos-Weather/issues)

</div>

---

## 📑 Table of Contents

- [🌟 Architectural Highlights](#-architectural-highlights)
- [🖥️ 100% Fullscreen Architecture (PC & Mobile)](#️-100-fullscreen-architecture-pc--mobile)
- [🎯 Comprehensive Feature Suite](#-comprehensive-feature-suite)
  - [1. Real-Time Hardware GPS & Colony Resolution](#1-real-time-hardware-gps--colony-resolution)
  - [2. Live RainViewer Weather Radar](#2-live-rainviewer-weather-radar)
  - [3. Astronomical Celestial Engine (Sun & Moon)](#3-astronomical-celestial-engine-sun--moon)
  - [4. Procedural Ambient Soundscapes (Web Audio API)](#4-procedural-ambient-soundscapes-web-audio-api)
  - [5. 24-Hour Sparklines & 7-Day Extended Forecast](#5-24-hour-sparklines--7-day-extended-forecast)
  - [6. Atmospheric Telemetry & Air Quality (AQI)](#6-atmospheric-telemetry--air-quality-aqi)
  - [7. Progressive Web App (PWA) & Offline Resiliency](#7-progressive-web-app-pwa--offline-resiliency)
- [🔬 Scientific & Algorithmic Foundations](#-scientific--algorithmic-foundations)
- [📁 Repository Architecture](#-repository-architecture)
- [🚀 Quick Start & Local Development](#-quick-start--local-development)
- [⌨️ Keyboard Shortcuts](#️-keyboard-shortcuts)
- [📱 Mobile Installation Guide (PWA)](#-mobile-installation-guide-pwa)
- [🌐 Data Providers & Attribution](#-data-providers--attribution)
- [📄 License & Author](#-license--author)

---

## 🌟 Architectural Highlights

```
┌────────────────────────────────────────────────────────────────────────────────┐
│                           ATMOS CLIENT RUNTIME                                 │
├──────────────────────────────┬─────────────────────────────────────────────────┤
│ Core Engine                  │ Pure Vanilla JavaScript (ES2022+), Zero Bundler │
│ UI & Layout                  │ Responsive 100% Fullscreen CSS Grid / Flexbox   │
│ Visual Effects               │ Multi-layered Animated CSS Weather Scenes       │
│ Audio Engine                 │ Native Web Audio API (Synthesized DSP Nodes)    │
│ Geolocation Pipeline         │ W3C High-Accuracy GPS + Client Reverse Geocoding│
│ Meteorological Provider      │ Open-Meteo High-Resolution Forecast Engine      │
│ Radar Provider               │ RainViewer Live Doppler Precipitation Radar     │
│ Offline / PWA Engine         │ Service Worker Cache API + Standalone Manifest  │
└──────────────────────────────┴─────────────────────────────────────────────────┘
```

- **Zero Runtime Dependencies**: No React, Vue, jQuery, Tailwind, or Chart.js. Everything is built natively with vanilla web standards for sub-millisecond execution and minimal memory footprint.
- **Micro-Second Load Time**: Single-page bundle with instant initial paint, optimized SVG vector graphics, and zero network bloat.
- **Privacy-Centric Geolocation**: Location queries are handled strictly on the client side; zero user tracking, zero remote database telemetry.

---

## 🖥️ 100% Fullscreen Architecture (PC & Mobile)

Atmos is architected to eliminate visual clutter and completely adapt to 100% of the display canvas on any device:

### 📱 Mobile & Smartphone Experience
- **Unboxed Clean Hero**: Temperature and locality float naturally on top of the dynamic weather background with subtle drop-shadows, creating an open, unboxed aesthetic matching modern mobile OS design.
- **Clean SVG Settings Drawer**: The home screen is decluttered into a single clean SVG settings icon (no emojis), opening a native bottom sheet housing Units, GPS, Live Radar, Soundscape, Sharing, and Installation.
- **Edge-to-Edge Viewport**: Engineered with `viewport-fit=cover` and dynamic viewport units (`100dvh`), eliminating dead white bars and stretching seamlessly to screen edges.
- **Notch & Safe-Area Insets**: Full native integration with iOS and Android display cutouts using CSS environment variables (`env(safe-area-inset-top)` and `env(safe-area-inset-bottom)`).
- **Thumb-Zone Navigation**: Mobile-first touch targets ($\ge 44\text{px}$) with tactile active feedback.

### 💻 PC, Tablet & Ultra-Wide Monitor Experience
- **Fluid Multi-Column Dashboard**: On widescreen monitors ($\ge 1100\text{px}$), the interface automatically expands into an auto-fitting multi-column dashboard, scaling metrics fluidly across the full screen width.
- **Hardware Fullscreen API**: Dedicated `⛶ Fullscreen` toggle button and keyboard shortcut (`F` key) to trigger the browser's native Fullscreen API for kiosk setups, wall-mounted displays, or ambient desktop weather stations.
- **Expansive SVG Sparkline**: Dynamic 1000-unit horizontal coordinate space that scales linearly across 1080p, 1440p, and 4K displays.

---

## 🎯 Comprehensive Feature Suite

### 1. Real-Time Hardware GPS & Colony Resolution
- **Zero-Cache Hardware Querying**: Initiates `navigator.geolocation.getCurrentPosition` with `maximumAge: 0` and `enableHighAccuracy: true` to prevent stale location caching.
- **Granular Locality Reverse-Geocoding**: Dual-tier reverse geocoding via BigDataCloud client API and OpenStreetMap Nominatim. Resolves exact neighborhoods, sectors, and colonies (e.g., *Sector 62, Noida*, *Bandra West, Mumbai*, *Indiranagar, Bengaluru*).
- **High-Resolution Meteorological Grid**: Open-Meteo queries incorporate exact 4-decimal coordinates ($\sim 11\text{m}$ resolution) combined with `models=best_match` to select the highest quality national numerical weather prediction model (ECMWF, GFS, ICON, HRRR).

### 2. Live RainViewer Weather Radar
- **Live Doppler Rain Map**: Integrates RainViewer's global radar overlay directly into an expandable, full-width glass modal.
- **Precipitation & Cloud Tracking**: Displays live precipitation intensity and cloud movement loops centered dynamically on your coordinates.

### 3. Astronomical Celestial Engine (Sun & Moon)
- **Sun Arc Tracker**: Real-time parabolic SVG visualization of the sun's path across the horizon, including solar noon, golden hour timing, daylight duration, and next-day sunrise countdown.
- **Algorithmic Lunar Engine**: Accurately computes the current phase, age in days, and illumination percentage across all 8 major lunar phases (*New Moon, Waxing Crescent, First Quarter, Waxing Gibbous, Full Moon, Waning Gibbous, Last Quarter, Waning Crescent*).
- **Horizon Transit Solver**: SunCalc-style trigonometric altitude solver to estimate daily moonrise and moonset times.

### 4. Procedural Ambient Soundscapes (Web Audio API)
- **100% Native Audio DSP**: Generates soothing, procedural ambient sound directly in the browser with **zero external audio files**.
- **Dynamic Weather Modulation**:
  - *Rain & Thunder*: Generates custom pink/brown noise using a 2-second synthesized audio buffer passed through a resonant bandpass filter, with low-frequency oscillator rumble for thunderstorms.
  - *Windy Conditions*: Sweeping low-pass filter frequency modulations simulating gusting breezes.
  - *Clear Sky / Evening*: Calming harmonic sine-wave drones ($174\text{Hz}$ / $220\text{Hz}$) for peaceful ambient focus.

### 5. 24-Hour Sparklines & 7-Day Extended Forecast
- **Vector Sparkline Trend**: Custom SVG polyline mapping 24-hour temperature curves with subtle gradient fills and dynamic high/low labels.
- **Horizontal Scroll Carousel**: Smooth snap-to-card hourly view displaying time, condition icon, temperature, and percentage chance of rain.
- **7-Day Outlook**: Daily min/max temperature gradient sliders calibrated against the week's absolute high and low extremes.

### 6. Atmospheric Telemetry & Air Quality (AQI)
- **Complete Metric Grid**:
  - Relative Humidity (%) & Comfort Classification (Dry, Comfortable, Muggy)
  - Wind Velocity, Gust Peak, and 8-Point Compass Direction
  - Direct UV Index & Safe Exposure Duration
  - Surface Atmospheric Pressure ($\text{hPa}$) & Barometric Trends
  - Optical Visibility ($\text{km}$ / $\text{mi}$) & Cloud Cover Percentage (%)
  - Calculated Dew Point Temperature
- **Air Quality Telemetry**: Integrated Open-Meteo Air Quality API monitoring real-time US AQI and $\text{PM}_{2.5}$ particulate levels.
- **Contextual Health Advisory**: Automated advisories for rain gear, high UV exposure, severe heat, wind precautions, and air quality mask warnings.

### 7. Progressive Web App (PWA) & Offline Resiliency
- **Installable**: Full Web App Manifest (`manifest.json`) compliant with desktop and mobile installation criteria.
- **Service Worker (`sw.js`)**: Network-first strategy with automatic fallback to cached assets when offline.

---

## 🔬 Scientific & Algorithmic Foundations

Atmos contains mathematical modeling implementations for astronomy and signal processing:

### 1. Lunar Phase & Illumination Formula
The lunar cycle calculation computes the time elapsed since the reference epoch (January 6, 2000, 18:14 UTC):
$$\Delta d = \frac{\text{Date.now()} - \text{Date.UTC}(2000, 0, 6, 18, 14)}{86,400,000}$$
$$\text{Phase Fraction } (p) = \left( \frac{\Delta d \pmod{29.530588} + 29.530588}{29.530588} \right) \pmod 1$$
$$\text{Illumination Percentage} = \frac{1 - \cos(2\pi p)}{2} \times 100$$

### 2. Moon Altitude Approximation
Calculates equatorial coordinates and topocentric altitude ($h$) using ecliptic coordinates:
$$L = 218.316^\circ + 13.176396^\circ d, \quad M = 134.963^\circ + 13.064993^\circ d, \quad F = 93.272^\circ + 13.22935^\circ d$$
$$h = \arcsin\left(\sin(\phi)\sin(\delta) + \cos(\phi)\cos(\delta)\cos(H)\right)$$

### 3. Procedural Noise Generation for Ambient Weather Audio
A 3-pole IIR filter algorithm filters white noise into brown/pink noise suitable for rainfall modeling:
$$b_0 = 0.99 b_0 + 0.05 \cdot \text{white}$$
$$b_1 = 0.95 b_1 + 0.10 \cdot \text{white}$$
$$b_2 = 0.85 b_2 + 0.25 \cdot \text{white}$$
$$\text{sample} = 0.35 \cdot (b_0 + b_1 + b_2)$$

---

## 📁 Repository Architecture

```text
Atmos-Weather/
├── index.html        # Single-file core application (HTML5, Responsive CSS3, Vanilla JS ES2022)
├── manifest.json     # W3C Web App Manifest (PWA configuration)
├── sw.js             # Service Worker for Cache Storage & offline execution
├── icon.svg          # Vector branding & multi-resolution app icon
└── README.md         # Professional project documentation
```

---

## 🚀 Quick Start & Local Development

No compilation, transpilation, or Node package installations are needed!

### Running via Local Server (Recommended for GPS Access)

Modern web browsers require an active HTTP origin (`http://localhost` or `https://`) to grant high-accuracy GPS permissions.

#### Option 1: Python 3 (Pre-installed on macOS/Linux)
```bash
# Clone the repository
git clone https://github.com/jayprakashkkk/Atmos-Weather.git
cd Atmos-Weather

# Start instant HTTP server on port 3000
python3 -m http.server 3000
```
Open your browser at `http://localhost:3000`.

#### Option 2: Node.js (via npx serve)
```bash
npx serve .
```

#### Option 3: Docker
```bash
docker run --rm -p 8080:80 -v "$PWD":/usr/share/nginx/html:ro nginx:alpine
```
Open your browser at `http://localhost:8080`.

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action | Description |
| :---: | :---: | :--- |
| <kbd>/</kbd> | **Quick Search** | Automatically focuses the city search input |
| <kbd>Esc</kbd> | **Close Overlays** | Closes settings drawer, radar viewer, or suggestions |

---

## 📱 Mobile Installation Guide (PWA)

### iOS (Safari)
1. Open Atmos in Safari.
2. Tap the **Share** button (box with an upward arrow) in the bottom navigation bar.
3. Scroll down and select **"Add to Home Screen"**.
4. Tap **"Add"**. Atmos will now launch in 100% fullscreen standalone mode with zero browser chrome!

### Android (Chrome / Edge)
1. Open Atmos in Chrome.
2. An **"📲 Install"** button will automatically appear in the top header.
3. Tap **Install**, or tap the browser menu ($\vdots$) and select **"Install App"**.

---

## 🌐 Data Providers & Attribution

- **Weather Forecasting & Air Quality**: [Open-Meteo](https://open-meteo.com/) *(Licensed under CC BY 4.0)*
- **Live Doppler Precipitation Radar**: [RainViewer](https://www.rainviewer.com/)
- **Client Reverse Geocoding**: [BigDataCloud API](https://www.bigdatacloud.com/) & [OpenStreetMap](https://www.openstreetmap.org/)
- **Network Geolocation Fallback**: [ipwho.is](https://ipwho.is/)

---

## 📄 License & Author

This project is open-source software licensed under the **[MIT License](LICENSE)**.

Developed with ❤️ by **[Jay Prakash](https://github.com/jayprakashkkk)**.

⭐ **If you find Atmos useful, consider giving this repository a star!**

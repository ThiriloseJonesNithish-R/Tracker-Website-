# 🛸 Fusion Frame — Drone Flight Tracker & Simulator

<p align="center">
  <img src="https://img.shields.io/badge/Version-1.0.0-blue?style=for-the-badge" alt="Version">
  <img src="https://img.shields.io/badge/Built%20With-HTML5%20%7C%20CSS3%20%7C%20JS-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="Stack">
  <img src="https://img.shields.io/badge/Mapping-Leaflet.js-199900?style=for-the-badge&logo=leaflet&logoColor=white" alt="Leaflet">
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="License">
</p>

<p align="center">
  A lightweight, interactive browser-based telemetry simulator and path visualization tool for UAVs / Drones using <b>Leaflet.js</b> and <b>OpenStreetMap</b>.
</p>

---

## 📌 Overview

**Fusion Frame** is an open-source flight path simulator designed to replay and visualize drone telemetry datasets exported from IoT platforms such as **ThingSpeak**. 

Simply upload a standard flight telemetry CSV file, hit **Start Simulation**, and watch your drone fly across a live, dynamic map complete with real-time HUD telemetry, smooth path interpolation, and auto-centering camera feeds.

---

## ✨ Key Features

- 🛰️ **Interactive Dynamic Map**: Powered by **Leaflet.js** and **OpenStreetMap** with full panning, zooming, and tracking capabilities.
- 📈 **Real-Time Flight Polyline**: Traces and renders flight history paths dynamically as the drone travels.
- 📊 **Telemetry Pop-up HUD**: Live telemetry data overlay on the drone marker:
  - **UIN** (Unique Identification Number)
  - **GPS Coordinates** (Latitude & Longitude)
  - **Speed** ($m/s$)
  - **Timestamp**
  - **Battery Percentage** ($\%$)
  - **Altitude / Elevation**
- 📂 **Plug & Play CSV Parser**: In-browser client-side CSV processing with zero external server dependencies.
- ⚡ **Zero Setup Required**: Entirely standalone single-page application (`index.html`) ready to run in any modern web browser.

---

## 📂 CSV Telemetry Format

To ensure seamless playback, your CSV file should include a header row followed by at least **7 comma-separated columns** per entry:

```csv
UIN,Latitude,Longitude,Speed,TimeStamp,BatteryPercentage,Elevation
DRONE-IND-001,13.0827,80.2707,12.5,2026-09-29 10:00:00,98,45.2
DRONE-IND-001,13.0835,80.2715,14.1,2026-09-29 10:00:05,97,48.0
DRONE-IND-001,13.0848,80.2729,13.8,2026-09-29 10:00:10,96,50.1

```

> **Note:** If exporting from **ThingSpeak**, align your channel fields with the order: `Field 1: UIN`, `Field 2: Latitude`, `Field 3: Longitude`, `Field 4: Speed`, `Field 5: Timestamp`, `Field 6: Battery %`, `Field 7: Elevation`.

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone [https://github.com/ThiriloseJonesNithish-R/Tracker-Website-.git](https://github.com/ThiriloseJonesNithish-R/Tracker-Website-.git)
cd Tracker-Website-

```

### 2. Run the Application

Because it is a self-contained web app, simply open `index.html` directly in your browser:

* **Double click** `index.html`, or
* Use a live server extension (e.g., VS Code Live Server):
```bash
npx serve .

```



---

## 🧭 How to Use

1. **Log in** to your IoT platform (e.g., [ThingSpeak](https://thingspeak.com)).
2. Go to your target channel and **Export / Download** your feed data in `.csv` format.
3. Open **Fusion Frame** in your browser.
4. Click **Upload File** and select your downloaded CSV.
5. Click **Start Simulation** to launch the flight path animation.

---

## 🛠️️ Tech Stack

| Technology | Purpose |
| --- | --- |
| **HTML5 / CSS3** | Clean UI, landing screen, and responsive layout |
| **JavaScript (ES6+)** | FileReader API, simulation loop & telemetry parsing |
| **Leaflet.js** | Geospatial map rendering, layer control, and marker animation |
| **OpenStreetMap** | Open-source map tile provider |

---

## 🤝 Contributing

Contributions, feature requests, and bug reports are welcome!

1. Fork the Project.
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`).
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the Branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

---

## 📄 License

Distributed under the **MIT License**. See `LICENSE` for more information.

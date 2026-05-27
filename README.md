# Rapid Telemetry: F1 Distance Comparison & Pace Analysis

**Rapid Telemetry** is a high-performance, web-based analytical tool designed for Formula 1 enthusiasts and data analysts. It leverages the OpenF1 API to provide deep insights into driver performance through intra-lap telemetry comparison and session-wide pace analysis.

## 🚀 Features

### 1. Telemetry Viewer (Dual-Slot Comparison)
*   **Slot Manager:** Compare two different laps (Reference vs. Comparison) across any session.
*   **Distance-Based Plotting:** Unlike time-based charts, telemetry is plotted against distance (meters) to accurately compare braking points and apex speeds regardless of lap time differences.
*   **Multi-Data Visualization:**
    *   **Speed (km/h):** Overlay speed traces to find where time is found.
    *   **Inputs (%):** Analyze Throttle and Brake application.
    *   **Engine Data:** View RPM and Gear selection synchronized with track position.
    *   **Time Delta:** A real-time calculation of time gained/lost across the lap.

### 2. Geospatial Insight Mapping
*   **Dynamic Track Map:** The circuit map is segmented by performance—Red sections indicate the Reference driver is faster, while Cyan sections indicate the Comparison driver is faster.
*   **Chart-to-Map Synchronization:** Hovering over any telemetry chart updates a cursor on the track map to show exactly where that data point occurred on the circuit.
*   **Sector Zoom:** Click any sector in the comparison table to automatically zoom all charts and the map to that specific portion of the track.

### 3. Advanced Pace Analysis
*   **Session-Wide Visualization:** View every lap of a session color-coded by tire compound (Soft, Medium, Hard, Intermediate, Wet).
*   **Driving Characteristics Report:** Automatically generated metrics including:
    *   **Consistency Score:** Calculated via Standard Deviation of lap times.
    *   **Tire Management:** Estimated degradation rates (seconds lost per lap per compound).
    *   **Pit Cycle Analysis:** Calculation of "Total Pit Loss" by combining In-lap and Out-lap performance.
*   **Strategy Insights:** Automated comparison of stint lengths and compound choices.

### 4. Communication & Context
*   **Team Radio:** Integrated audio player and transcripts for driver-engineer communications.
*   **Race Control Log:** A chronological log of flags (Yellow, Red, Green) and Safety Car periods.

---

## 🛠️ Tech Stack

*   **Frontend:** Vanilla JavaScript (ES6+), HTML5, CSS3.
*   **Charts:** [Chart.js](https://www.chartjs.org/) (v4.4.2).
*   **Plugins:** [chartjs-plugin-annotation](https://www.chartjs.org/chartjs-plugin-annotation/).
*   **API:** [OpenF1](https://openf1.org/) (Unofficial F1 Data API).

---

## 📥 Installation

Rapid Telemetry is a static web application. No build step or server-side environment (like Node.js) is required for deployment.

**Check out the website:** <a href="https://rapidtelem.com" target="_blank">rapidtelem.com</a>

or

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/yourusername/rapid-telemetry.git
    ```
2.  **Open the project:**
    Simply open `index.html` in any modern web browser.

---

## 📖 Usage Guide

1.  **Select Data:** Use the header controls to select the Year, Meeting (Grand Prix), Session, and Driver.
2.  **Load Lap 1:** Click a lap from the "Laps" sidebar to load it into Slot 1.
3.  **Load Lap 2:** Click "Slot 2 (Compare)" in the Slot Manager, then select another lap (either from the same driver or a different one).
4.  **Analyze:** Use the charts to identify performance gaps. Hover over the speed trace to see the exact corner on the track map where the speed difference occurs.
5.  **Pace Analysis:** Click the "Pace Analysis" button to open the modal. Select two drivers to compare their entire race stint performance and tire life.

---

## 🧪 Technical Details

### Distance-Based Interpolation
The application converts timestamped telemetry into distance-based data using the following logic:
```javascript
cumulativeDist += (avgSpeedMs * timeDiff);
```
This allows for a "Spatial Comparison" which is the professional standard in motorsport engineering, as it accounts for different lines taken by drivers.

### API Resilience
The application includes a `delay()` helper and recursive retry logic to handle `429 (Too Many Requests)` responses, ensuring the UI remains stable even when fetching large datasets for an entire race.

---

## ⚖️ Disclaimer

**Rapid Telemetry** is an unofficial hobby project. It is not affiliated with Formula 1, the FIA, or any F1 team. All data is provided "as-is" via the OpenF1 API for personal and educational use.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

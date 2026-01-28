# 🚀 Rapid Telemetry Viewer for iRacing

## Fast, Free, Local Telemetry Analysis – No Install, No Account, No Cloud! [rapidtelem.com] (https://rapidtelem.com)

<img width="540" height="360" alt="image" src="https://github.com/user-attachments/assets/92f4e2ef-67dc-4acf-af89-b0017cf1b6ca" />

The Rapid Telemetry Viewer is a client-side, browser-based tool designed specifically for iRacing telemetry data analysis. Unlike conventional telemetry solutions, this viewer redefines accessibility and privacy, offering a powerful suite of analysis features encapsulated within a single, portable HTML file. Forget installations, subscriptions, or data uploads. Simply open the file in your web browser, import your iRacing `.ibt` files, and dive deep into your driving data instantly.

---

### ✨ Key Features at a Glance

*   **Pure Client-Side Operation:** Runs entirely in your web browser, no backend server or internet connection required after initial load.
*   **Direct `.ibt` File Parsing:** Efficiently reads and processes iRacing's binary telemetry (`.ibt`) files locally.
*   **Interactive Lap Comparison:**
    *   Load multiple `.ibt` files simultaneously.
    *   Automatic detection of complete and valid laps.
    *   Identify and highlight fastest laps within a file.
    *   Toggle lap visibility and select a reference lap for comparison.
    *   Customizable lap colors for easy distinction.
*   **Comprehensive Charting Suite:** Visualize critical driving data across various synchronized charts:
    *   **Time Delta Chart:** Compare lap times against a reference lap, section by section.
    *   **Speed Chart:** Analyze speed profiles throughout the lap.
    *   **Throttle/Brake Input Chart:** Examine driver inputs and ABS activity.
    *   **Steering Angle Chart:** Understand steering patterns.
    *   **RPM/Gear Chart:** Monitor engine RPM and gear selections.
    *   **Suspension Velocity Histogram:** Analyze damper velocities for ride quality and setup validation (X-axis symmetrical around zero).
*   **Dynamic Visual Aids:**
    *   **Interactive Track Map:** See your driving line, synced with cursor positions across other charts.
    *   **ABS Active Zones:** Overlay shaded regions on the throttle/brake chart to highlight ABS activation.
    *   **Sector Lines:** Vertical markers indicate predefined sector boundaries across all distance-based charts.
*   **In-Depth Analysis Tools:**
    *   **Sector Analysis Table:** Quick comparison of sector times and deltas against the reference lap.
    *   **"Placemat" Report:** Generate a printable PDF report for detailed side-by-side comparison of selected laps, including track maps with ABS zones and min-speed corner markers, and detailed sector metrics.
*   **Enhanced User Experience:**
    *   **Intuitive Controls:** Easy file import, lap selection, and chart interaction.
    *   **Synchronized Zoom & Pan:** Effortlessly navigate through telemetry data; zoom/pan on one distance-based chart reflects across others. Damper velocity chart zooms independently.
    *   **Reset Zoom Functionality:** Quickly reset chart views to auto-scaled.
    *   **Chart Fullscreen Toggle:** Expand any individual chart to fill the main view area for focused analysis without hiding the sidebar.
    *   **Responsive Design:** Adapts to various screen sizes.

---

### 🌟 Why Choose Rapid Telemetry Viewer?

This tool stands out from traditional telemetry analysis software by offering unparalleled benefits:

*   **⚡ Unparalleled Accessibility:** It's a single `.html` file. **No complex software installations**, no dependencies to manage. Just download it, open it in any modern web browser (Chrome, Firefox, Edge, Safari), and you're ready.
*   **🔒 Absolute Data Privacy:** Your telemetry data (`.ibt` files) **never leaves your computer**. There are no accounts to create, no servers to upload to, and no cloud processing. All analysis happens locally in your browser, ensuring your driving data remains entirely private and secure.
*   **💰 Completely Free:** No licenses, no subscriptions, no hidden costs. It's free to use, forever.
*   **🌐 Offline Capability:** Once loaded in your browser, the tool functions perfectly without an internet connection, making it ideal for use at the trackside, in your sim rig, or anywhere you need rapid analysis on the go.
*   **🚀 Blazing Fast Performance:** Leveraging modern browser technologies for binary parsing and GPU-accelerated rendering via Chart.js, the viewer offers a smooth and responsive experience.
*   **💡 Open & Extensible Design:** For the curious mind, the entire source code is right there in the HTML file. Inspect it, learn from it, and even modify it to add your own custom features or integrate with other tools.

---

### 📖 How to Use

1.  **Download:** Grab the `index.html` file from this GitHub repository.
2.  **Open:** Double-click the downloaded `.html` file, or drag it into your preferred modern web browser.
3.  **Import Data:** Click the "Import .ibt File(s)" button in the header and select one or more iRacing `.ibt` telemetry files.
4.  **Analyze:** Your laps will appear in the sidebar. Select laps for comparison, choose a reference lap, and explore the interactive charts. Utilize the zoom, pan, and fullscreen options for detailed insights.

---

### 📊 Supported iRacing Telemetry Variables

The viewer intelligently parses your `.ibt` files to extract and visualize the following key channels:

*   `Lap`, `LapDist`, `SessionTime`
*   `Speed` (converted to km/h)
*   `RPM`, `Gear`
*   `Throttle`, `Brake` (converted to %)
*   `SteeringWheelAngle` (converted to radians)
*   `Lat`, `Lon` (for track map generation)
*   `LapInvalid`, `BrakeABSactive`
*   `FuelLevel`
*   `LFshockVel`, `RFshockVel`, `LRshockVel`, `RRshockVel` (for damper velocity histogram)

---

### 🛠 Technical Highlights

*   **Frontend:** Pure HTML, CSS, and JavaScript.
*   **Binary Parsing:** Utilizes `FileReader` and `DataView` for efficient, in-browser processing of `.ibt` binary data structures.
*   **Charting:** Powered by `Chart.js` for dynamic, interactive, and high-performance data visualization.
*   **Chart.js Plugins:** Integrates `chartjs-plugin-zoom` for advanced navigation and `chartjs-plugin-annotation` for visual cues like sector lines and ABS zones.
*   **Modular Design:** JavaScript code is structured into logical functions and classes for maintainability and extensibility.

---

### 🤝 Contributing

We welcome community contributions! If you have ideas for new features, bug fixes, or performance improvements, please feel free to fork the repository and submit a pull request.

---

### 📧 Contact

Questions, feedback, or suggestions? Reach out to us at:
[hello@rapidtelem.com](mailto:hello@rapidtelem.com)

---

### 📄 License

This project is licensed under the MIT License - see the `LICENSE` file for details.

# Heat-Furnace-SCADA

# ⚡ Enterprise SCADA / MES HMI Monitoring Dashboard

A high-performance, real-time industrial SCADA (Supervisory Control and Data Acquisition) / MES Human-Machine Interface built for browser-based monitoring and telemetry control across industrial furnace lines.

![SCADA Dashboard Preview](https://img.shields.io/badge/System-SCADA%20%2F%20MES-blue?style=for-the-badge)
![MQTT Protocol](https://img.shields.io/badge/Protocol-MQTT%20via%20WebSockets-orange?style=for-the-badge)
![Status](https://img.shields.io/badge/Deployment-GitHub%20Pages-brightgreen?style=for-the-badge)

---

## 🌟 Key Features

* **Real-Time MQTT Telemetry:** Connects directly to secure Cloud MQTT brokers (HiveMQ) over WebSockets for low-latency Process Value (PV) and Set Value (SV) updates.
* **Auto-Collapsing Navigation:** Selecting a machine automatically glides the sidebar shut to maximize real-time chart visualization area.
* **Persistent Machine Tag Renaming:** Custom machine labels (e.g., *Boiler Alpha*, *Rotary Kiln B*) persist across browser refreshes via browser `localStorage`.
* **Alarm System & Exportable Logs:** 
  * Visual critical threshold banners when $PV > 80^\circ\text{C}$.
  * Dedicated Notification Center with **📥 Export Alarms CSV** button for full audit trails.
* **Telemetry Data Export:** Instant **📊 Export CSV** generation for offline trend analysis in Microsoft Excel.
* **Custom UI Themes & Fonts:**
  * **Theme Switcher:** Dark Mode (Industrial Dark) / Light Mode (Clean White).
  * **Typography Switcher:** Inter (Modern UI), Roboto Mono (Technical SCADA), Segoe UI.

---

## 🛠️ Technology Stack

* **Frontend:** HTML5, CSS3 (CSS Variables for themes), Vanilla JavaScript (ES6+)
* **Charting:** [Chart.js](https://www.chartjs.org/) for real-time line charts
* **Messaging:** [MQTT.js](https://github.com/mqttjs/MQTT.js) over Secure WebSockets (`wss://`)
* **MQTT Broker:** HiveMQ Cloud Broker

---

## 📡 MQTT Topic Architecture

| Topic Pattern | Direction | Payload Example | Description |
| :--- | :--- | :--- | :--- |
| `factory/+/temp/pv` | **Subscribe** | `{"pv": 75.4, "status": "HEATING"}` | Receives real-time temperature telemetry |
| `factory/{machine_id}/temp/sv` | **Publish** | `{"sv": 65.0}` | Transmits updated target setpoints to PLCs |

---

## 🚀 How to Run Locally

1. **Clone the Repository:**
   ```bash
   git clone [https://github.com/YOUR_GITHUB_USERNAME/heat-furnace-scada.git](https://github.com/YOUR_GITHUB_USERNAME/heat-furnace-scada.git)
   cd heat-furnace-scada

   ---

## 🛠️ How to Add This File to GitHub

1. Go to your **`heat-furnace-scada`** repository on GitHub.
2. If you see a button that says **"Add a README"**, click it. 
   *(If you already have a `README.md` file, click on it and select the **✏️ Edit** pencil icon).*
3. Paste the markdown code above into the editor.
4. Replace `YOUR_GITHUB_USERNAME` in the clone command with your actual GitHub username.
5. Select **"Commit directly to the main branch"** and click **Commit changes**.

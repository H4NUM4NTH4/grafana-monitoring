# 📊 Grafana System Monitoring

This project sets up a **complete monitoring stack** using **Grafana**, **Prometheus**, and **Node Exporter** inside Docker.  
It allows you to visualize real-time system metrics (CPU, memory, disk, etc.) and configure **alerts** (like high CPU usage, memory alerts) directly in Grafana.

---

## ⚡ Features
- ✅ System monitoring with Prometheus + Node Exporter  
- ✅ Beautiful Grafana dashboards with multiple panels  
- ✅ Alerting rules (e.g., high CPU or memory usage)  
- ✅ Docker Compose setup (easy to run)  
- ✅ JSON export of dashboards for easy import/reuse  

---

## 📂 Project Structure
```
grafana-monitoring/
├── docker-compose.yml        # Docker Compose file to start all services
├── grafana/                  # Grafana configs
│   └── dashboards/           # Exported Grafana dashboards
│       └── system-monitoring.json
└── prometheus/               # Prometheus configs
    └── prometheus.yml
```

---

## 🐳 Setup & Installation

### 1️⃣ Clone this repository
```bash
git clone git@github.com:H4NUM4NTH4/grafana-monitoring.git
cd grafana-monitoring
```

### 2️⃣ Start services with Docker Compose
```bash
docker compose up -d
```

### 3️⃣ Access the services
- **Prometheus** → [http://localhost:9090](http://localhost:9090)  
- **Node Exporter** → [http://localhost:9100](http://localhost:9100/metrics)  
- **Grafana** → [http://localhost:3000](http://localhost:3000)  
  - Username: `admin`  
  - Password: `admin`  

---

## 📊 Grafana Dashboards

- Import `grafana/dashboards/system-monitoring.json` into Grafana:
  1. Open Grafana → Dashboards → Import
  2. Upload the JSON file
  3. Start monitoring 🚀

### Example Panels:
- **CPU Usage (%)**  
- **Memory Usage (%)**  
- **Disk Usage (%)**  
- **System Load Average**

---

## 🚨 Alerts

Example: High CPU Usage Alert  
- Triggered when CPU usage > 80% for 1 minute  
- Configurable under **Alerting → Alert Rules**  
- Can integrate with Email, Slack, or other Notifiers  

---

## 🛠️ Tech Stack
- [Grafana](https://grafana.com/) → Visualization & Dashboards  
- [Prometheus](https://prometheus.io/) → Metrics collection  
- [Node Exporter](https://github.com/prometheus/node_exporter) → System metrics  
- [Docker](https://www.docker.com/) → Containerized setup  

---

## 🚀 Future Improvements
- Add more exporters (e.g., MySQL, Redis, Kafka)  
- Create advanced dashboards  
- Integrate Grafana with Slack/Email for alert notifications  

---

## 🤝 Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you’d like to change.

---

## 📜 License
This project is open-source under the **MIT License**.

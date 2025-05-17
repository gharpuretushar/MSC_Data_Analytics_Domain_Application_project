# 🚆 Optimizing Metro Train Maintenance with Predictive Analytics

This project presents an advanced deep learning solution for **predictive maintenance of metro trains**, focusing on **sensor fault detection** in the **Air Production Unit (APU)** using a **Sparse Autoencoder** model. Built with the real-world **MetroPT dataset**, this project enables early anomaly detection, visual explanations, and clustering of failure types for actionable maintenance planning.

---

## 📌 Project Overview

> Traditional maintenance techniques either wait for failure (reactive) or rely on schedule-based checks (preventive). Our project applies an unsupervised Sparse Autoencoder to learn from sensor patterns and identify failures **before they occur**.

### Project Goals:
- Build a 3D Time-Aware Autoencoder using windowed sensor data
- Pinpoint abnormal behavior across 17+ analog and digital sensor types
- Cluster similar failures using PCA and KMeans for interpretability
- Enable real-time, lightweight deployment for metro APU maintenance

---

## 🛠️ Tools & Technologies

- **Deep Learning**: TensorFlow, Keras
- **Clustering & Explainability**: Scikit-learn (PCA, KMeans)
- **Visualization**: Matplotlib, Seaborn
- **Data**: MetroPT Dataset (Open Source)
- **Model Type**: Sparse Autoencoder (TimeDistributed)

---

## 🗂️ Project Files

| File | Description |
|------|-------------|
| `x23289902_Tushar_Domain_Application_Report.docx` | Full report covering background, methodology, implementation, results, and business value. |
| `PPT_Metro.pptx` | Final presentation slide deck showcasing key findings and model insights. |

---

## 📊 Key Features

- 📈 **3D Input**: `(samples × 30 timesteps × 17 features)` windowing for time series learning
- ⚙️ **TimeDistributed Layers**: Dense layers applied to each timestep for temporal awareness
- 🎯 **L1 Regularization**: Enforces sparsity, avoids overfitting, highlights critical signals
- 📉 **Dynamic Thresholding**: Anomalies flagged at 95th percentile of reconstruction error
- 🧩 **PCA + KMeans**: Groups anomalies into failure categories like pressure faults, overheating, etc.
- 🔎 **Sensor-Level Error Analysis**: Tracks which sensors contribute to each anomaly

---

## 🔍 Dataset: MetroPT

- Contains **real-world sensor data** from a metro train's air production unit (APU)
- Data includes both **analog** (e.g., motor current, oil temperature) and **digital** signals
- Used widely in academic research (see references below)

Reference: [MetroPT Dataset – Scientific Data (Nature)](https://doi.org/10.1038/s41597-022-01877-3)

---

## 📈 Visual Insights

Included in the report:
- Boxplots of sensor ranges and anomalies
- Error distribution charts with 95% threshold
- PCA cluster maps of detected failure types
- Time-based reconstruction error analysis

These visualizations offer strong interpretability for engineers and maintenance staff.

---

## 📉 Results

| Metric | Value |
|--------|-------|
| MSE (Test) | ~0.0014 |
| RMSE | ~0.00226 |
| Anomalies Detected | 7,128 out of 142,556 |
| Clustering Silhouette Score | 0.63 |
| Key Faulty Sensors | Flowmeter, Oil Temperature, Motor Current |

---

## 💼 Business Value

- 🔧 Enables proactive, targeted maintenance before system failure
- 💰 Reduces downtime and cost of unnecessary inspections
- 📊 Dashboard-friendly metrics and visualizations for decision-makers
- ⚡ Real-time deployment potential with fast, low-parameter model (only 2,209 trainable params)
- 🧠 Supports smart cities' transportation systems with sustainable operations

---

## 🏷️ Domain Area

**Transportation & Infrastructure**, specifically:
- Metro Rail Systems
- Predictive Maintenance in Public Transit
- Sensor-based Fault Detection

---

## 📚 References

1. Davari, N. et al., “Predictive Maintenance using Deep Learning for Railway APU”, [IEEE Xplore](https://ieeexplore.ieee.org/abstract/document/9564181/)
2. Najjar, A. et al., “Classification of APU Failures Using ML”, SSRN (2023) – [SSRN Link](https://doi.org/10.2139/ssrn.4403258)
3. Veloso, B. et al., “The MetroPT Dataset for Predictive Maintenance”, Scientific Data (2022) – [Nature](https://doi.org/10.1038/s41597-022-01877-3)
4. Barpute, J. et al., “CatBoost/XGBoost Comparison for Metro APU”, IEEE ICESC (2024)

---

## 📘 License

This project was developed as part of the Domain Application module at **National College of Ireland** by Tushar Rajesh Gharpure (x23289902). For academic use only.

---

## ✨ Tags

`#SparseAutoencoder` `#PredictiveMaintenance` `#MetroPT` `#SensorData` `#KMeans` `#AnomalyDetection` `#TransportationAI` `#DomainApplications`
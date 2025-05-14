# 🐟 Estimating Fish Weight Growth in Aquaponic Farming using Machine Learning

> Smart farming meets machine learning to boost fish harvest in aquaponic systems.

---

## 🌱 Project Overview

Conventional farming is struggling to keep up with rising food demands due to urbanization and climate change. **Aquaponics**, a symbiotic system of fish and plants, offers a sustainable alternative. But here’s the kicker — without intelligent monitoring, it's inefficient.

This project leverages **machine learning regression algorithms** to **predict the final harvest weight of fish** based on real-time sensor data in aquaponic ponds. The goal? Automate and optimize fish farming for **maximum yield** with **minimum waste**.

---

## 🔬 Problem Statement

Fish health and growth in aquaponics depend on multiple water parameters like temperature, pH, ammonia, turbidity, nitrate, and dissolved oxygen. Manual monitoring is outdated and unreliable.

So, we built a smart ML pipeline to:

- Predict fish harvest weight
- Optimize pond conditions
- Reduce human guesswork

---

## 📦 Dataset Description

Collected from 12 aquaponic catfish ponds using an **ESP32-based IoT setup**, measuring:

- 🌡 Temperature (DS18B20)
- 💧 Dissolved Oxygen
- ⚗️ pH
- ☁️ Turbidity
- 🧪 Ammonia & Nitrate levels

Each reading was captured every 5 seconds from **June to October 2021**, generating over **223,000 samples**.

---

## 🛠️ Preprocessing Pipeline

- 🔄 Filled missing/NaN values via forward fill
- 📏 Descaled ammonia & nitrate using log and sqrt transformations
- 📆 Parsed timestamp into year, month, date, hour, min, sec
- 🔍 Removed outliers based on domain thresholds

---

## 🤖 ML Models Used

We used 6 regression models to predict `Fish Weight (g)`:

1. **Linear Regression**
2. **Lasso Regression**
3. **Ridge Regression**
4. **KNN Regression**
5. **Support Vector Regression (SVR)**
6. **Decision Tree Regression**

---



✅ **KNN and Decision Tree** dominated across all metrics.

---

## 📈 Visual Insights

We explored relationships between features and fish growth:

- Ideal **temperature**: ~24°C
- Safe **pH range**: 6–8
- Stable **dissolved oxygen**: 5–20 g/ml
- **Ammonia & nitrate** levels were normalized before modeling

---

## 🚀 Future Work

- 🧠 Integrate deep learning (CNN/RNN) for better predictions
- 🎥 Add image-based features using YOLO or ResNet
- 🌿 Predict plant health for full aquaponics optimization
- 💰 Compare economic value: aquaponics vs traditional farming

---

## 📚 Tech Stack

- Python 🐍
- Pandas, NumPy, Matplotlib
- Scikit-learn
- ESP32 + IoT Sensors

---






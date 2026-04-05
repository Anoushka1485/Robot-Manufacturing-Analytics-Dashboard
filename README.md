# 🤖 Robot Manufacturing Analytics Dashboard

## 📌 Overview

This project simulates a humanoid robot manufacturing analytics system, designed to monitor production performance, detect failures, and identify process inefficiencies across assembly stages.

Using a real-world predictive maintenance dataset, I built a data pipeline and dashboard that mirrors how manufacturing teams track and optimize production in a robotics environment.

---

## 🎯 Objectives

* Monitor production throughput and efficiency
* Track defect rates and failure patterns
* Analyze sensor data to identify root causes of failures
* Simulate a real-world manufacturing data pipeline

---

## 🏭 Dataset

Source: Kaggle Predictive Maintenance Dataset

The dataset includes:

* Machine conditions (temperature, torque, speed)
* Tool wear indicators
* Failure labels and failure types

---

## 🔄 Data Transformation

### 1. Manufacturing Context Mapping

The dataset was reinterpreted to simulate a robot production line:

* `Product ID` → Robot ID
* `Machine failure` → Defective robot
* Each row → Production event

---

### 2. Assembly Stages

Production stages were introduced:

* Mechanical Assembly
* Electrical Wiring
* Final QA

This enables stage-level performance analysis.

---

### 3. Time Simulation

A synthetic timestamp column was created to simulate real-time production flow.

---

## 🧱 Data Model

### 🧾 production_events

Primary table containing all production data:

* robot_id, timestamp, assembly_stage
* sensor data (temperature, torque, etc.)
* failure indicators

---

### ❌ failure_events

Normalized table of failure types:

* failure_type (HDF, OSF, etc.)
* robot_id, timestamp

---

### 📊 production_metrics

Aggregated table for dashboards:

* total_units
* failures
* defect_rate
* avg_temperature, avg_torque
* downtime

---

## 📈 Key Metrics

* **Throughput** → Units produced over time
* **Defect Rate** → Failures / total units
* **Downtime** → Time lost due to failures
* **Cycle Time** → Time between production events
* **Failure Breakdown** → Root causes of defects

---

## 🔍 Key Insights

* Lightweight robots (L-type) have the highest defect rate (~3.9%)
* Heat Dissipation Failures (HDF) are the leading cause of defects
* Mechanical stress (OSF) is a major contributor to failures
* L-type robots contribute disproportionately to downtime

---

## ⚙️ Tech Stack

* Python (Pandas)
* SQL (data transformations)
* Dashboard: Power BI / Grafana

---

## 📊 Dashboard Features

* Factory overview with KPIs (throughput, defect rate, downtime)
* Failure analysis by type and robot model
* Time-series trends for production performance
* Station-level cycle time analysis

<img width="1236" height="698" alt="image" src="https://github.com/user-attachments/assets/763f4917-1527-4989-8350-f0f49c2a9e13" />

---

## 🚀 Future Improvements

* Real-time data streaming simulation
* Predictive failure modeling
* Alerting system for anomaly detection

---

## 🧠 Takeaway

This project demonstrates how raw operational data can be transformed into actionable insights through structured data pipelines and intuitive dashboards, reflecting real-world manufacturing analytics workflows.

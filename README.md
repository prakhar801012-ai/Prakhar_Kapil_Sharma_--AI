# 🦺 SmartPPE AI – Full Person PPE Compliance Detection System

![Python](https://img.shields.io/badge/Python-3.10-blue)
![YOLOv8](https://img.shields.io/badge/YOLOv8-Ultralytics-green)
![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-red)
![License](https://img.shields.io/badge/License-MIT-yellow)

## 📌 Overview

SmartPPE AI is an intelligent Computer Vision system designed to monitor Personal Protective Equipment (PPE) compliance in industrial environments.

The system analyzes workers in images and determines whether they are:

🟢 Fully Compliant (Full PPE Kit)

🟡 Partially Compliant (Missing PPE Items)

🔴 Non-Compliant (No PPE Detected)

Using YOLOv8 object detection and PPE association logic, SmartPPE can automatically identify workers and verify the presence of mandatory safety equipment.

---

## 🚨 Industry Problem

Industrial accidents frequently occur because workers fail to wear required PPE.

Common challenges include:

* Manual safety inspections
* Human monitoring errors
* Large workforce management
* Real-time compliance tracking
* Missing critical PPE components

Organizations require automated monitoring solutions to improve worker safety and reduce compliance violations.

---

## 🎯 Project Objective

Build an AI-powered PPE compliance detection system capable of:

* Detecting workers in images
* Detecting PPE equipment
* Mapping PPE items to individuals
* Identifying missing PPE components
* Generating compliance reports
* Visualizing safety status using color-coded bounding boxes

---

# 🏗 System Architecture

Input Image
↓
YOLOv8 Detection
↓
Person Detection
↓
PPE Detection
↓
IoU Association Engine
↓
Compliance Verification
↓
Status Classification
↓
Annotated Output + Report

---

# 🦺 Supported PPE Categories

| PPE Item      | Status |
| ------------- | ------ |
| Helmet        | ✅      |
| Safety Vest   | ✅      |
| Face Mask     | ✅      |
| Goggles       | ✅      |
| Gloves        | ✅      |
| Safety Boots  | ✅      |
| Coverall Suit | ✅      |

---

# 🧠 Compliance Logic

## FULL PPE

Worker contains:

* Helmet
* Vest
* Mask
* Goggles
* Gloves
* Boots
* Coverall

Status:

🟢 GREEN

---

## PARTIAL PPE

Worker missing one or more PPE items.

Status:

🟡 YELLOW

---

## NO PPE

No PPE items detected.

Status:

🔴 RED

---

# ⚙️ Technology Stack

| Technology   | Purpose              |
| ------------ | -------------------- |
| Python       | Core Development     |
| YOLOv8       | Object Detection     |
| OpenCV       | Image Processing     |
| NumPy        | Computation          |
| Matplotlib   | Visualization        |
| Google Colab | Training & Inference |

---

# 📂 Project Structure

SmartPPE-AI/

├── README.md

├── smartppe.py

├── requirements.txt

├── sample_images/

│ ├── worker1.jpg

│ ├── worker2.jpg

│ └── worker3.jpg

├── outputs/

│ ├── annotated_worker1.jpg

│ ├── annotated_worker2.jpg

│ └── annotated_worker3.jpg

├── assets/

│ ├── architecture.png

│ └── demo.png

└── notebooks/

└── SmartPPE_Colab.ipynb

---

# 🔍 Detection Pipeline

### Step 1

Detect all objects using YOLOv8.

### Step 2

Separate:

* Person objects
* PPE objects

### Step 3

Associate PPE items with detected workers using IoU matching.

### Step 4

Verify required PPE checklist.

### Step 5

Generate worker-level compliance report.

### Step 6

Draw compliance status on image.

---

# 📊 Sample Output

Worker 1

Present PPE:

* Helmet
* Vest
* Mask
* Gloves
* Boots
* Goggles
* Coverall

Missing PPE:

None

Status:

GREEN

---

Worker 2

Present PPE:

* Helmet
* Vest
* Gloves

Missing PPE:

* Mask
* Goggles
* Boots
* Coverall

Status:

YELLOW

---

Worker 3

Present PPE:

None

Missing PPE:

All Required PPE

Status:

RED

---

# 📈 Key Features

✅ Full PPE Compliance Detection

✅ Person-wise PPE Mapping

✅ Missing Equipment Identification

✅ Color-coded Safety Visualization

✅ Automated Compliance Reporting

✅ Google Colab Compatible

✅ Scalable for CCTV Monitoring

✅ Industrial Safety Automation

---

# 📸 Future Enhancements

### Version 2

* Video Stream Processing
* CCTV Integration
* RTSP Camera Support
* Real-Time Monitoring

### Version 3

* Custom PPE YOLO Training
* Hardhat Color Classification
* Worker Tracking
* Safety Violation Alerts

### Version 4

* Edge AI Deployment
* NVIDIA Jetson Support
* Safety Dashboard
* Cloud Analytics

---

# 📊 Evaluation Metrics

Metrics used for industrial deployment:

* Precision
* Recall
* mAP@50
* mAP@50-95
* Compliance Accuracy

---

# 🚀 Deployment Options

* Google Colab
* Local Machine
* Docker
* NVIDIA Jetson
* AWS EC2
* Azure AI Services
* GCP Vertex AI

---

# 🏭 Industrial Applications

* Construction Sites
* Oil & Gas Plants
* Chemical Industries
* Manufacturing Facilities
* Mining Operations
* Warehouses
* Smart Factories

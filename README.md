# 🚦 Smart Traffic Monitoring & e-Challan Issuance System

An AI-powered computer vision project that automatically detects motorcycle riders violating helmet rules, extracts their license plate using OCR, and issues digital challans (e-fines) with real-time SMS and email alerts. Designed for Indian roads, this system reduces human bias, increases road safety, and streamlines enforcement.

![Helmet Detection Demo](https://your-image-link-here) <!-- Optional demo image -->

---

## 🧠 Key Features

- ✅ Detects **helmetless riders** using YOLOv5 and transfer learning
- 🔍 Extracts **license plate numbers** with EasyOCR
- 💬 Sends **instant notifications** via Twilio (SMS) and Gmail (Email)
- 💳 Integrates **dummy payment system** for challan clearance (Razorpay)
- 📁 Logs violators in a local **CSV database** (replaceable with live DB)
- 📹 Compatible with **CCTV footage or live video stream**

---



## 🛠️ Tech Stack

| Component          | Technology Used          |
|-------------------|--------------------------|
| Language          | Python 3.9               |
| Object Detection  | YOLOv5 (Ultralytics)     |
| OCR               | EasyOCR                  |
| Notification      | Twilio API, SMTP Gmail   |
| Backend DB        | CSV (can be upgraded)    |
| Payment Gateway   | Razorpay (dummy setup)   |

---

## 📷 System Workflow

1. **Input**: CCTV or recorded footage of road junctions.
2. **Detection**: YOLOv5 detects motorcycles, helmets, and number plates.
3. **Violation**: If a rider is detected without a helmet, the number plate is cropped and processed.
4. **OCR**: EasyOCR extracts the plate number.
5. **Challan Generation**: System logs the violation, and sends SMS + Email to the rider.
6. **Payment (optional)**: Admin dashboard allows payment tracking and status updates.

---

## 🚀 Installation

```bash
# Clone repository
git clone https://github.com/your-username/smart-traffic-monitor.git
cd smart-traffic-monitor

# Create environment
conda create -n traffic-monitor python=3.9
conda activate traffic-monitor

# Install dependencies
pip install -r requirements.txt

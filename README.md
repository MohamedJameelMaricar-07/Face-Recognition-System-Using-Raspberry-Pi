# Face-Recognition-System-Using-Raspberry-Pi
A lightweight, real-time face recognition system implemented on Raspberry Pi using  *OpenCV*, **LBPH Face Recognizer**, and **Haar Cascade** classification. This project captures facial images, trains a recognition model, and performs real-time identification through the camera module. It is suitable for IoT-based authentication, automation, and security applications.

---
**Project Overview**

This project implements a complete face recognition pipeline on Raspberry Pi:

1. **Face Data Collection (dataset.py)**
   Captures facial images of multiple users and stores them in a structured dataset directory.

2. **Model Training (training.py)**
   Trains an LBPH face recognition model using the collected dataset.

3. **Real-Time Recognition (recognition.py)**
   Performs live face detection and recognition using the trained model.

The project uses the **LBPH (Local Binary Patterns Histogram)** algorithm, known for low computational requirements and excellent performance on embedded devices like Raspberry Pi.

---

## **Features**

* Real-time face detection and recognition
* Collect multiple users’ face samples
* LBPH-based model training
* High accuracy on Raspberry Pi Camera Module
* Lightweight and optimized for low-power devices
* Modular code (capture → train → recognize)
* Customizable for attendance systems, access control, and IoT security

---

## **Directory Structure**

```
Face-Recognition-RaspberryPi/
│── README.md
│── Images/
│── Report/
│── Reference_Code/
│      ├── dataset.py
│      ├── training.py
│      ├── recognition.py```

---

## **Hardware Requirements**

* Raspberry Pi 3 Model B / B+ / Pi 4
* Raspberry Pi Camera Module
* MicroSD Card (16GB or higher)
* 5V Power Supply
* External monitor or VNC for remote access

---

## **Software Requirements**

* Raspberry Pi OS
* Python 3.x
* OpenCV
* NumPy
* Pillow
* Haar Cascade XML (included)

Install dependencies:

```bash
pip install opencv-python numpy pillow
```

---

## **How It Works**

### **1. Capture Face Data**

Run:

```bash
python3 dataset.py
```

* Enter a numeric ID (e.g., 0,1,2…)
* System captures 30 sample images per user
* Images stored as:

```
dataset/User.<ID>.<ImageNumber>.jpg
```

---

### **2. Train the Recognition Model**

```bash
python3 training.py
```

* Reads images from `dataset/`
* Detects faces
* Trains LBPH model
* Saves model as:

```
trainer/trainer.yml
```

---

### **3. Run Real-Time Face Recognition**

```bash
python3 recognition.py
```

* Loads trained model
* Detects faces
* Displays ID and confidence
* Works live with Pi Camera

## **Model Used: LBPH**

LBPH is chosen because:

* Works well with low-resolution images
* Robust to lighting variations
* Efficient on resource-limited devices
* No GPU required

---

## **Applications**

* Smart door access
* Attendance systems
* Home security
* Lab entry monitoring
* IoT automation
* Identity-based notifications

---

## **Project Credits**


Customized and documented for academic demonstration by:
**Mohamed Jameel Maricar**
Electronics and Communication Engineering Graduate
Puducherry Technological University

---

## **Author**

**Mohamed Jameel Maricar**
GitHub: github.com/MohamedJameelMaricar-07
LinkedIn: linkedin.com/in/mohamedjameelmaricar
Email: [jameelmaricar711@gmail.com](mailto:jameelmaricar711@gmail.com)

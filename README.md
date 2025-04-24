# 🚗 Car Crash Detection & Risk Analysis System

A real-time deep learning-based system that detects car crashes, estimates vehicle speed, analyzes crash risk levels, sends emergency SOS alerts, and generates comprehensive reports. The system uses computer vision and object detection (YOLO) techniques to provide dynamic visual feedback using bounding box color changes based on risk probability.

---

## 🧠 Key Features

- 🔍 **Car Crash Detection**  
  Detects collisions in real-time using YOLO-based object detection on video feeds or uploaded videos.

- 🛣️ **Vehicle Speed Estimation**  
  Estimates the speed of detected vehicles frame-by-frame.

- ⚠️ **Crash Risk Analysis**  
  Calculates the probability of a crash occurring and updates bounding box colors:
  - 🟩 **Green** – Low Risk  
  - 🟨 **Yellow** – Moderate Risk  
  - 🟥 **Red** – High Risk  

- 🆘 **SOS Emergency Alert System**  
  Automatically sends SOS alerts with crash data (e.g., time, location, risk level) to emergency contacts when a high-risk crash is detected.

- 📊 **Automated Report Generation**  
  Generates detailed reports summarizing:
  - Number of vehicles detected  
  - Time and location of crashes (if available)  
  - Risk scores  
  - Vehicle speed history  

- 🎥 **Video Input Support**  
  Accepts video files or live camera feeds for analysis.

---
🖼️ Screenshots & Demo
Car Crash Detection in Action
Here is a screenshot of the car crash detection in action:

Report:
![Image With accident](image-1.png)
![Image Wihtout accident](image-2.png)
![Report](image.png)
![SOS Message](1.jpg)
![SOS Email](email.jpg)

## 🛠️ Tech Stack

- **YOLOv8** – Object detection for car and crash detection  
- **OpenCV** – Video processing and visualization  
- **Python** – Backend logic and report generation  
- **Pandas** – Data handling and analytics  
- **Matplotlib / Seaborn** – Graphs  
- **SMTP / Twilio API** – For SOS alerts via email/SMS  

---
## 📁 Project Structure

```bash
├── Runs/                          # YOLO training outputs
├── MEDIUM/                        # YOLOV8M trained output
├── NONO/                          # YOLOV8N trained output
├── train/                         # YOLOv8 training notebooks
│   ├── yolov8m_train.ipynb        
│   ├── yolov8m_2_train.ipynb      
│   └── yolov8n_train.IPYNB        
├── video_final/                   # Sample crash videos
│   ├── Crash_1.mp4
│   ├── Crash_2.mp4
│   └── ...
├── detection_report.csv           # Auto-generated report
├── output_crash_detection.mp4     # Final processed video with bounding boxes
├── main.ipynb                     # Main code for detection and analysis
├── .gitignore                     # Git ignore config
└── requirements.txt               # Dependencies 

How to Run
1. Clone the Repository
git clone https://github.com/khushipatel27/car-crash-detection.git
cd car-crash-detection

2. Install Dependencies Make sure you have Python installed. Then run:
pip install -r requirements.txt

3.Run the Main Script Launch the detection system:
jupyter notebook main.ipynb

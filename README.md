🚗 Driver Drowsiness Detection Using MobileNetV3

A lightweight deep-learning–based system that detects driver fatigue in real time using MobileNetV3, helping prevent accidents caused by drowsy driving.

📌 Overview

Driver drowsiness is one of the major causes of road accidents globally. This project presents a real-time driver drowsiness detection system using the MobileNetV3 deep learning architecture. The model analyzes the driver’s facial features—primarily eye states and facial behavior—to determine whether the driver is awake or drowsy.

Designed for portability and speed, MobileNetV3 ensures the system runs efficiently on:

Mobile devices

Laptops

Low-power embedded platforms (Raspberry Pi, Jetson Nano)

If drowsiness is detected for a continuous duration, the system triggers a visual and audio alert to prevent potential accidents.

🎯 Features

⚡ Real-time detection with high accuracy

🧠 MobileNetV3-based lightweight deep learning model

👁️ Detects eye closure, blinking frequency, yawning, and head posture

📱 Works on mobile/edge devices due to low computational cost

🔊 Automatic alarm alert when drowsiness is detected

🚘 Suitable for intelligent transportation systems and ADAS

🏗️ Project Architecture
Camera Input → Face Detection → ROI Extraction (Eyes/Face)  
              → MobileNetV3 Classification  
              → “Awake / Drowsy” Prediction  
              → Alert System (Audio/Visual)

📂 Project Structure
├── app.py                 # Streamlit or main application file
├── model/
│   ├── mobilenetv3.h5     # Trained MobileNetV3 model
├── utils/
│   ├── detector.py        # Face/Eye detection logic
│   ├── preprocessing.py   # Image preprocessing functions
├── requirements.txt       # Python dependencies
├── README.md              # Project documentation
└── samples/               # Test images/videos

📦 Requirements

Install the required Python libraries:

pip install -r requirements.txt


Typical dependencies include:

TensorFlow / Keras

OpenCV

NumPy

Streamlit

imutils

▶️ How to Run the Project
1. Create and activate virtual environment
python -m venv venv
venv\Scripts\activate  # Windows

2. Install Dependencies
pip install -r requirements.txt

3. Run the Application

For Streamlit app:

streamlit run app.py


For OpenCV-based script:

python app.py

📷 Working Demo

The system performs:

Face detection

Eye state classification (open/closed)

Yawn detection

Real-time alert generation

🧠 Model Details — MobileNetV3

Efficient architecture optimized for real-time inference

Uses depthwise separable convolutions

Includes Squeeze-and-Excitation (SE) blocks

Works well in low-light or partial face visibility

Suitable for edge & mobile applications

🚨 Alert Mechanism

If the driver’s eyes remain closed for a threshold duration (e.g., >2 seconds):

🔔 An alert sound is played

⚠️ A warning message is displayed on screen

This helps prevent accidents caused by micro-sleep or fatigue.

🌟 Applications

Intelligent vehicles

Fleet management

Highway transportation systems

Driver monitoring for trucks/buses

Automobile safety research

🚀 Future Enhancements

Integration with IoT sensors

Multi-class emotion detection

Night-time IR camera support

Integration with cloud driving analytics

Deployment on mobile as an Android/iOS app

🤝 Contributions

Contributions, pull requests, and bug reports are welcome!

📜 License

MIT License — free to modify and use for academic or research purposes.

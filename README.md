
# 🎓 Dolaveen – A Secret Eye

A real-time AI powered proctoring system built with Flask, OpenCV, and multiple detection modules. This tool monitors students during online exams and detects suspicious behavior such as looking away, unauthorized objects, multiple faces, and speaking.

---

## 🚀 Features

- 🔍 Eye Tracker — Detects if the user’s gaze deviates from the screen.
- 🙆 Head Detector — Monitors head movement direction.
- 🧑‍🤝‍🧑 Face Verifier — Checks for unauthorized additional faces.
- 🎤 Audio Detector — Flags background or user speech.
- 📦 Object Detector — Detects non-allowed physical objects.
- 📷 Webcam Integration — Captures live feed using OpenCV.
- 📝 PDF Report Generator — Creates session summary in downloadable format.
- ☁️ MongoDB Logging — Stores session logs and evidence.
- 🔐 Secure Upload — Upload and store verification media safely.
- 🖥️ Live Surveillance View — Continuous camera streaming.

---

## 🧠 Architecture Overview

Frontend (HTML + Flask templates)

Flask Server (app.py)

    +--> EyeTracker (eye_tracker.py)
    +--> HeadDetector (head_detector.py)
    +--> FaceVerifier (faceverifier.py)
    +--> AudioDetector (audio_detector.py)
    +--> ObjectDetector (object_detector.py)

MongoDB (Logging events, timestamps, violations)

---

## 📁 Project Structure

```bash
your_project/

├── app.py                    # Main Flask application
├── eye_tracker.py            # Eye tracking logic
├── head_detector.py          # Head movement detection
├── faceverifier.py           # Face verification logic
├── audio_detector.py         # Speech detection
├── object_detector.py        # Object detection model
├── templates/                # HTML templates
├── static/                   # CSS, JS, images
├── uploads/                  # Uploaded reference images/videos
└── requirements.txt          # Python dependencies
````

---

## ⚙️ How It Works

### 1. Launch Flask App

```bash
python app.py
```

Visit:

```bash
http://localhost:5001
```

### 2. Upload User Data

* Provide student name, ID, and a reference face image before starting the exam.

### 3. Start Surveillance

* System captures webcam feed.
* Runs detection models in real-time using parallel threads.
* Logs suspicious events such as:

  * Multiple faces detected
  * Looking away
  * Talking
  * Unauthorized object detection

### 4. Report Generation

* After session completion, a PDF report is generated.
* Includes:

  * Timestamps
  * Violation types
  * Optional screenshots

---

## 🧪 Example Use Case

1. Student logs in and uploads ID + face image.
2. Invigilator starts the monitoring session.
3. AI models continuously analyze candidate behavior.
4. Violations are logged automatically.
5. Final report is generated and downloaded.

---

## 📦 Installation

### Clone Repository

```bash
git clone https://github.com/Mprince29/Intelligent-Proctoring-Detection-Framework.git

cd Intelligent-Proctoring-Detection-Framework
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Start Server

```bash
python app.py
```

---

## 📋 Dependencies

* Flask
* OpenCV (cv2)
* reportlab
* numpy
* pymongo
* werkzeug
* face_recognition
* SpeechRecognition
* Custom AI detection modules

---

## 🛡️ Security Notes

* Use HTTPS for secure webcam access in production.
* Store secrets using environment variables.
* Validate uploaded files before processing.
* Restrict unauthorized media access.

---

## 🧰 Tips for Developers

* Models are globally initialized for faster execution.
* Multi-threading is used for parallel real-time analysis.
* MongoDB stores logs, timestamps, and metadata.
* Uploaded files are stored inside the `uploads/` directory.

---

## 📄 Example Report Output

* Timestamped list of all violations
* Session duration
* Student metadata
* Captured snapshots during suspicious activity
* Downloadable PDF summary

---

## 🚀 Future Improvements

* AI-based emotion analysis
* Cloud deployment support
* Admin analytics dashboard
* Real-time alerts and notifications

---

## 👨‍💻 Author

Developed by **Dolendra**

```
```

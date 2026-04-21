# 🎨 White-Box Cartoonization Web App

A deep learning–based web application that converts images and videos into cartoon-style outputs using a **White-Box Cartoonization GAN**. Built with **TensorFlow 2.x**, exposed via a **Flask API**, and designed for scalable media processing using **FFmpeg** and **Google Cloud Storage**.

---

## 🚀 Features

* Image cartoonization using GAN model
* Video cartoonization via frame-wise processing (FFmpeg)
* REST API built with Flask
* Asynchronous processing pipeline
* Google Cloud Storage integration
* Docker support for deployment

---

## 🏗️ Project Structure

```
.
├── static/                 # Static files (CSS, JS, assets)
├── templates/              # HTML templates
├── white_box_cartoonizer/  # Core model and inference logic
├── app.py                  # Flask app entry point
├── video_api.py            # Video processing pipeline
├── gcloud_utils.py         # GCP integration
├── config.yaml             # App configuration
├── Dockerfile              # Container setup
├── requirements.txt        # Dependencies
└── .github/workflows/      # CI/CD (if configured)
```

---

## ⚙️ Tech Stack

* **Backend:** Flask
* **ML Framework:** TensorFlow 2.x
* **Model:** White-Box Cartoonization GAN
* **Video Processing:** FFmpeg
* **Cloud:** Google Cloud Storage
* **Containerization:** Docker

---

## 🧪 Requirements

* Python 3.7
* TensorFlow 2.1.0
* tf_slim 1.1.0
* FFmpeg 3.4.8
* CUDA 10.1 (for GPU acceleration)
* Ubuntu 18.04 (recommended)

---

## 🛠️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/harshals01/white-box-cartoonization-web-app.git
cd white-box-cartoonization-web-app
```

### 2. Create virtual environment

```bash
virtualenv -p python3 cartoonize
source cartoonize/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure application

Update values in:

```
config.yaml
```

(Add paths, model configs, and GCP credentials if used)

---

## ▶️ Run the App

```bash
python app.py
```

Open in browser:

```
http://127.0.0.1:5000/
```

---

## 🐳 Docker (Optional)

```bash
docker build -t cartoonizer .
docker run -p 5000:5000 cartoonizer
```

---

## 🔄 Processing Flow

1. Upload image/video
2. Preprocessing
3. GAN inference (cartoonization)
4. Video encoding (FFmpeg)
5. Output stored locally / on GCP
6. Result returned via API

---

## 📡 API Endpoints

| Endpoint   | Method | Description          |
| ---------- | ------ | -------------------- |
| `/`        | GET    | Home page            |
| `/predict` | POST   | Image cartoonization |
| `/video`   | POST   | Video cartoonization |

---

## ⚠️ Notes

* GPU recommended for faster inference
* Video processing is computationally expensive
* TensorFlow version is legacy (2.1.0)

---

## 🔮 Improvements

* Upgrade TensorFlow / migrate to PyTorch
* Add batch processing for GPU efficiency
* Introduce async task queue (Celery/Redis)
* Improve frontend UI
* Optimize video pipeline

---


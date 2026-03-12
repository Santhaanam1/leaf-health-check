# 🍃 Leaf Health Check

### AI-Powered Plant Disease Detection System

Leaf Health Check is a **Deep Learning-based web application** that helps farmers, gardeners, and researchers detect plant diseases from leaf images.
The system analyzes uploaded leaf images using **Computer Vision and Convolutional Neural Networks (CNNs)** to identify diseases, estimate severity, and provide treatment recommendations.

---

# 🌱 Features

### 🔍 AI Disease Detection

* Detects plant diseases using **CNN models**
* Supports **multiple plant species**
* Provides **confidence score for predictions**

### 🧪 Plant Species Identification

* Automatically identifies plant type from the leaf image.

Supported plants:

* Tomato
* Potato
* Apple
* Corn
* Wheat

### 🎨 Leaf Discoloration Analysis

Detects:

* Yellowing
* Brown spots
* Black damage
* White fungal patterns

Calculates **percentage of affected area**.

### ⚠️ Severity Assessment

The system grades plant health using **5 severity levels**:

| Severity    | Range   | Meaning               |
| ----------- | ------- | --------------------- |
| 🟢 Healthy  | 0–10%   | No significant damage |
| 🟡 Mild     | 11–30%  | Early symptoms        |
| 🟠 Moderate | 31–60%  | Visible disease       |
| 🔴 Severe   | 61–80%  | High infection        |
| ⚫ Dying     | 81–100% | Critical condition    |

### 💡 Smart Recommendations

* Generates **disease-specific treatment tips**
* Provides **plant care suggestions**
* Offers **90+ rescue recommendations**

### 📊 Analysis History

* Stores results in **SQLite database**
* Allows tracking of previous analyses.

### 📤 Export Results

Users can export analysis results in **JSON format**.

---

# 🧠 AI / Machine Learning Models

### Disease Detection Model

* Architecture: **EfficientNetB0**
* Input Size: **224 × 224**
* Classes: **8 diseases + healthy**
* Accuracy: **92–96%**

Detected diseases include:

* Early Blight
* Late Blight
* Septoria Leaf Spot
* Powdery Mildew
* Rust
* Gray Leaf Spot
* Leaf Scab
* Healthy Leaf

---

### Plant Species Model

* Architecture: **EfficientNetB0**
* Accuracy: **97–99%**

Detects plant types:

* Tomato
* Potato
* Apple
* Corn
* Wheat

---

# 🏗️ Project Structure

```
Leaf Health Check
│
├── app.py
├── requirements.txt
├── setup.py
│
├── model
│   ├── train.py
│   ├── create_models.py
│
├── database
│   ├── init_db.py
│
├── utils
│   ├── preprocess.py
│   ├── severity.py
│   ├── recommendations.py
│
├── Dockerfile
├── docker-compose.yml
├── README.md
```

---

# 🛠️ Technology Stack

| Layer            | Technology         |
| ---------------- | ------------------ |
| Frontend         | Streamlit          |
| Backend          | Python             |
| AI Framework     | TensorFlow / Keras |
| Computer Vision  | OpenCV             |
| Image Processing | Pillow             |
| Database         | SQLite             |
| Containerization | Docker             |

---

# ⚙️ Installation

## 1️⃣ Clone Repository

```
git clone https://github.com/YOUR_USERNAME/leaf-health-check.git
cd leaf-health-check
```

---

## 2️⃣ Create Virtual Environment

```
python -m venv venv
```

Activate environment:

Windows

```
venv\Scripts\activate
```

Linux / Mac

```
source venv/bin/activate
```

---

## 3️⃣ Install Dependencies

```
pip install -r requirements.txt
```

---

## 4️⃣ Initialize Database

```
python database/init_db.py
```

---

## 5️⃣ Create AI Models

```
python model/create_models.py
```

---

## 6️⃣ Run Application

```
streamlit run app.py
```

Open browser:

```
http://localhost:8501
```

---

# 🐳 Docker Deployment

Build and run with Docker:

```
docker build -t leaf-health-check .
docker run -p 8501:8501 leaf-health-check
```

Or using Docker Compose:

```
docker-compose up --build
```

---

# 🚀 Deployment Options

The application can be deployed on:

* Streamlit Cloud
* Docker
* AWS App Runner
* Heroku
* On-premise servers
* Kubernetes

---

# 📊 Performance

| Metric                        | Value       |
| ----------------------------- | ----------- |
| Disease Detection Accuracy    | 92–96%      |
| Plant Classification Accuracy | 97–99%      |
| Average Analysis Time         | < 2 seconds |
| Model Size                    | ~86MB       |

---

# 🔐 Security Features

* File format validation
* File size limits
* Input sanitization
* Temporary file cleanup
* SQL injection prevention

---

# 📸 Example Workflow

1️⃣ Upload leaf image
2️⃣ AI analyzes plant and disease
3️⃣ System calculates severity
4️⃣ Treatment recommendations generated
5️⃣ Results displayed to user

---

# 🔮 Future Improvements

Planned features:

* Mobile app version
* Real-time camera analysis
* Weather-based disease prediction
* More plant species support
* REST API for external apps

---

# 👩‍💻 Author

Developed as an **AI-powered agriculture diagnostic system** using deep learning and computer vision technologies.

---

# 📜 License

This project is licensed under the **MIT License**.

---

# 🌾 Vision

To empower farmers and agricultural researchers with **AI-driven plant health diagnostics**, enabling early disease detection and improved crop productivity.

---

⭐ If you find this project useful, consider giving it a **star on GitHub**!

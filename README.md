# 🌾 CropMonitor AI — Smart Farming Dashboard

## ✨ Highlights

* 🤖 **Krishi Mitra — Smart Farmer Assistant**
  An AI-powered chatbot that helps farmers with questions related to crop health, irrigation, pest/disease issues, sensor values, and using the dashboard.

* 🗣️ **Multilingual Interaction**
  Farmers can select from multiple regional languages such as Hindi, Punjabi, Tamil, Telugu, Marathi, Bengali, Urdu, and others. A custom language can also be entered when required.

* 🧩 **Built-In Demo Mode**
  The application can run even without an API key, using predefined responses so the dashboard remains functional during demonstrations and deployment.

* ⚡ **Optional Gemini AI Integration**
  Adding a Gemini API key enables live AI-generated responses and multilingual chatbot interaction.

---

## 📁 Project Structure

```text
CropMonitor/
│
├── app.py
├── requirements.txt
└── .streamlit/
    └── secrets.toml.example
```

* `app.py` — Main Streamlit application
* `requirements.txt` — Required Python packages
* `secrets.toml.example` — Example configuration for securely adding the Gemini API key

---

## 🚀 Deploy on Streamlit Cloud

### 1. Upload the project to GitHub

Create a repository or add these files to your existing CropMonitor repository.

Make sure `app.py` and `requirements.txt` are accessible from the location you specify during deployment.

### 2. Create the Streamlit application

Open Streamlit Cloud, sign in using GitHub, and choose **Create app**.

### 3. Configure the repository

Select:

* GitHub repository
* Branch
* Main file: `app.py`

### 4. Add the Gemini API key

Under **Advanced Settings → Secrets**, add:

```toml
GEMINI_API_KEY = "your_actual_key"
```

A Gemini API key can be generated through Google AI Studio.

> If no key is provided, the application automatically falls back to Demo Mode.

### 5. Launch

Click **Deploy**.

After deployment, Streamlit will provide a public `.streamlit.app` address for the dashboard.

---

## 💻 Run the Project Locally

Install the dependencies:

```bash
pip install -r requirements.txt
```

Then start the dashboard:

```bash
streamlit run app.py
```

---

## 🔌 Current Hardware Integration

At the moment, the dashboard uses **simulated sensor readings** for demonstration purposes.

The **"Simulate new sensor reading"** option generates updated values inside the Streamlit interface, allowing the monitoring and irrigation features to be demonstrated without a physical ESP32 connection.

### 🔧 Planned Live IoT Setup

For real-time hardware communication:

```text
ESP32
   ↓
Sensors
   ↓
Backend API
   ↓
Streamlit Dashboard
```

The ESP32 can send its sensor readings to a small backend service, while the Streamlit dashboard retrieves and displays the latest information.

---

## 🧠 AI Capabilities

When the Gemini API key is configured, CropMonitor can provide:

* 🌿 Crop image analysis
* 🐞 Disease and pest identification
* 💬 AI-based farmer assistance
* 🗺️ Multilingual responses
* 💧 Irrigation-related guidance
* 📊 Interpretation of sensor readings

Without an API key, the application continues to operate in **Demo Mode** using predefined responses.

---

## 🎯 Project Objective

CropMonitor aims to bring **crop health monitoring, AI assistance, sensor-based insights, and smart irrigation into one accessible platform**, helping farmers understand crop conditions and take timely decisions.

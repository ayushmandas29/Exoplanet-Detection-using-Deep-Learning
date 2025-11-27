# 🪐 Exoplanet Detection using Deep Learning (NASA Kepler Light Curves)

### 🔭 Real-time AI system to detect exoplanets from telescope data using a 1D-CNN model and Streamlit web app

![Python](https://img.shields.io/badge/Python-3.10-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![Streamlit](https://img.shields.io/badge/Streamlit-Web%20App-red)
![NASA](https://img.shields.io/badge/NASA-Kepler%20Data-black)
![Deep Learning](https://img.shields.io/badge/Deep%20Learning-CNN-green)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 🚀 Project Overview

This project uses **NASA Kepler space telescope light-curve data** to detect whether a star contains an **exoplanet** (a planet outside our solar system).
A **1D Convolutional Neural Network (1D-CNN)** is trained on time-series flux data and deployed as an interactive **Streamlit web app**.

📌 Upload a 1-row `.csv` containing brightness (flux) values  
📌 The app plots the light curve and predicts **Exoplanet / No Exoplanet** with a **probability score**

---

## 🌟 Highlights & Features

- Uses **real NASA Kepler light-curve data**
- 1D-CNN model achieves **high performance**
- **Streamlit app** for real-time predictions
- Clean, modular, and **easy to reproduce**
- Completely **open-source and beginner friendly**

---

## 📂 Repository Structure

.
├─ exoplanet_app.py # Streamlit web app
├─ best_model.keras # Trained DL model
├─ Exoplanet_Detection_using_Deep_Learning.ipynb # Training notebook
├─ sample_lightcurve.csv # Example input
├─ requirements.txt # Dependencies
└─ README.md

yaml
Copy code

---

## ▶️ Run Locally

```bash
git clone https://github.com/ayushmandas29/Exoplanet-Detection-using-Deep-Learning.git
cd Exoplanet-Detection-using-Deep-Learning
pip install -r requirements.txt
streamlit run exoplanet_app.py
Then open the link generated in terminal (usually http://localhost:8501)

📥 Input Format (VERY IMPORTANT)
The app expects a CSV with:

One row only

Only numeric flux values — no header

Example format:

Copy code
0.032, 0.031, 0.028, 0.021, 0.019, -0.002, -0.054, -0.049, ...
❌ Do NOT upload the full Kepler dataset
✔ Upload only one light curve per file

🛰 Dataset Info
Dataset: Exoplanet Hunting in Deep Space

Telescope: NASA Kepler

Format: Flux time-series data labelled as {exoplanet / no exoplanet}

Kaggle Source (Official):
🔗 https://www.kaggle.com/datasets/keplersmachines/exoplanet-hunting-in-deep-space

🧠 Model Architecture (1D-CNN)
scss
Copy code
Input → Conv1D → MaxPool →
        Conv1D → MaxPool →
        Conv1D → MaxPool →
        Flatten → Dense(128) + Dropout → Dense(1, Sigmoid)
Loss: binary_crossentropy

Optimizer: Adam

Output: 0 → No Exoplanet | 1 → Exoplanet Candidate

💡 Future Improvements
Try Transformers / LSTM for time-series

Explainability: highlight transit region in prediction

Support multi-planet systems

Deploy as API + dashboard

👤 Author
Ayushman Das
AI & Machine Learning Enthusiast | Space & Astronomy Lover 🚀

⭐ If you find this project useful, please consider giving it a star on GitHub!

# 🚨 Anomaly Detection in Network Traffic using Unsupervised Learning

This project leverages **unsupervised machine learning techniques**, specifically **Autoencoders**  to detect anomalous patterns in network traffic data. These anomalies may indicate potential **security breaches**, **intrusions**, or **system malfunctions**.

---

## 📌 Objective

To develop and evaluate models that can identify unusual behaviors in network traffic without requiring labeled data, making it suitable for real-world, large-scale deployment in cybersecurity or system monitoring.

---

## 🧠 Techniques Used

- **Autoencoders** (Neural Network-based):
  - Learn to compress and reconstruct "normal" network behavior.
  - High reconstruction error = potential anomaly.

---

## 🗂 Dataset

- The dataset contains **network traffic records** with features such as:
  - Source/Destination IP, Port
  - Protocol
  - Packet Size
  - Duration
  - Flags, etc.

---

## 📈 Model Architecture (Autoencoder)

- **Input Layer** → `Dense(128, ReLU)` → `BatchNorm` → `Dropout`
- `Dense(64, ReLU)` → `Dense(encoding_dim)`
- Decoder is a mirror of encoder
- Output: Reconstruct original input
- Loss: `MSE` | Optimizer: `Adam`

---

## 🚀 How to Run

1. Install dependencies:
   ```bash
   pip install -r requirements.txt

## 🚀 Hun Code

1. Install dependencies:
   ```bash
   jupyter notebook FinalCode.ipynb

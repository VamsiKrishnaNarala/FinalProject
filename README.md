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

## 📊 Dataset: KDD Cup 1999

**Source:** [Kaggle - galaxyh/kdd-cup-1999-data](https://www.kaggle.com/datasets/galaxyh/kdd-cup-1999-data)

- Records ~4.9 million connections with 41 features:
  - Duration, Protocol type, Service, Flag, Src bytes, Dst bytes, etc.
- Each record is labeled as:
  - `normal`
  - or one of 22 types of attacks (e.g., DoS, R2L, U2R, Probe)
- We use **only the features** for unsupervised learning (i.e., without labels during training).

---

## 📈 Model Architecture (Autoencoder)

- **Input Layer** → `Dense(128, ReLU)` → `BatchNorm` → `Dropout`
- `Dense(64, ReLU)` → `Dense(encoding_dim)`
- Decoder is a mirror of encoder
- Output: Reconstruct original input
- Loss: `MSE` | Optimizer: `Adam`


# 🩺 DermAI — Multimodal Skin Disease Detection System

> **Two AI Models. One Intelligent Diagnostic Assistant.**

DermAI is an advanced multimodal deep learning framework designed for automated skin disease detection. By combining visual analysis of skin images with symptom-based text understanding, the system delivers more reliable and accurate predictions than traditional single-modal approaches.

---

## 🚀 Overview

DermAI integrates two state-of-the-art AI models:

- 📸 **EfficientNetB0** for skin image classification
- 🧠 **BioBERT** for symptom text understanding
- ⚡ **Weighted Fusion Engine** for final disease prediction

This multimodal approach enables the system to leverage both visual and clinical symptom information, improving diagnostic confidence and overall performance.

---

## 🏗️ Model Architecture

| Stage | Model | Input | Output |
|---------|---------|---------|---------|
| Image Analysis | EfficientNetB0 (TensorFlow) | Skin Image | Disease Probabilities |
| Symptom Analysis | BioBERT (PyTorch) | Symptom Text | Disease Probabilities |
| Fusion Layer | Weighted Soft Voting | Image + Text | Final Prediction |

---

## 🔬 How It Works

```text
Image Input ──► EfficientNetB0 ──► Image Probabilities
                                     │
                                     ▼
                               Fusion Engine
                                     ▲
                                     │
Text Input ───► BioBERT ─────────► Text Probabilities
```

### Fusion Strategy

```text
Final Prediction = (0.65 × Image Prediction)
                 + (0.35 × Text Prediction)
```

✅ If symptom text is not provided, DermAI automatically performs image-only prediction using EfficientNetB0.

---

## ⚙️ Quick Start

### 1️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 2️⃣ Setup Datasets

```bash
python setup_datasets.py
```

### 3️⃣ Train Image Classification Model

```bash
python train_model.py
```

Generated Files:

```text
skin_disease_model.h5
class_names.json
disease_info.json
ood_threshold.json
```

### 4️⃣ Download Symptom Dataset

📥 Download the Disease Symptom Dataset from Kaggle.

### 5️⃣ Train BioBERT Model

```bash
python train_text_model.py
```

### 6️⃣ Run Application

```bash
python app.py
```

Open your browser and visit:

```text
http://localhost:5000
```

---

## 📂 Project Structure

```text
DermAI/
│
├── app.py
├── train_model.py
├── train_text_model.py
├── setup_datasets.py
├── requirements.txt
│
├── templates/
│   └── index.html
│
├── dataset/
└── model/
```

---

## 🛠️ Technology Stack

- 🐍 Python
- 🌐 Flask
- 📸 EfficientNetB0
- 🧠 BioBERT
- 🔥 TensorFlow
- ⚡ PyTorch
- 🤗 Hugging Face Transformers

---

## ✨ Key Features

- 🔍 Automated skin disease classification from images
- 📝 Symptom-aware diagnosis using BioBERT
- 🧠 Multimodal AI-powered prediction system
- ⚡ Weighted soft-voting fusion mechanism
- 📊 Confidence threshold-based prediction filtering
- 🌐 Interactive Flask web application
- 🚀 Fast and scalable inference pipeline

---

## 👨‍💻 Development Team

**Hafiz Muhammad Anas**  
**Zohaib Shafiq**  
**Muhammad Umar**

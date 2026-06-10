
****DermAI — Multimodal Skin Disease Detection****

**Two AI models. One intelligent diagnosis system.**

**Overview**
DermAI is a multimodal deep learning system for skin disease detection that combines image analysis and symptom text understanding to improve diagnostic accuracy.

It uses:
- EfficientNetB0 for image classification
- BioBERT for symptom text analysis
- Weighted fusion model for final prediction

**Model Architecture**
Layer | Model | Input | Output
1 | EfficientNetB0 (TensorFlow) | Skin Image | Disease probabilities
2 | BioBERT (PyTorch) | Symptom Text | Disease probabilities
Fusion | Weighted Soft Voting (0.65 + 0.35) | Image + Text | Final Prediction

**How It Works**
Image Input -> EfficientNetB0 -> Image Probabilities
Text Input -> BioBERT -> Text Probabilities

Final Prediction = 0.65 * Image + 0.35 * Text

If no text is provided, only image model is used.

**Quick Start**

1. Install dependencies
pip install -r requirements.txt

2. Setup datasets
python setup_datasets.py

3. Train image model
python train_model.py

Outputs:
- skin_disease_model.h5
- class_names.json
- disease_info.json
- ood_threshold.json

4. Download text dataset
Kaggle: disease symptom dataset

5. Train BioBERT model
python train_text_model.py

6. Run app
python app.py
Open http://localhost:5000

Project Structure
DermAI/
- app.py
- train_model.py
- train_text_model.py
- setup_datasets.py
- requirements.txt
- templates/index.html
- dataset/
- model/

Tech Stack
- Flask
- EfficientNetB0
- BioBERT
- TensorFlow
- PyTorch
- HuggingFace

**Developer:**
Hafiz Muhammad Anas, Zohaib Shafiq, Muhammad Umar

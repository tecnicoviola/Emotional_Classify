# Emotional_Classify
# GoEmotions Multi-Label Text Classification

## 🔍 Dataset Used
- **GoEmotions** from Google Research
- Source: [https://huggingface.co/datasets/google-research-datasets/go_emotions](https://huggingface.co/datasets/google-research-datasets/go_emotions)
- Multi-label emotion classification with 28 emotion labels + neutral

## 🧠 Approach Summary
- Utilized Hugging Face Transformers and Datasets library
- Used `bert-base-uncased` model with a classification head
- Applied light preprocessing (tokenization)
- Fine-tuned on the GoEmotions dataset for multi-label classification
- Evaluated using precision, recall, F1-score

## 🧪 Model
- Architecture: BERT + Sigmoid output layer
- Loss Function: Binary Cross-Entropy
- Evaluation: `sklearn` metrics

## 💡 Key Features
- Hugging Face `Trainer` API used for efficient training
- Handles multiple emotion labels per sentence
- Can be easily extended or deployed with Streamlit/Gradio

## 🛠️ Dependencies
```bash
pip install -r requirements.txt

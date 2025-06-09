# 🎭 GoEmotions Multi-Label Emotion Classifier

This project fine-tunes a BERT model (`bert-base-uncased`) to perform **multi-label emotion classification** using the [GoEmotions dataset](https://huggingface.co/datasets/google-research-datasets/go_emotions) from Google Research.

---

## 📂 Dataset Used

- **Name**: GoEmotions
- **Source**: [Hugging Face Datasets](https://huggingface.co/datasets/google-research-datasets/go_emotions)
- **Type**: Multi-label classification
- **Labels**: 28 emotion categories + neutral (e.g., *joy*, *anger*, *disappointment*, *love*, *fear*, etc.)
- **Size**: ~58k English Reddit comments annotated for emotion

---

## 🧠 Approach Summary

### 🔧 Preprocessing
- Used Hugging Face `datasets` to load and preprocess
- Applied `bert-base-uncased` tokenizer
- Truncated and padded sequences

### 🤖 Model
- Pretrained `bert-base-uncased` as base
- Classification head with 28 sigmoid-activated outputs
- Problem type: `multi_label_classification`

### 🧪 Training & Evaluation
- Trainer API used for training loop and evaluation
- Evaluation metrics: `Precision`, `Recall`, and `F1-Score` (micro average)
- Subsampled data for quick training demo (~1000 train, ~500 validation)

---

## 🛠️ Dependencies

Install all dependencies using:

```bash
pip install -r requirements.txt


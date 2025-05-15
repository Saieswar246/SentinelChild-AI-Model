# 🛡️ SentinelChild Child Grooming Detection System

This project is a **machine learning-based system** to detect online grooming behavior in chat conversations. It uses **SBERT (Sentence-BERT)** for text embeddings and **Logistic Regression** as the classifier. The model is trained on the full **PAN12 Sexual Predator Identification dataset**.

---

## 📌 Features

- 🔍 Detects grooming vs non-grooming conversations
- 💬 Trained on PAN12 predator dataset (XML format)
- 🧠 SBERT (`all-MiniLM-L6-v2`) for sentence embedding
- 📈 Model performance evaluated via:
  - Confusion Matrix
  - ROC Curve (AUC ~0.99)
  - Precision-Recall Curve
- 💾 Model saving and fast inference pipeline
- 🧪 Sample predictions included for testing

---

## 🧠 Algorithm

- **Algorithm**: Logistic Regression (with class weighting)
- **Embedding**: SBERT (`all-MiniLM-L6-v2`)
- **Training**: 80/20 Train-Test Split + 5-Fold Cross-Validation
- **Balancing**: Class weight = `balanced`
- **Evaluation Metrics**: F1 Score, Accuracy, ROC-AUC, Average Precision

---

## 📂 Project Structure

```bash
.
├── grooming_detection_models/
│   ├── classifier.pkl
│   └── sbert_model/
├── pan12-sexual-predator-identification-training-corpus.xml
├── pan12-sexual-predator-identification-training-corpus-predators.txt
├── sentinelchild.ipynb
└── README.md

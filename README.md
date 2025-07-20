# 🧠 BERT Question Answering Fine-Tuning

## 📌 Objective
Fine-tune a BERT-based model on the Stanford Question Answering Dataset (SQuAD) to accurately extract answers from short context passages.

## 📂 Dataset
The dataset used is the SQuAD v1.1, which contains context-question-answer triples. For efficiency, only samples with context lengths under 300 characters were used.

## 🛠️ Tools Used
`Python`, `Transformers`, `Datasets`, `PyTorch`, `Pandas`, `Matplotlib`, `Hugging Face`, `Scikit-learn`

## 🧪 Approach
1. **Data Loading and Preprocessing**:
   - Filtered short-context samples for faster training.
   - Tokenized inputs with offset mappings for answer span detection.

2. **Model Setup and Training**:
   - Used `bert-large-uncased-whole-word-masking-finetuned-squad` as the base model.
   - Applied Hugging Face's `Trainer` API for fine-tuning.

3. **Evaluation and Predictions**:
   - Selected 20 validation samples for manual evaluation.
   - Compared predicted answers with ground truth using a custom word-overlap similarity metric.


## 📈 Results
- The model achieved **100% match** on most samples, showing strong performance on short-context QA tasks.
- A few samples had partial or incorrect predictions, often due to ambiguous or complex phrasing.
- Overall, the model demonstrated high accuracy and robustness in extracting relevant answers.

## 🤓 What I Learned
- Fine-tuning BERT on domain-specific QA tasks can yield highly accurate results with minimal data preprocessing.
- Custom evaluation metrics help uncover nuanced model behavior beyond standard accuracy.
- Hugging Face's ecosystem simplifies the end-to-end pipeline from data loading to model deployment.

## 📁 Repo Contents
- `notebooks/` – Question-Answering Fine Tuning notebook.

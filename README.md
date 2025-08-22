# text_summarization.ipynb

This project applies a pretrained **BART model** (`facebook/bart-base`) from Hugging Face to perform **abstractive text summarization**.
The goal is to automatically generate concise summaries of input passages, demonstrating state-of-the-art NLP with transformer-based models.

---

## 🔹 Motivation
Summarization is a critical NLP task with real-world applications in news aggregation, legal documents, research papers, and customer support.
This project demonstrates how modern transformer models like BART can produce human-like summaries out-of-the-box with Hugging Face.

---

## 🔹 Dataset
- Source: **DeepLearning.AI**.
- Format: JSON files (`train.json`) and (`test.json`) with the following structure:
- `dialogue`: original passage
- `summary`: human-written reference summary


Example:
```json
{
"dialogue": "...The Apollo 11 mission landed on the moon in 1969...",
"summary": "Apollo 11 landed on the moon in 1969."
}
```
---

## 🔹 Methodology
1. Load datasets (`train.json`) and (`test.json`).
2. Initialize Hugging Face summarization pipeline with `facebook/bart-base`.
3. Generate summaries for sample passages.
4. Compare predicted summaries against reference summaries qualitatively.

---

## 🔹 Results
- The model produces **fluent and concise summaries**.
- Example:
```text
Input: "The stock market crashed yesterday due to global uncertainty..."
Predicted: "Global uncertainty caused a market crash."
Reference: "Stock market crashed due to uncertainty."
```
- Observations:
- Model captures main ideas well.
- Paraphrasing differs from references but remains faithful to meaning.
- Occasional factual drift (hallucination) observed.

---

## 🔹 How to Run
```bash
# Clone the repository
git clone <repo_url>
cd text_summarization.ipynb

# Install dependencies
pip install -r requirements.txt

# Run Jupyter Notebook
jupyter text_summarization.ipynb
```

---

## 🔹 Requirements
The main dependencies are listed in `requirements.txt`:

```
torch
matplotlib
transformers
pytorch_lightning
pandas
numpy
jupyter
```

- Install them with:
pip install -r requirements.txt


---


## 🔹 Skills Demonstrated
- Abstractive text summarization with transformer models
- Using Hugging Face `transformers` pipeline
- Working with JSON datasets for NLP
- Qualitative evaluation of generated summaries
- Reproducible NLP workflows with PyTorch & Hugging Face


---

## 🔹 License
This project is released under the MIT License. See the [LICENSE](LICENSE) file for details.


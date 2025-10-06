# TextMorph: Advanced Text Summarization and Paraphrasing

TextMorph is a Python-based pipeline designed to **extract, summarize, and paraphrase text** from PDF documents. It leverages **pre-trained Hugging Face transformer models** to generate concise summaries and multiple paraphrased variations. The project also includes evaluation metrics and visualizations to identify the most effective models for given datasets.

---

## 📂 Project Overview

This project is divided into several milestones. **Milestone 1** focused on understanding:

- PDF text extraction and cleaning.
- Chunking large documents for model-friendly processing.
- Loading and using summarization and paraphrasing models.
- Evaluating summaries using ROUGE metrics.
- Visualizing and saving results for easier inspection.

**Key Learnings from Milestone 1:**

- Extracting text from PDFs using `PyPDF2` and controlling page ranges.
- Chunking documents to avoid model input limitations.
- Understanding Hugging Face models for NLP tasks.
- Generating multiple paraphrased versions of summaries.
- Evaluating and comparing summaries using ROUGE-1, ROUGE-2, and ROUGE-L.
- Visualizing runtime, summary length, and quality to choose the best model.

---

## 🛠 Features

- Extract text from PDFs and clean it for processing.
- Split documents into smaller chunks for better summarization.
- Generate summaries using multiple Hugging Face transformer models.
- Produce paraphrased summaries using community checkpoints.
- Evaluate summarization performance quantitatively using ROUGE metrics.
- Visualize quality, runtime, and summary length for comparison.
- Save all outputs in an organized folder and display previews in the notebook.

---

## 📌 Hugging Face Models Used

### **Summarization Models**

| Model        | Description | Why Chosen |
|-------------|-------------|------------|
| `t5-base`   | Text-to-Text Transfer Transformer (T5) | Good balance between speed and summary quality; widely used for text generation. |
| `facebook/bart-base` | BART (Bidirectional and Auto-Regressive Transformer) | Known for high-quality summarization; generates more detailed summaries. |
| `google/pegasus-xsum` | Pegasus for Extreme Summarization | Optimized for concise, extractive summaries; performs well on very short summaries. |

### **Paraphrasing Models**

| Model | Description | Why Chosen |
|-------|-------------|------------|
| `Vamsi/T5_Paraphrase_Paws` | T5-based paraphrasing | Produces alternative wordings while preserving meaning. |
| `eugenesiow/bart-paraphrase` | BART-based paraphrasing | Generates fluent paraphrases with context awareness. |
| `ramsrigouthamg/pegasus_paraphrase` | Pegasus-based paraphrasing | Produces concise paraphrased sentences; good for short summaries. |

**Model Selection Insight:**

- After generating summaries, **BART-base** consistently produced the most content-rich summaries for both **Computer Networks** and **Neuroscience** datasets.  
- **T5-base** generated concise summaries quickly and balanced quality and speed.  
- **Pegasus-xsum** was the most concise but sometimes lost details.  
- ROUGE evaluation and visualizations helped determine the best model for each dataset.

---

## 📁 Datasets

1. **Computer Networks (Andrew S. Tanenbaum)**  
[Download Link](https://drive.google.com/file/d/1lLUYb5dpVBb-fh82nGR9FJhDcud1ZdzC/view?usp=sharing)

2. **Neuroscience**  
[Download Link](https://drive.google.com/file/d/1jeJ3hdS_0rkKlWgbycCDHDQb3Tk0vLf7/view?usp=sharing)

---



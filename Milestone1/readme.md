# TextMorph: Advanced Text Summarization and Paraphrasing

TextMorph is a Python-based pipeline for extracting, summarizing, and paraphrasing text from PDF documents. It uses pre-trained Hugging Face transformer models to generate concise summaries and multiple paraphrased variations. The project also includes evaluation metrics and visualizations to identify the most effective models for different datasets.

## Project Overview

This project is structured into milestones. Milestone 1 focused on understanding:

- PDF text extraction and cleaning.
- Chunking large documents for efficient model processing.
- Loading and using summarization and paraphrasing models.
- Evaluating summaries using ROUGE metrics.
- Visualizing and saving results for inspection.

Key learnings from Milestone 1 include:

- Extracting text from PDFs using PyPDF2 with page range control.
- Chunking documents to respect model input limitations.
- Using Hugging Face models for summarization and paraphrasing.
- Generating multiple paraphrased versions of summaries.
- Evaluating summaries using ROUGE-1, ROUGE-2, and ROUGE-L.
- Visualizing runtime, summary length, and quality to identify the best model.

## Features

- Extract text from PDFs and clean it for processing.
- Split documents into smaller chunks for summarization.
- Generate summaries using multiple Hugging Face transformer models.
- Produce paraphrased summaries using community models.
- Evaluate summarization performance with ROUGE metrics.
- Visualize quality, runtime, and summary length.
- Save all outputs in an organized folder and display previews in the notebook.

## Hugging Face Models Used

Summarization Models:

- t5-base: A Text-to-Text Transfer Transformer. Chosen for its balance between speed and summary quality.
- facebook/bart-base: BART transformer. Known for producing content-rich, detailed summaries.
- google/pegasus-xsum: Pegasus model for extreme summarization. Produces concise summaries optimized for short output.

Paraphrasing Models:

- Vamsi/T5_Paraphrase_Paws: T5-based paraphrasing. Produces alternative wordings while preserving meaning.
- eugenesiow/bart-paraphrase: BART-based paraphrasing. Generates fluent paraphrases with context awareness.
- ramsrigouthamg/pegasus_paraphrase: Pegasus-based paraphrasing. Produces concise paraphrased sentences.

Model Selection Insight:

- BART-base produced the most content-rich summaries for both datasets.
- T5-base provided a good balance of speed and quality.
- Pegasus-xsum produced the shortest summaries and sometimes omitted details.
- ROUGE evaluation and visualizations guided the selection of the best model for each dataset.

## Datasets

- Computer Networks (Andrew S. Tanenbaum): [Download Link](https://drive.google.com/file/d/1lLUYb5dpVBb-fh82nGR9FJhDcud1ZdzC/view?usp=sharing)
- Neuroscience: [Download Link](https://drive.google.com/file/d/1jeJ3hdS_0rkKlWgbycCDHDQb3Tk0vLf7/view?usp=sharing)

## 📄 Milestone-1 Report  
This PDF explains each code cell in detail, describing its function and purpose in the TextMorph project.  
[View Milestone-1 Report](https://drive.google.com/file/d/1jiTHByMTKLmBmjmVZPPPCgxAVQJXOtMO/view?usp=sharing)







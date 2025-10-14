#  TextMorph – Multi-Model Text Summarization Project  
**Infosys Springboard Virtual Internship – Milestone 2**



##  Project Overview  
This project, **TextMorph**, was developed as part of the Infosys Springboard Virtual Internship under the **Generative AI** module (Milestone 2).  
The main goal of this project was to build a **text summarization system** that can take long pieces of text and generate short, meaningful summaries using different **AI models**.

The project was implemented in **Google Colab** using **Hugging Face Transformers** and other NLP libraries.  
An **interactive UI** was created using `ipywidgets` to make it easier to test, compare, and visualize results from multiple models.



##  Aim  
The aim of this project is to compare and analyze the performance of multiple AI models for **text summarization** and understand how different models handle meaning, fluency, and readability.



##  Objectives  
- To explore and implement **different summarization techniques** (abstractive and extractive).  
- To integrate multiple pre-trained **transformer models** from Hugging Face.  
- To design an **interactive UI** in Google Colab for real-time summarization.  
- To evaluate the performance using metrics like **ROUGE**, **Semantic Similarity**, **Readability**, and **Processing Time**.  
- To test and compare model results on **10 different domains of text**.  



##  Models Used  

| Model | Type | Developed By | Description |
|--------|------|--------------|-------------|
| **TinyLlama-1.1B-Chat** | Abstractive | TinyLlama Community | A lightweight version of LLaMA fine-tuned for chat and summarization tasks. |
| **Phi-2** | Abstractive | Microsoft | Compact 2.7B model trained on high-quality reasoning and educational datasets. |
| **BART-Large-CNN** | Abstractive | Meta (Facebook) | Transformer model fine-tuned on the CNN/DailyMail dataset for news summarization. |
| **Gemma-2B-IT** | Abstractive | Google DeepMind | Instruction-tuned model built for summarization and text generation. |
| **TextRank** | Extractive | NLTK / NetworkX | A classic algorithm that extracts key sentences based on graph ranking. |

###  Why Gemma Needs HF Token
 Google Gemma (google/gemma-2b-it) is a gated model on Hugging Face.
 It requires users to:
 Accept its license on Hugging Face
 Authenticate using an HF Token
 This ensures that only authorized users who accepted the license can access the model weights.

###  Token Setup Details
1. Created Hugging Face account → https://huggingface.co/
2. Generated Read Access Token → Profile > Settings > Access Tokens
3. Accepted Gemma License → https://huggingface.co/google/gemma-2b-it
4. Used GPU runtime in Google Colab → Runtime > Change runtime type > GPU
5. **Logged in interactively using `login()` method (not via Colab Secrets).**
6. After successful login, loaded Gemma model using the provided token.


##  Tools and Libraries Used  
- **Google Colab (GPU Runtime)**  
- **Python 3.12**  
- **Transformers (Hugging Face)**  
- **PyTorch**  
- **Sentence Transformers**  
- **ROUGE Score**  
- **NLTK**  
- **TextStat**  
- **Matplotlib, Pandas**  
- **Ipywidgets**  



##  Evaluation Metrics  

| Metric | Description |
|--------|-------------|
| **ROUGE (1, 2, L)** | Measures how much of the original content is preserved in the summary. |
| **Semantic Similarity** | Checks how similar the generated summary meaning is to the original text. |
| **Readability (Flesch / Gunning Fog)** | Measures how easy it is to read and understand the summary. |
| **Processing Time** | Calculates how long each model takes to generate the summary. |



##  Domains Used for Testing  
To make the evaluation fair and diverse, I tested the system on **10 different types of text**:  
1. Biography  
2. Science & Technology  
3. Education  
4. Business & Economy  
5. Healthcare & Medicine  
6. Environment  
7. History  
8. Sports  
9. Literature & Culture  
10. Research & Innovation  



##  Results and Observations  

| Model | Strengths | Weaknesses | Remarks |
|--------|------------|-------------|----------|
| **TinyLlama** | Fast and efficient; works well on short texts. | Sometimes misses key details. | Best for quick, small summaries. |
| **Phi-2** | Excellent accuracy and readability. | Slightly rigid phrasing. | Most balanced and reliable model overall. |
| **BART-Large-CNN** | Strong structure and factual accuracy. | Slower on large inputs. | Good for news-style content. |
| **Gemma-2B-IT** | Most fluent and human-like summaries. | Requires more computation. | Best for natural language fluency. |
| **TextRank** | Simple and transparent. | Doesn’t rephrase content. | Good for extractive tasks. |



##  Conclusion  
After testing across 10 domains and evaluating all metrics, I found that:  
- **Microsoft Phi-2** performed the best overall, giving high accuracy and fast response.  
- **Gemma-2B-IT** gave the best fluency and coherence but was slightly slower.  
- **BART-Large-CNN** produced well-structured summaries for long articles.  
- **TinyLlama** was the fastest, making it good for smaller systems.  
- **TextRank** worked well as a traditional extractive approach.  

 **Final Verdict:** Phi-2 is the most balanced model overall in terms of quality and speed.



## 💡 What I Learned  
- Gained practical experience using **transformer-based NLP models**.  
- Understood **abstractive vs extractive summarization** in detail.  
- Learned to calculate and analyze **ROUGE, Semantic Similarity, and Readability metrics**.  
- Got hands-on with **interactive UI design** using ipywidgets.  
- Learned how **model choice depends on task size, speed, and accuracy requirements**.  



##  Project Report  
A complete report was prepared covering:  
- Project aim, objectives, and description  
- Step-by-step explanation of code and functions  
- Evaluation results for 10 different texts  
- Charts, graphs, and metric tables  
- Final observations and conclusions  

📘 **Project Report:** [`TextMorph_Project_Report.pdf`](https://drive.google.com/file/d/1y6EBHSO0NqAdaxQdxbPYF5ruX_96gRVN/view?usp=sharing)



##  Project Outputs  
All outputs and evaluations from all 10 domains are compiled into one file.  
 **Combined Output PDF:** [`TextMorph_All_In_One_Final.pdf`](https://drive.google.com/file/d/1u7K14kd9iOsmPLAJSTdt64fJaZCnAXwR/view?usp=sharing)




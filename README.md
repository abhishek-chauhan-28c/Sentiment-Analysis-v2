# Sentiment Analysis v2 📊

NLP-powered sentiment classification pipeline using **Ollama (local LLM)** for analyzing Twitter and news data — zero external API calls.

## 📋 Problem Statement

Classifying sentiment in social media and news data at scale requires:
- Accurate sentiment labeling across large datasets
- Cost-effective processing (no API fees for large volumes)
- Structured, reproducible outputs

This project builds a pipeline that uses a **locally deployed LLM** (Mistral 7B via Ollama) to perform sentiment classification on text data.

## 📊 Dataset

- **Source:** Twitter/news data (Kotak Bank related mentions)
- **Data:** Processed CSV with text content and existing cluster labels
- **Volume:** Large-scale text classification task

## 🔧 Approach

### Pipeline Steps

1. **Data Loading:** Load processed text data from CSV
2. **Preprocessing:** Clean and prepare text data for classification
3. **Sentiment Classification:** Use Ollama (local LLM) to classify sentiment
4. **Structured Output:** Map classification results back to the dataset

### Sentiment Labels
- **Negative** — texts classified as negative sentiment
- **Neutral/Other** — default category for non-negative classification

### Key Implementation Details

- Uses `ollama.chat()` for LLM-based classification
- Applies classification logic using `pandas` for efficient batch processing
- Leverages existing cluster information (`cluster_name`) as supplementary signals
- Produces a new `Sentiment Pattern` column with classification results

## 📁 Project Structure

```
Sentiment-Analysis-v2/
├── Sentiment_Code.ipynb    # Main analysis notebook
    └── README.md              # This file
```

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3 | Core language |
| Ollama | Local LLM inference (Mistral 7B) |
| Pandas | Data loading, manipulation, and result mapping |
| NumPy | Numerical operations, conditional logic |

## 🚀 How to Run

```bash
# Clone
git clone https://github.com/Abhi-pacific/Sentiment-Analysis-v2.git
cd Sentiment-Analysis-v2

# Install dependencies
pip install pandas numpy ollama

# Make sure Ollama is running with a model loaded
# ollama serve
# ollama pull mistral

# Run the notebook
jupyter notebook Sentiment_Code.ipynb
```

## 💡 Key Insights

1. **Local LLM deployment** eliminates API costs and latency for large-scale sentiment analysis
2. **Zero external API calls** — fully local processing with Ollama
3. **Structured pipeline** — reproducible classification from raw data to labeled output
4. **Hybrid approach** — combines LLM classification with existing cluster signals for accuracy

## 👨‍💻 Author

**Abhishek Chauhan** — Data Analyst @ Netimpact Solutions  
[LinkedIn](https://linkedin.com/in/abhishek-chauhan-28c) | [Email](mailto:Chauhan.a.abhishek@icloud.com)

---

*Part of my data science portfolio. Check out my other projects on [GitHub](https://github.com/Abhi-pacific).*

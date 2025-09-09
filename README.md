# 🧠 Natural Language Processing (NLP) with Python

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=for-the-badge&logo=jupyter)
![NLP](https://img.shields.io/badge/NLP-Preprocessing-green?style=for-the-badge&logo=ai)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=for-the-badge)

This repository contains hands-on implementations of core **NLP preprocessing techniques** using **Python** and **Jupyter Notebook**. Each section demonstrates a fundamental concept in text preprocessing, preparing raw text for advanced Natural Language Processing tasks.

## 📋 Table of Contents

- [✨ Features](#-features)
- [🚀 Quick Start](#-quick-start)
- [📚 Topics Covered](#-topics-covered)
- [🗃️ Dataset](#️-dataset)
- [🛠️ Installation](#️-installation)
- [💻 Usage](#-usage)
- [🏗️ Project Structure](#️-project-structure)
- [📊 Results](#-results)
- [🤝 Contributing](#-contributing)
- [📜 License](#-license)
- [📞 Contact](#-contact)

---

## ✨ Features

- 🎯 **Hands-on implementations** of all core NLP preprocessing techniques
- 📓 **Jupyter Notebook** with detailed explanations and examples
- 🔬 **Practical examples** using real-world text data
- 📈 **Visualizations** to understand text transformations
- ⚡ **Optimized code** for efficiency and readability
- 🧠 **Advanced NLP techniques** including NER and POS tagging
- 📰 **Multiple real-world datasets** for diverse applications

---

## 🚀 Quick Start

### Prerequisites
- Python 3.13+
- pip package manager
- virtualenv (recommended)

### Installation
```bash
# Clone the repository
git clone https://github.com/mohammed28s/NLP_AI.git

# Navigate to project directory
cd NLP_AI

# Create virtual environment
python -m venv nlp-env

# Activate virtual environment
# On Windows:
nlp-env\Scripts\activate
# On macOS/Linux:
source nlp-env/bin/activate

# Install dependencies
pip install -r requirements.txt

# Download necessary NLP models
python -m spacy download en_core_web_sm
python -c "import nltk; nltk.download('punkt'); nltk.download('stopwords'); nltk.download('wordnet'); nltk.download('averaged_perceptron_tagger'); nltk.download('maxent_ne_chunker'); nltk.download('words')"

# Launch Jupyter Notebook
jupyter notebook
```

---

## 📚 Topics Covered

1. **🔠 Lowercasing**  
   - Convert all text into lowercase for normalization.  

2. **🚫 Removing Stop Words**  
   - Eliminate common words (like *the, is, and*) that don't add meaningful value.  

3. **🔍 Regular Expressions (Regex)**  
   - Clean text, extract patterns, and filter unwanted characters.  

4. **✂️ Tokenization**  
   - Break text into words or sentences for easier processing.  

5. **🌱 Stemming**  
   - Reduce words to their root form (e.g., *running → run*).  

6. **🍃 Lemmatization**  
   - Use linguistic rules to get dictionary base forms of words.  

7. **🔗 N-Grams**  
   - Generate word sequences (e.g., bigrams, trigrams) for context analysis.

8. **🧠 Named Entity Recognition (NER)**  
   - Identify and classify named entities in text (persons, organizations, locations).

9. **📖 Parts-of-Speech (POS) Tagging**  
   - Label words with their corresponding parts of speech.

10. **😊 Sentiment Analysis**
    - Analyze customer reviews to determine positive or negative sentiment.

---

## 🗃️ Dataset

The project uses two comprehensive real-world datasets:

1. **`bbc_news.csv`** - Contains:
   - News articles from BBC across various categories (business, politics, tech, etc.)
   - Ideal for NER, POS tagging, and content analysis
   - Columns include article content, categories, and metadata

2. **`tripadvisor_hotel_reviews.csv`** - Contains:
   - Customer reviews from Tripadvisor with rating scores
   - Perfect for sentiment analysis and review classification
   - Includes review text and numerical ratings

---

## 🛠️ Installation

Detailed installation instructions:

```bash
# Install required packages
pip install nltk scikit-learn pandas numpy matplotlib seaborn spacy textblob

# Download NLTK data
python -c "import nltk; nltk.download('punkt'); nltk.download('stopwords'); nltk.download('wordnet'); nltk.download('averaged_perceptron_tagger'); nltk.download('maxent_ne_chunker'); nltk.download('words')"

# Download spaCy model
python -m spacy download en_core_web_sm

# Download TextBlob corpora
python -c "import textblob; textblob.download_corpora()"
```

---

## 💻 Usage

Open the Jupyter Notebook and execute cells sequentially:

1. **Basic Preprocessing** (`NLP_Preprocessing.ipynb`):
```python
# Example code snippet for text preprocessing
from preprocessing_utils import TextPreprocessor

processor = TextPreprocessor()
processed_text = processor.clean_text("Your raw text goes here!")
print(processed_text)
```

2. **Advanced NLP Analysis** (`Advanced_NLP_Analysis.ipynb`):
```python
# Example code for NER and POS tagging
from advanced_utils import NLPAnalyzer

analyzer = NLPAnalyzer()
text = "Apple Inc. is located in Cupertino, California."

# Perform NER
entities = analyzer.extract_entities(text)
print("Named Entities:", entities)

# Perform POS tagging
pos_tags = analyzer.pos_tagging(text)
print("POS Tags:", pos_tags)
```

3. **Sentiment Analysis** (`Sentiment_Analysis.ipynb`):
```python
# Example code for sentiment analysis
from sentiment_utils import ReviewAnalyzer

analyzer = ReviewAnalyzer()
review = "This hotel had amazing service and beautiful rooms!"

# Analyze sentiment
sentiment = analyzer.analyze_sentiment(review)
print("Sentiment Score:", sentiment)
```

---

## 🏗️ Project Structure

```
NLP_AI/
│
├── 📓 NLP_Preprocessing.ipynb          # Core preprocessing techniques
├── 📓 Advanced_NLP_Analysis.ipynb      # Advanced techniques: NER & POS tagging
├── 📓 Sentiment_Analysis.ipynb         # Sentiment analysis on hotel reviews
├── 📰 bbc_news.csv                     # News dataset for analysis
├── 📝 tripadvisor_hotel_reviews.csv    # Hotel reviews dataset for sentiment analysis
├── 🔧 src/                             # Source code utilities
│   ├── preprocessing_utils.py          # Text preprocessing functions
│   ├── advanced_utils.py               # Advanced NLP analysis functions
│   └── sentiment_utils.py              # Sentiment analysis functions
├── 📊 results/                         # Output and visualizations
├── 📝 requirements.txt                 # Project dependencies
└── 📖 README.md                        # Project documentation
```

---

## 📊 Results

The notebooks include visualizations showing:
- 📉 Vocabulary reduction after preprocessing
- 📊 Word frequency distributions
- 🗂️ Comparison of different techniques
- 📋 Performance metrics for each method
- 🧠 Named entity recognition results
- 📖 Parts-of-speech tagging analysis
- 😊 Sentiment distribution across reviews
- ⭐ Rating vs sentiment correlation analysis

**Example Output:**
```
Original text: "The quick brown foxes are jumping over the lazy dogs!"
After preprocessing: "quick brown fox jump lazy dog"

NER Results: [('Apple', 'ORG'), ('Cupertino', 'LOC'), ('California', 'LOC')]
POS Tags: [('Apple', 'NNP'), ('Inc.', 'NNP'), ('is', 'VBZ'), ('located', 'VBN')]

Sentiment Analysis: 
Review: "This hotel had amazing service and beautiful rooms!"
Sentiment: Positive (Score: 0.87)
```

---

## 🤝 Contributing

We welcome contributions! Please feel free to submit issues, feature requests, or pull requests.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 📞 Contact

Created by [Mohammed](https://github.com/mohammed28s) - feel free to reach out!

[![Email](https://img.shields.io/badge/Email-Contact%20Me-blue?style=flat-square&logo=gmail)](mailto:mohammed.23s@outlook.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://linkedin.com/in/mohammed-86390a255)

---

<div align="center">

### ⭐️ Don't forget to star this repository if you found it helpful!

</div>

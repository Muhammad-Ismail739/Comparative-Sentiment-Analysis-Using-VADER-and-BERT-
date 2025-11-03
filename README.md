# Comparative Sentiment Analysis Using VADER and BERT  
### Amazon Reviews Sentiment Analysis

---

## Overview
This project investigates how individuals communicate their diverse thoughts and feelings through **Amazon product reviews**, by applying three **Natural Language Processing (NLP)** techniques (**TextBlob**, **VADER**, and **BERT**) to product reviews.  
The purpose is to ascertain how each model interprets **emotion in text**, and evaluate how the simpler **traditional rule-based tools** compare with the **advanced, deep learning models**, in assessing **sentiment**.  
The assessment process includes a **data-cleaning stage**, **sentiment assessment**, **social media analysis** of patterned and common words, and **visualization of the results**, which is done to contribute to a clear, meaningful, and aesthetically pleasing presentation of the analysis.  


---

## Dataset Summary
The dataset comprises many **Amazon product reviews**, primarily about **books** and **movies**.  
The most common words are *book*, *movie*, *read*, *story*, and *love*.  
The data is **diverse** since it includes approximately **equal numbers of positive and negative reviews**, which is good for **unbiased comparisons of models**.  

---

## Text Preprocessing
The reviews were prepared and standardized before analysis:
- HTML tags, punctuation, numbers, and special symbols were removed using **regex**.
- The text was tokenized and lemmatized with **NLTK** in order to transform words to their base form.
- Stopwords were removed, and everything was converted to lowercase.

---

## Sentiment Models Used

### 1. **TextBlob**
A lightweight model that calculates:
- **Polarity:** How positive or negative the text is.  
- **Subjectivity:** How factual or opinion-based the text is.  

It’s fast and easy to use but sometimes misses context or sarcasm.

---

### 2. **VADER (Valence Aware Dictionary and sEntiment Reasoner)**
VADER is a rule-based sentiment analyzer tuned for online text.  
It understands tone, capitalization, and punctuation.

**Average Scores:**
- Neutral → 0.63  
- Positive → 0.26  
- Negative → 0.11  

Most reviews lean toward a neutral tone, showing balanced emotions.

---

### 3. **BERT (Transformers Pipeline)**
BERT is a deep learning model capable of understanding **context** and **subtle meaning**.  
Using Hugging Face’s pre-trained model, it captured more nuanced sentiment patterns.

**Results:**
- Negative → ~61%  
- Positive → ~39%  

BERT detected slightly more negativity, showing its strength in recognizing context and sarcasm.

---

## Visual Insights

### Subjectivity Distribution
- **Mixed:** ~82%  
- **Subjective:** ~11–12%  
- **Objective:** ~6–7%  

Most reviews combine both facts and opinions.

### Polarity Distribution
- **Neutral:** ~60%  
- **Positive:** ~25%  
- **Negative:** ~15%  

Neutral reviews dominate the dataset, indicating that most users express opinions in a balanced way.

### Word Cloud
Common words like *book*, *movie*, *story*, and *love* appear frequently, confirming that the dataset focuses on storytelling and entertainment-related products.

---

## Model Comparison

| Model | Type | Strength | Limitation |
|--------|------|-----------|-------------|
| **TextBlob** | Lexicon-based | Simple and quick | Struggles with context & sarcasm |
| **VADER** | Rule-based | Detects tone and punctuation emphasis | Limited for longer, complex reviews |
| **BERT** | Transformer-based | Understands deeper context | Requires more resources (GPU) |

---

## Key Insights
- Most reviews are **neutral or mixed**, reflecting balanced feedback.  
- **VADER** classifies the majority of text as neutral.  
- **BERT** captures more subtle negativity and emotional tone missed by simpler models.  
- Together, these methods give a richer understanding of customer sentiment.

---

## Tools and Libraries
- **Python**
- **pandas**, **NumPy**, **Matplotlib**, **Seaborn**
- **NLTK**, **TextBlob**
- **Hugging Face Transformers**
- **WordCloud**, **Scikit-learn**

---

## Conclusion
This example illustrates how various sentiment analysis models analyze emotions in text.  
While **TextBlob** and **VADER** quickly and effectively capture general trends in sentiment, **BERT** is able to develop a much richer and context-sensitive understanding, especially for more subtle reviews.  
It serves as a nice illustration of combining classical NLP and modern transformer-related models to get a more complete picture of human sentiment.

---

## Author
**Muhammad Ismail Saleem**  

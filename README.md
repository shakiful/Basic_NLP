# Basic_NLP
# Homework 4 – Part C  
**Course:** CS5710 – Machine Learning  
**Student Name:** Md Shakiful Islam Khan  
**Student ID:** 700778823  

---

## 📄 Overview
This notebook contains the coding portion (Part C) of Homework 4, focusing on **Natural Language Processing (NLP)** tasks using **spaCy**.  
It demonstrates basic text preprocessing, tokenization, lemmatization, named entity recognition, and pronoun ambiguity detection.

---

## 🧩 Question 1 – Tokenization, Stopword Removal, and Lemmatization

### ✅ Objective
To preprocess a given sentence by:
- Tokenizing the text into words  
- Removing common stopwords  
- Applying **lemmatization** to get the root forms of words  
- Keeping only **nouns** and **verbs**

The code in Question 1 performs text preprocessing using the spaCy natural language processing (NLP) library.
The process starts by loading the English language model en_core_web_sm, which is capable of performing tokenization, part-of-speech (POS) tagging, and lemmatization.

The given input text is first tokenized — broken into individual words or tokens. Then, all stopwords (common words such as “the”, “in”, “is”, etc.) are removed since they do not contribute significant meaning to the text. The code then filters out only nouns and verbs, as these are the most informative parts of speech for understanding the core meaning of a sentence.

Finally, lemmatization is applied to each remaining word to convert it to its root or base form (for example, “playing” → “play”, “loves” → “love”).
This preprocessing step is often used before performing more complex NLP tasks like text classification, sentiment analysis, or clustering, as it reduces noise and standardizes the text.

## 🧩 Q2 – Named Entity Recognition and Pronoun Ambiguity Detection:
The code in Question 2 also uses spaCy to perform two main NLP tasks: Named Entity Recognition (NER) and Pronoun Ambiguity Detection.

In NER, spaCy automatically identifies and classifies real-world entities in the text, such as persons, organizations, locations, or products. For example, in the sentence

“Chris met Alex at Apple headquarters in California. He told him about the new iPhone launch.”
the model identifies Chris and Alex as PERSON, Apple as ORG, California as GPE, and iPhone as PRODUCT.

After entity recognition, the code checks for the presence of pronouns like “he”, “she”, “they”, “him”, “her”, or “them”. The goal is to detect pronoun ambiguity — situations where a pronoun could refer to multiple entities in the text, which can confuse NLP systems during text understanding or coreference resolution.

This approach is useful in applications such as chatbots, information extraction, or text summarization, where understanding who or what a pronoun refers to is essential for accurate comprehension.

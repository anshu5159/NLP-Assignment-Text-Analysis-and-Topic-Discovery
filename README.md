# 📑 NLP Assignment: Text Analysis and Topic Discovery  

## 🔹 Overview  
This project demonstrates an end-to-end workflow for **text analysis and topic discovery** using **Natural Language Processing (NLP)**.  
The dataset consists of **30 documents** spanning three domains:  
- 🌍 Climate & Environment  
- ⚽ Sports & Athletics  
- 💻 Technology & Data Science  

The main objective is to extract meaningful insights from unstructured text using:  
- **Text Preprocessing**  
- **TF-IDF Analysis**  
- **Word2Vec Embeddings**  
- **Latent Dirichlet Allocation (LDA)** Topic Modeling  

---

## 🔹 Objectives  
- Perform **text preprocessing**: lowercasing, punctuation removal, tokenization, and stopword removal.  
- Use **TF-IDF** to identify top keywords per document.  
- Train a **Word2Vec** model to capture semantic similarity between words.  
- Apply **LDA** topic modeling to discover hidden themes in the corpus.  
- Visualize results using **PCA (Word2Vec)** and **pyLDAvis (LDA topics)**.  

---

## 🔹 Methodology  

### 1. Preprocessing  
- Converted text to lowercase  
- Removed punctuation, digits, and stopwords (`nltk.stopwords`)  
- Tokenized using `nltk.word_tokenize`  

### 2. TF-IDF Analysis  
- Extracted top words per document using `TfidfVectorizer`  
- Produced a document-term matrix to quantify word importance  

### 3. Word2Vec Embeddings  
- Trained a **Skip-gram Word2Vec model** (`vector_size=100, window=5, epochs=300`)  
- Found similar words (e.g., `data → analysis, models, processing`)  
- Applied **PCA** to reduce embeddings and plotted clusters  

### 4. Topic Modeling (LDA)  
- Built an LDA model with **3 topics** using Gensim  
- Extracted **top 5 words per topic**  
- Assigned most relevant topic to each document  
- Visualized with **pyLDAvis**  

---

## 🔹 Results & Observations  

### TF-IDF (Top Keywords)  
- Climate docs: `emissions, warming, glaciers, biodiversity`  
- Sports docs: `goal, match, cricket, championship`  
- Tech docs: `data, analysis, models, machine`  

### Word2Vec  
- `"data"` was closest to `analysis, models, processing`  
- `"analysis"` was closest to `data, exploratory, patterns`  
- PCA plot showed **clear clustering** of climate, sports, and tech words  

### LDA Topics  
- **Topic 1 (Climate):** warming, emissions, climate, global, energy  
- **Topic 2 (Sports):** team, match, goal, athletes, championship  
- **Topic 3 (Technology):** data, analysis, models, machine, ai  

---

## 🔹 Visualizations
- **Word2Vec (PCA):** 2D scatter plot of embeddings  
- **LDA (pyLDAvis):** Interactive HTML visualization of topic-word distributions  

---


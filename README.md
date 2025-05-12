# H&M Product Material NLP Analysis

This repository contains a comprehensive NLP analysis of product material descriptions from H&M's dataset. The focus is on cleaning, vectorizing, clustering, and semantically analyzing the text data.

---

## 📌 Code Summary

### 1. Importing Required Libraries

- **Data Handling:** `pandas`, `numpy`  
- **Visualization:** `matplotlib`, `seaborn`, `wordcloud`  
- **Natural Language Processing (NLP):** `nltk`, `spacy`, `re`, `gensim`  
- **Machine Learning:** `TF-IDF`, `CountVectorizer`, `PCA`, `TSNE`, `KMeans`, `cosine_similarity`  

---

### 2. Data Loading & Preprocessing

- Dataset: [handm.csv](https://github.com/Mosaad2010-star/nlp-on-ecommerce-products/blob/main/handm.csv)  
- Removed rows missing material info  
- Lowercased all text, stripped digits and punctuation  
- Removed generic words like *lining*, *shell*, etc.  
- Applied stopword removal using NLTK  

---

### 3. Word Frequency & WordCloud

- Generated a WordCloud from cleaned text  
- Bar plot showing top 20 frequent words  
- Bigram analysis (2-word phrases) with visualization  

---

### 4. TF-IDF Vectorization & Visualization

- Vectorized material descriptions using TF-IDF (max 1000 features)  
- Dimensionality reduction with:
  - **PCA (Principal Component Analysis)**
  - **t-SNE (t-Distributed Stochastic Neighbor Embedding)**
- Visualized material clusters in 2D  

---

### 5. K-Means Clustering

- Applied KMeans (k=5) on TF-IDF vectors  
- Visualized clusters on PCA plot  
- Appended cluster labels to the dataframe  

---

### 6. Rule-Based Material Type Classification

- Categorized materials into:
  - **Natural:** cotton, wool, linen  
  - **Synthetic:** polyester, elastane, viscose  
  - **Other:** non-matching types  
- Pie chart visualizing the distribution  
- Grouped bar plot (if available) by product categories  

---

### 7. Material Similarity via Cosine Distance

- Used TF-IDF and cosine similarity to find top 5 similar descriptions to a given query (e.g., *"cotton polyester"*)  

---

### 8. Word2Vec-Based Semantic Clustering

- Trained Word2Vec model on cleaned text  
- Clustered most common words via KMeans  
- Visualized word clusters using PCA, annotated with labels  

---

## 🔗 Resources

- Dataset: [`handm.csv`](https://github.com/Mosaad2010-star/nlp-on-ecommerce-products/blob/main/handm.csv)  
- Notebook: [`nlp-on-ecommerce-products.ipynb`](./nlp-on-ecommerce-products.ipynb)

---

## 📧 Contact

Created by [Mosaad Hendam](mailto:Mosaad2010@gmail.com) – feel free to reach out!

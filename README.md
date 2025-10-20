# Topic Modeling on BBC News Articles Dataset

This project is part of the **Eleevo NLP Internship** and focuses on performing **Topic Modeling** on BBC News Articles using Natural Language Processing (NLP) and clustering techniques. The goal is to identify and extract hidden topics from a collection of BBC news articles.  

## Dataset  

- The dataset contains **2225 news articles** categorized into **5 topics**:  
  - Business  
  - Entertainment  
  - Politics  
  - Sports  
  - Technology  

- After combining and cleaning, the final dataset contains **2127 unique news articles** with 3 columns:  
  1. `index`  
  2. `News Article`  
  3. `Type`  

- Initial exploration shows:  
  - **Business** and **Sports** have higher proportions of articles.  
  - **Business** articles tend to be shorter, while **Politics** and **Entertainment** articles are longer.  
  - Most articles have word counts around **500 words**.  

## Data Cleaning  

- Removal of:  
  - Stopwords  
  - Short-length words (<3 characters)  
  - Special characters, numbers, extra white spaces, and newline characters  
- **Lemmatization** applied to reduce words to their root form  
- Plots were generated for **top 20 unigrams, bigrams, and trigrams** to highlight frequent and meaningful words after cleaning  

## Feature Extraction  

- Vectorization of news articles using **TF-IDF Vectorizer**  

## Modeling  

- **Clustering algorithms used:**  
  1. **Latent Dirichlet Allocation (LDA)**  
  2. **Latent Semantic Analysis (LSA)**  

### LDA Results  

- Successfully identified **5 distinct topics**.  
- Wordclouds for each topic show the **most significant words per topic**, reflecting the thematic structure of the news articles.  
- Visualization using **pyLDAvis** confirms clear separation of topics.  

### LSA Results  

- Also discovered 5 topics but clusters were **less distinct** compared to LDA.  
- Wordclouds show some irrelevant words in topics such as business and technology.  

## Conclusion  

- **LDA** is the best clustering algorithm for this dataset.  
- It effectively identifies the 5 topics and clusters articles with high accuracy.  
- Most significant words per topic provide insights into the thematic distribution of news content.  

## Tools and Libraries  

- Python  
- Pandas, NumPy  
- NLTK, SpaCy  
- Scikit-learn  
- Gensim  
- Matplotlib, Seaborn, WordCloud  
- pyLDAvis 

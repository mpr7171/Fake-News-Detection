# 📰 Fake News Detection

A Machine Learning-based project to classify news articles as **True** or **Fake** using natural language processing and a combination of statistical and semantic features. The model leverages pre-trained **Word2Vec embeddings** to extract meaningful linguistic characteristics, and it employs supervised learning algorithms to deliver high-accuracy predictions.

---

## 👨‍💻 Team Members

- **Arnab Biswas**  
- **Maddi Pranav Reddy**  
- **Mohan Nishantam**

---

## 📌 Problem Statement

Classify a given news text as **True** or **Fake** using supervised machine learning algorithms. Utilize the **Google News Word2Vec (300-d)** pre-trained embeddings for feature extraction and semantic representation.

---

## 🔍 Approach

### 1. **Data Preprocessing**
- Text cleaning: removal of punctuation, numbers, brackets, and stop words.
- Lemmatization: focusing primarily on nouns (`NN`, `NNS`) as they hold key semantic value.
- Conversion to lowercase for normalization.

### 2. **Feature Engineering**
- **Sentence Vectors**: Sum of all word vectors in a sentence.
- **Frobenius Norm**: Captures the volume of the text’s hyperspace.
- **Word Similarity**: Dot product between individual word vectors and the sentence vector.
- **Text Length**: Used as a proxy for editorial standards.
- **Named Entity Recognition (NER)**: Counts of entity types (person, organization, location, etc.).

### 3. **Modeling**
- Tried and tested models: Logistic Regression, Decision Tree, and Random Forest.
- Hyperparameter tuning using **GridSearchCV**.
- Evaluation metric: **F1 Score** (balances precision and recall, ideal for binary classification with roughly balanced classes).

---

## 📈 Exploratory Data Analysis (EDA)

- **Text length distributions** differ significantly between true and fake news.
- **Word clouds and N-grams** highlight focus areas: 
  - Fake news: more personal references, vague justifications, and visual proof.
  - True news: more institutional terms, verifiable sources, and official tone.
- **NER patterns**: Fake news focuses disproportionately on persons; true news has a balanced distribution across types.

---

## 🧠 Best Model

### ✅ **Logistic Regression**
- `(solver: liblinear, regularization: l1, penalty: 0.1)`
- **Accuracy**: 93.06%  
- **Precision**: 92.47%  
- **Recall**:  93.03%,  
- **F1 Score**: 92.75%  

✔️ Outperformed Decision Trees and Random Forest on most metrics  

---

## 📁 Files Included

All files are provided inside the ZIP archive:  
**`Fake_News_Detection_ArnabBiswas_MaddiPranavReddy_MohanNishantam.zip`**

- `Fake_News_Detection.ipynb` – Jupyter notebook containing the full implementation.
- `Fake_News_Detection_Report.pdf` – Final project report with analysis, EDA insights, and model evaluations.
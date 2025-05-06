
# 📰 News Recommender System

A content-based recommendation system for news headlines using **TF-IDF Vectorization** and **Cosine Similarity**, built with Python and Scikit-learn. This project allows users to get similar news articles based on a given headline or query text.

---

## 🚀 Features

- Clean and preprocess news headlines (remove stopwords, punctuation, lemmatize).
- Visualize distribution of news articles by category and month.
- Vectorize headlines using **TF-IDF**.
- Recommend articles based on:
  - A selected index from the dataset.
  - A custom input query entered by the user.
- Simple command-line interface for real-time headline recommendations.

---

## 📂 Dataset

- Dataset: **[News Category Dataset v2](https://www.kaggle.com/datasets/rmisra/news-category-dataset)**
- Contains over 200,000 news headlines from HuffPost from 2012 to 2018.
- Key columns: `headline`, `category`, `date`.

---

## 🛠️ Technologies Used

- Python
- Pandas & NumPy
- Scikit-learn
- NLTK (tokenization, stopwords, lemmatization)
- Matplotlib & Seaborn (visualizations)

---

## 📈 Visualizations

- Category-wise distribution of articles
- Month-wise article distribution

---

## 🧠 How It Works

### Preprocessing
- Filter headlines with less than 5 words.
- Remove duplicate headlines.
- Clean text by removing stopwords, punctuation, and applying lemmatization.

### Feature Extraction
- Use **TF-IDF Vectorizer** to convert text into numerical feature vectors.

### Recommendation Logic
- Compute cosine similarity using `pairwise_distances` from Scikit-learn.
- Retrieve top `n` similar headlines.

---

## 🧪 Example

```python
recommend_from_input("Trump signs new tax reform bill", 5)
```

**Output:**
```
============================== Queried headline ==============================
Your input: Trump signs new tax reform bill

========================= Recommended articles =========================
         date                     headline
2018-01-12    Trump praises tax reform during Ohio rally
2017-12-21    GOP celebrates as Congress passes tax reform
...
```

---

## ▶️ How to Run

1. Clone this repo or open the notebook in Google Colab.

2. Install required libraries (if not already installed):
   ```bash
   pip install nltk scikit-learn matplotlib seaborn
   ```

3. Download necessary NLTK resources:
   ```python
   import nltk
   nltk.download('stopwords')
   nltk.download('punkt')
   nltk.download('wordnet')
   nltk.download('omw-1.4')
   ```

4. Run the notebook or script:
   ```bash
   python NewsRecommender.py
   ```

5. Enter your own headline when prompted:
   ```
   Enter a news headline (or type 'exit' to quit): NASA launches new satellite for space observation
   ```

---

## 📌 Notes

- Headlines are filtered to improve semantic quality.
- Recommendations are based on content similarity — no user behavior or collaborative filtering.

---

## 📄 License

This project is open-source and free to use under the [MIT License](LICENSE).

---

## 🙌 Acknowledgments

- Dataset provided by [Rishabh Misra on Kaggle](https://www.kaggle.com/datasets/rmisra/news-category-dataset)
- Built as a hands-on NLP project to demonstrate text preprocessing and recommender systems using TF-IDF.

---


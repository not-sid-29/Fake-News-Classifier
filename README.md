# Fake-News-Classifier
## Aim: **Classifying between legitimate news and fake news using various deep learning models** <br>

---

### 1. Data Collection: <br>
- Dataset used: [Fake News Data](https://www.kaggle.com/c/fake-news/data) <br>
- Data cols: <br>
> `id` - unique id for news, <br>
> `title` - title for the news, <br>
> `author` - author of the news article, <br>
> `text` - contents of the article, <br>
> `label` - a label that marks an article to be potentially unreliable {1 : unreliable, 0 : reliable}<br>
---
### 2. Data Preprocessing: <br>
- Followed standard data cleaning technique, generated a custom engineered column `content` by appending the `author`, `title` and `text` columns.
- Stemmed the training split using `PorterStemmer`
- Generated one-hot encodings
---
### 3. Model Creation & Training: <br>
**A. Classifying using a Bidirectional LSTM-RNN model**:
- Created a bidirectional LSTM model, trained it for `epochs=25` with `batch_size=64`.
- Achieved an overall `accuracy_score` of `0.91` (model was approx. 91% accurate)

**B. Classifying using a simple LSTM-RNN model**:
- Created a simple LSTM-RNN model, trained it for `epochs=10` with `batch_size=64`.
- Achieved an overall `accuracy_score` of `0.92` (model was approx. 92% accurate)
---

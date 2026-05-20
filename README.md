# 🧠 Fake Review Detection System

A Machine Learning project that predicts whether a review is **Fake**, **Suspicious**, or **Genuine** using both **text analysis** and **review-based numerical features**.

This project combines **Natural Language Processing (NLP)** with **feature engineering** to detect potentially misleading or spam reviews.

---

## 🚀 Features

The model analyzes:

### 📝 Text Features
- Review text using **TF-IDF Vectorization**
- Repeated phrases detection
- Capital letter ratio
- Exclamation mark frequency

### 📊 Numerical Features
- Rating given by user
- Account age
- Verified purchase status
- Review length
- Profile photo visibility

---

## 🧠 Machine Learning Model

The project uses:

- **TF-IDF Vectorizer** → Converts text into numerical form
- **StandardScaler** → Scales numerical features
- **Random Forest Classifier** → Final prediction model

A **Pipeline + ColumnTransformer** is used to combine text and numerical preprocessing into a single ML workflow.

---

## 📂 Dataset Features

The dataset includes:

| Feature | Description |
|----------|-------------|
| `review_text` | Review content |
| `rating` | User rating |
| `account_age_days` | Age of reviewer account |
| `verified_purchase` | Whether purchase is verified |
| `review_length_words` | Total words in review |
| `all_caps_ratio` | Ratio of uppercase letters |
| `exclamation_count` | Number of `!` marks |
| `repeated_phrases` | Detects repetitive wording |
| `profile_photo` | Whether profile picture exists |

### Target Labels

| Label | Meaning |
|--------|----------|
| `Fake` | Likely spam/fake review |
| `Suspicious` | Potentially biased or sponsored |
| `Genuine` | Authentic review |

---

## ⚙️ Installation

Install required libraries:

```bash
pip install pandas numpy scikit-learn
```

---

## ▶️ How to Run

Run the Python file:

```bash
python PROJECT_2.py
```

Then provide inputs:

```text
PASTE THE REVIEW HERE:
TELL THE RATING:
IS THE PURCHASE VERIFIED:
IS THE PROFILE PICTURE VISIBLE:
```

Example:

```text
PASTE THE REVIEW HERE:
BEST PRODUCT EVER!!! MUST BUY!!!

TELL THE RATING:
5

IS THE PURCHASE VERIFIED:
no

IS THE PROFILE PICTURE VISIBLE:
yes
```

Output:

```text
Prediction: Fake
```

---

## 🔍 Feature Engineering Used

### 1. Review Length
Counts total words:

```python
len(review.split())
```

### 2. All Caps Ratio
Measures uppercase usage:

```python
sum(1 for c in letters if c.isupper()) / len(letters)
```

### 3. Exclamation Count
Detects aggressive marketing tone:

```python
review.count("!")
```

### 4. Repeated Phrase Detection
Flags repeated wording:

```python
Counter(review.lower().split())
```

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Scikit-Learn
- NLP (TF-IDF)

---

## 📌 Future Improvements

- Add sentiment analysis
- Improve dataset size
- Add GUI using Tkinter or Streamlit
- Try advanced NLP models
- Hyperparameter tuning

---

## 👨‍💻 Author
NAMIT SINGH
Developed as a Machine Learning project for detecting fake and suspicious online reviews.



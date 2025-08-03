# 📩 SMS Spam Classifier

A simple web application built using **Streamlit**, **NLTK**, and **Scikit-learn** to classify SMS messages as **Spam** or **Not Spam** using a trained machine learning model.

---

## 🚀 Features

- Clean UI using Streamlit
- Text preprocessing with NLTK (tokenization, stemming, stopword removal)
- Real-time prediction of SMS message type

---

## 🖥️ Demo

Enter a message in the text area and click **Predict** to classify the message as **Spam** or **Not Spam**.

---

## 🧠 Model Training (done separately)

The model and TF-IDF vectorizer were trained and saved using:

- Preprocessing (`transform_text`)
- `TfidfVectorizer`
- A classification algorithm (e.g., `MultinomialNB`)

The following files are required for inference:

- `model.pkl` – trained classification model
- `vectorizer.pkl` – trained TF-IDF vectorizer

---

## 📁 Project Structure

```
.
├── app.py                # Streamlit application script
├── vectorizer.pkl        # Trained TF-IDF vectorizer
├── model.pkl             # Trained machine learning model
├── requirements.txt      # Python dependencies
├── Spam-Detection.ipynb  # Jupyter notebook for training and experimentation
└── README.md             # Project documentation
```
---

## ⚙️ Setup Instructions

### 1. 🔁 Clone the Repository

```bash
git clone https://github.com/your-username/sms-spam-classifier.git
cd sms-spam-classifier
```

### 2. 🛡️ Create a Virtual Environment (Optional but Recommended)

```bash
# For Linux / macOS
python3 -m venv venv
source venv/bin/activate

# For Windows
python -m venv venv
venv\Scripts\activate
```

### 3. 📦 Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. 📚 Download NLTK Resources

Run the following **once** to download NLTK's tokenizer and stopwords:

```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
```

---

## ▶️ Run the App

```bash
streamlit run app.py
```

---

## 📌 Example Use Case

**Input Message:**
```
Congratulations! You've won a $1000 Walmart gift card. Go to http://bit.ly/123456 to claim now.
```

**Output:**
```
Spam
```

---

## ✅ Requirements

All required packages are listed in `requirements.txt`:

```
streamlit
nltk
scikit-learn
```

Install them via:

```bash
pip install -r requirements.txt
```

---

## 🧠 Model Details

- The model was trained using **TF-IDF vectorization** and a classification algorithm (e.g., Multinomial Naive Bayes).
- The training logic is available in `Spam-Detection.ipynb`.
- Trained artifacts:
  - `model.pkl`: the trained ML model
  - `vectorizer.pkl`: TF-IDF vectorizer

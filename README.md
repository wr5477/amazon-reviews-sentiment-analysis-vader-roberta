# 🛒 Amazon Reviews Sentiment Analysis (VADER vs RoBERTa)
<img width="735" height="310" alt="image" src="https://github.com/user-attachments/assets/7a6e3e18-29d3-4ff6-b38a-7ab866b37a2f" />


This project explores sentiment analysis on Amazon Fine Food Reviews by comparing a traditional lexicon-based model (**VADER**) with a transformer-based model (**RoBERTa**).  

The goal is to understand how different sentiment models behave, how confident they are in their predictions, and how well they align with human-provided star ratings.

---

## 📊 Dataset
**Amazon Fine Food Reviews Dataset**  
Source: https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews/data  

- ~500,000 Amazon reviews collected over more than 10 years (up to October 2012)
- Includes product and user information, star ratings (1–5), and plain text reviews
- Covers fine food products as well as reviews from other Amazon categories

<img width="1665" height="310" alt="image" src="https://github.com/user-attachments/assets/ea20fb08-68dd-4255-b124-22eb45d4f8ee" />

---

## 🧠 Project Workflow

### 1️⃣ Data Loading & Exploration
- Loaded the Amazon review dataset using pandas
- Inspected dataset structure and key columns
- Subsampled reviews for efficient experimentation

---

### 2️⃣ Text Preprocessing
- Tokenized review text using NLTK
- Performed basic text preparation for sentiment analysis models

---

### 3️⃣ Sentiment Analysis with VADER
- Applied VADER, a lexicon-based sentiment analysis model
- Extracted positive, neutral, negative, and compound sentiment scores
- Observed relatively conservative and overlapping sentiment distributions

<img width="802" height="150" alt="image" src="https://github.com/user-attachments/assets/148b8583-791d-4e14-b871-504a3a6be1e6" />
<img width="1490" height="490" alt="image" src="https://github.com/user-attachments/assets/71ad72d1-a833-4bd8-b59b-498908a360d9" />

---

### 4️⃣ Sentiment Analysis with RoBERTa
- Used a pretrained RoBERTa transformer model for sentiment classification
- Computed softmax probabilities for negative, neutral, and positive sentiment
- Compared predictions across different star ratings
- Observed stronger confidence and clearer sentiment separation compared to VADER


---
### 5️⃣ Quick Experiment with Hugging Face Pipelines
- Briefly explored the `pipeline()` API from Hugging Face
- Demonstrated how sentiment analysis can be performed with minimal code
- Highlighted a simpler, higher-level interface for rapid experimentation

<img width="1656" height="501" alt="image" src="https://github.com/user-attachments/assets/70fa1770-a9b9-4446-81e6-16efd3670aa6" />


---

### 6️⃣ Model Comparison & Visualization
- Merged sentiment scores with original star ratings
- Visualized relationships using pair plots
- Compared how VADER and RoBERTa distribute sentiment scores across ratings

<img width="1558" height="1476" alt="image" src="https://github.com/user-attachments/assets/c5931150-1469-4a0c-b6fa-99aac1f283e7" />

## 🔍 Key Observations
- RoBERTa produces more confident and clearly separated sentiment predictions
- VADER tends to be more conservative with overlapping sentiment scores
- Both models generally align with star ratings but differ in confidence
- Individual review examples reveal that perfectly capturing sentiment remains challenging

---

## 🧩 Conclusion
This project highlights the strengths and limitations of different sentiment analysis approaches.  
While transformer-based models such as RoBERTa show strong performance and confidence, they are not flawless and can struggle with subtle or ambiguous language.  
The brief exploration of the Hugging Face `pipeline()` API also suggests that there are accessible, higher-level tools that make advanced NLP models easier to use—an area worth exploring further.

<img width="1366" height="221" alt="image" src="https://github.com/user-attachments/assets/f87d2009-2e26-44fc-9d25-d93520b5ea57" />

---

## 🛠 Tools & Libraries
- Python
- pandas, numpy
- NLTK
- Hugging Face Transformers
- matplotlib, seaborn

---

## 📚 References
- Amazon Fine Food Reviews Dataset (Kaggle)
- [**Rob Mulla**](https://www.youtube.com/@robmulla)

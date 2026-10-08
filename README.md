# Machine Learning for Customer Complaint Categorisation (Python)

## Tools & Skills
- **Tools:** Python in Google Colab – pandas, NumPy, re, scikit-learn, Matplotlib, seaborn
- **Data preparation:** Data collection and manual labelling, text cleaning and normalisation, label encoding
- **Natural language processing:** TF-IDF vectorisation (unigrams and bigrams, English stopwords removed), stratified 80/20 train-test split
- **Machine learning:** Logistic Regression, Linear SVM and Multinomial Naïve Bayes, with balanced class weights
- **Evaluation:** Accuracy, precision, recall, F1-score and confusion matrix heatmaps

## What I Did
This was an assignment for the Machine Learning & Big Data module of my Data Analytics MSc. The aim was to automatically sort customer complaints into the right category, so they can be sent to the right team and resolved faster.

- **Dataset:** I built my own dataset by collecting 200 one-star Amazon reviews from Trustpilot and labelling each one into one of five categories: delivery, product quality, customer service, payment/billing and technical website/app (40 per category).
- **Preprocessing:** I cleaned and standardised the labels and text (fixing casing, whitespace, special characters and common typos), checked class balance and converted the text into numerical features using TF-IDF.
- **Modelling:** I trained three classification models on 80% of the data, tested them on the remaining 20%, and compared their performance overall and for each category.

## Key Findings
- Logistic Regression and Linear SVM performed best with 80% accuracy, compared with 75% for Naïve Bayes.
- Delivery complaints were the easiest to identify (F1-score of 1.0 for Logistic Regression and Linear SVM).
- Payment/billing complaints were the hardest for all three models, with recall of 0.50 for Logistic Regression and Linear SVM and 0.38 for Naïve Bayes. They were most often confused with customer service complaints.
- Next steps would be to collect a larger dataset and test an ensemble method such as adaptive boosting (AdaBoost) to improve the weaker categories.

## Files
| File | Description |
|------|-------------|
| `CIS4513 coursework.docx` | Full research report: literature review, methodology, results and discussion |
| `CIS4513_coursework.ipynb` | Python notebook covering preprocessing, model training and evaluation |
| `complaint categories dataset.xlsx` | The labelled dataset of 200 complaints |

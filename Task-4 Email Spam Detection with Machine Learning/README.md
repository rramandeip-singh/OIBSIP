# Email Spam Detection using Machine Learning

## 1. Project Overview

This project focuses on detecting whether a text message is **Spam** or **Ham (Not Spam)** using Machine Learning and Natural Language Processing (NLP).

This project was completed as part of the **Oasis Infobyte OIBSIP Data Science Internship – Task 4**.

---

## 2. Project Objective

The main objectives of this project are:

- Clean and preprocess the text dataset
- Analyze Spam and Ham messages
- Convert text into numerical features using TF-IDF
- Train multiple Machine Learning models
- Compare model performance
- Evaluate the final model
- Test the model using custom messages

---

## 3. Dataset

The project uses the **SMS Spam Collection Dataset**.

The messages are classified into two categories:

- **Ham** – Normal or legitimate messages
- **Spam** – Unwanted or fraudulent messages

The dataset initially contained **5,572 messages**.

After removing duplicate records, **5,169 unique messages** remained.

### Dataset Distribution

| Category | Messages |
|----------|---------:|
| Ham | 4,516 |
| Spam | 653 |
| **Total** | **5,169** |

---

## 4. Technologies and Tools Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Natural Language Processing (NLP)
- TF-IDF
- Logistic Regression
- Multinomial Naive Bayes
- Random Forest

---

## 5. Data Cleaning

The dataset was cleaned by:

- Renaming `v1` to `Label`
- Renaming `v2` to `Message`
- Removing unnecessary columns
- Checking for missing values
- Removing duplicate records

There were **403 duplicate records**.

After removing duplicates, **5,169 unique messages** remained.

---

## 6. Exploratory Data Analysis

Exploratory Data Analysis (EDA) was performed to understand the Spam and Ham messages.

### Message Distribution

| Category | Messages |
|----------|---------:|
| Ham | 4,516 |
| Spam | 653 |

### Average Message Length

| Category | Average Length |
|----------|---------------:|
| Ham | 70.46 |
| Spam | 137.89 |

Spam messages were generally longer than Ham messages.

---

## 7. Text Preprocessing

The text messages were cleaned before applying Machine Learning.

The preprocessing steps included:

- Converting text to lowercase
- Removing unnecessary characters
- Removing extra spaces
- Creating a `Clean_Message` column

---

## 8. Train-Test Split

The dataset was divided into training and testing sets using an **80/20 stratified split**.

- Training set: **4,135 messages**
- Testing set: **1,034 messages**

The split was performed before TF-IDF feature extraction to avoid data leakage.

---

## 9. TF-IDF Feature Extraction

TF-IDF (Term Frequency-Inverse Document Frequency) was used to convert the cleaned text messages into numerical features.


## 10. Machine Learning Models

Three Machine Learning classification models were trained and compared:

1. **Logistic Regression**
2. **Multinomial Naive Bayes**
3. **Random Forest**

These models were trained using the TF-IDF features.

---

## 11. Model Evaluation

The models were evaluated using the following metrics:

- Accuracy
- Precision
- Recall
- F1 Score

### Best Model: Logistic Regression

| Metric | Score |
|--------|------:|
| Accuracy | **97.87%** |
| Precision | **93.60%** |
| Recall | **89.31%** |
| F1 Score | **91.41%** |

Logistic Regression achieved the best overall performance and was selected as the final model.

---

## 12. Confusion Matrix

The Logistic Regression confusion 

13. Custom Message Prediction

Two custom messages were tested using the final model.

Message	Prediction	Spam Probability
Congratulations! You have won a free cash prize. Claim now!	Ham	22.58%
Hi, are we still meeting for lunch today?	Ham	25.34%

These results show that the model can classify new messages, but it may sometimes misclassify spam-like messages.

14. Key Findings

The main findings from the project are:

The final dataset contained 5,169 unique messages.
Ham messages were more common than Spam messages.
Spam messages were generally longer than Ham messages.
The average Spam message length was 137.89.
The average Ham message length was 70.46.
TF-IDF was used to convert text into numerical features.
Three Machine Learning models were trained and compared.
Logistic Regression performed the best overall.
The final model achieved 97.87% accuracy.
The final model achieved 93.60% precision.
The final model achieved 89.31% recall.
The final F1 Score was 91.41%.
The confusion matrix showed that 117 Spam messages were correctly detected, while 14 Spam messages were incorrectly classified as Ham.

## Author

**Rramandeip Singh**

Data Science Intern  
**Oasis Infobyte — OIBSIP**

---

## Internship Information

| Details | Information |
|---------|-------------|
| Organization | Oasis Infobyte |
| Program | OIBSIP – Data Science Internship |
| Domain | Data Science |
| Task | Task 4 – Email Spam Detection |
| Author | Rramandeip Singh |

---

## Acknowledgement

I would like to thank **Oasis Infobyte** for providing this opportunity through the **OIBSIP Data Science Internship**.

This project provided practical experience in Data Cleaning, Exploratory Data Analysis, Natural Language Processing, TF-IDF, Machine Learning, and Model Evaluation.

---

## Project Status

**Completed — OIBSIP Data Science Internship Task 4**






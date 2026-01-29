# 🧠 Mental Health Status Detection from Text

Language plays a central role in how individuals express emotional and psychological states. This project uses machine learning and text analysis to explore how different mental health statuses (such as depression, anxiety, stress, and suicidal ideation) are expressed through language in online posts. A key focus of the project is **interpretability**: rather than only predicting labels, we identify **status-specific words** and visualize them using **word clouds** to better understand how different mental health conditions are linguistically expressed.

## 🎯 Research Objectives

In addition to **mental health status classification**, this project explores the following question:

* **Are certain words uniquely associated with specific mental health conditions?**

## 📂 Dataset

**Sentiment Analysis for Mental Health Dataset**
🔗 [https://www.kaggle.com/datasets/suchintikasarkar/sentiment-analysis-for-mental-health](https://www.kaggle.com/datasets/suchintikasarkar/sentiment-analysis-for-mental-health)

### Dataset Features

* `statement`: text from online posts
* `status`: labeled mental health condition

**Mental health categories include:**
Normal, Depression, Suicidal, Anxiety, Bipolar, Stress, Personality disorder

**Unit of analysis:** Individual text statement

## 🛠️ Methods Used

* Sentiment analysis
* Word cloud visualization for status-specific language

## 🎓 Course Information

**Course:** STATS 201

## Weekly Progress

## Week 2: Research Setup & Initial Exploration

* Defined the **research problem** 
* Selected the **dataset** containing text statements labeled with mental health statuses.
* Formulated the **machine learning task** as a multi-class text classification problem.
* Conducted **initial exploratory data analysis (EDA)**

## Week 3: Model Training & Evaluation

* Split the dataset into train and test sets
* Used Logistic Regression as baseline model
* Evaluated performance using **accuracy, precision, recall, F1-score**, and a **confusion matrix**.

## Week 4: Feature Engineering & Model Comparison

* Text preprocessing (lowercasing, tokenization, stemming)
* Used XGBoostClassifier and Multinomial Naive Bayes
* Feature Engineering
* Evaluated performance using **accuracy, precision, recall, F1-score**, and a **confusion matrix**.

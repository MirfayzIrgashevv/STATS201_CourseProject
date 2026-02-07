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

# 📈 Weekly Progress Report — STATS201 Course Project

## Week 2: Research Definition & Initial Exploration

This week focused on establishing the foundation of the project. The main research question was defined around whether linguistic patterns can be used to distinguish between different mental health statuses, with particular attention to accessibility and language ambiguity.

* Selected the **Sentiment Analysis for Mental Health** dataset from Kaggle
* Examined dataset structure, features (`statement`, `status`), and missing values
* Conducted initial exploratory data analysis (EDA)
* Visualized the distribution of mental health statuses using a pie chart

The analysis revealed clear **class imbalance**, with *Normal* and *Depression* dominating the dataset, while *Anxiety*, *Bipolar*, *Stress*, and *Personality disorder* were underrepresented. This imbalance was noted as an important consideration for later modeling.

---

## Week 3: Baseline Model & Evaluation

The goal of this week was to establish a strong and interpretable baseline model.

* Cleaned the dataset by removing rows with missing text values
* Split the data into **80% training / 20% test sets** using stratified sampling
* Converted text into numerical features using **TF-IDF vectorization**
* Trained a **Logistic Regression** baseline model

Model performance was evaluated using accuracy, precision, recall, F1-score, and a confusion matrix.
The baseline model achieved an accuracy of **77.8%**, performing especially well on the *Normal* class, while showing notable confusion between linguistically similar categories such as *Depression* and *Suicidal*.

---

## Week 4: Feature Engineering & Error Exploration

This week focused on expanding the feature space and understanding model errors more deeply.

* Added interpretable structural features:

  * number of characters per statement
  * number of sentences per statement
* Analyzed descriptive statistics for these features
* Examined **misclassified samples** to understand instance-level errors

The error analysis showed that misclassifications were **systematic**, not random. Most errors occurred between clinically related mental health conditions, suggesting strong overlap in language rather than weaknesses in model implementation.

---

## Week 5: Model Comparison, Robustness & Interpretability

The final stage concentrated on understanding model behavior and improving robustness.

* Trained and compared:

  * Logistic Regression
  * Multinomial Naive Bayes
  * XGBoost
* Used **train vs. test diagnostics** to identify underfitting and overfitting
* Regularized XGBoost to reduce overfitting and improve generalization
* Compared confusion matrices across models to identify consistent error patterns

In addition, TF-IDF was used to extract the **top 20 unigrams and bigrams** for each mental health status. These results were visualized to provide interpretable insights into status-specific language. The analysis showed that categories with more distinctive vocabulary (e.g., *Anxiety*) were easier to classify, while overlapping language led to persistent confusion (e.g., *Depression* vs. *Suicidal*).

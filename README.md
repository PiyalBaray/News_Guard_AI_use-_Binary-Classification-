#  Fake News Detection Using Machine Learning

##  Project Overview

Fake News Detection is a Binary Text Classification project that uses Machine Learning and Natural Language Processing (NLP) to classify news articles into two categories: **Fake News** and **Real News**.

The project uses TF-IDF (Term Frequency–Inverse Document Frequency) to convert news text into numerical features and compares multiple classification algorithms. Based on the evaluation results, the **Passive-Aggressive Classifier** was selected as the best-performing model for this project.

An interactive web interface built with Gradio allows users to enter a news headline or article and receive a prediction.

##  Objectives

- Detect potentially fake and real news articles using Machine Learning.
- Preprocess and clean news text.
- Convert text into numerical features using TF-IDF.
- Compare 10 classification algorithms.
- Evaluate models using standard classification metrics.
- Build an interactive web application for news prediction.

##  Dataset

The project uses the Fake and Real News Dataset, which contains two CSV files:

- `Fake.csv` — Fake news articles.
- `True.csv` — Real news articles.

The dataset is combined into a single DataFrame, and binary labels are assigned:

| Label | Category |
|---|---|
| `0` | Fake News |
| `1` | Real News |

##  Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- TF-IDF Vectorizer
- Matplotlib
- Seaborn
- Gradio
- Google Colab

##  Project Workflow

1. **Data Collection:** Load `Fake.csv` and `True.csv`.
2. **Data Inspection:** Check dataset shape, columns, missing values, and duplicates.
3. **Data Labeling:** Assign `0` to Fake News and `1` to Real News.
4. **Data Merging:** Combine and shuffle both datasets.
5. **Data Cleaning:** Remove missing or duplicate records and clean the text.
6. **Exploratory Data Analysis:** Analyze class distribution and text length.
7. **Data Splitting:** Split the data into training and testing sets.
8. **Feature Extraction:** Convert text into numerical features using TF-IDF.
9. **Model Training:** Train and compare 10 classification algorithms.
10. **Model Evaluation:** Compare Accuracy, Precision, Recall, F1-Score, and Confusion Matrix.
11. **Model Selection:** Select the Passive-Aggressive Classifier based on the observed evaluation results.
12. **Web Application:** Build an interactive Gradio interface for predictions.

##  Classification Algorithms Compared

The following 10 algorithms were considered for comparison:

1. Logistic Regression
2. Perceptron
3. Passive-Aggressive Classifier
4. Linear Discriminant Analysis (LDA)
5. Quadratic Discriminant Analysis (QDA)
6. Bernoulli Naive Bayes
7. Complement Naive Bayes
8. Multinomial Naive Bayes
9. K-Nearest Neighbors (KNN)
10. Linear Support Vector Machine (Linear SVM)

**Selected Model:** Passive-Aggressive Classifier

The Passive-Aggressive Classifier was selected because it achieved the best result among the successfully evaluated models in this experiment. Actual performance metrics should be reported from the model evaluation output.

##  Evaluation Metrics

The models are evaluated using:

- **Accuracy:** Measures the proportion of correct predictions.
- **Precision:** Measures how many predicted positive examples are actually positive.
- **Recall:** Measures how many actual positive examples are correctly identified.
- **F1-Score:** Combines Precision and Recall into a single metric.
- **Confusion Matrix:** Shows correct and incorrect predictions for each class.

##  Web Application Features

- Simple and interactive user interface.
- Textbox for entering a news headline or full article.
- Predict button to classify the submitted text.
- Clear button to reset the input.
- Prediction output for Fake News or Real News.
- Home, About, and Contact sections.

##  Project Structure

```text
Fake-News-Detection/
│
├── Fake.csv
├── True.csv
├── Fake_News_Detection_Binary_Classification.ipynb
├── passive_aggressive_model.pkl
├── tfidf_vectorizer.pkl
├── app.py
├── requirements.txt
└── README.md
```

##  How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
cd YOUR-REPOSITORY
```

Replace `YOUR-USERNAME` and `YOUR-REPOSITORY` with your actual GitHub username and repository name.

### 2. Install Dependencies

```bash
pip install pandas numpy scikit-learn matplotlib seaborn gradio joblib
```

### 3. Train the Model

Open the Google Colab notebook and run the cells in order to preprocess the dataset, train the classification algorithms, evaluate their performance, and save the selected model and TF-IDF vectorizer.

### 4. Run the Web Application

After creating `app.py` and placing the saved model files in the same project directory, run:

```bash
python app.py
```

The application can then be tested using the local or hosted Gradio interface configured in the script.

##  Limitations

- Predictions depend on the quality and coverage of the training dataset.
- Unseen topics, writing styles, or misleading articles may be classified incorrectly.
- A model prediction does not independently verify the truth of a news story.
- Important news should be checked against reliable sources.

##  Future Improvements

- Expand the training dataset with more diverse and recent news.
- Improve text preprocessing and feature engineering.
- Perform hyperparameter tuning.
- Evaluate generalization on an independent dataset.
- Add probability or confidence estimates where supported and properly calibrated.
- Deploy the application on a permanent hosting platform.

##  Author

**Piyal Baray**

Email: [piyalbaray314@gmail.com](mailto:piyalbaray314@gmail.com)

##  Disclaimer

This project is developed for educational and research purposes. The output represents a Machine Learning prediction and should not be treated as definitive proof that a news article is true or false.

---

⭐ If you find this project useful, consider giving the repository a star on GitHub.

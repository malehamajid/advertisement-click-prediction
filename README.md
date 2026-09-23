# advertisement-click-prediction
# Ad Click Prediction Using Machine Learning

## Project Overview

Ad Click Prediction is a machine learning project that predicts whether a user will click on an advertisement based on information such as their age, income, internet usage, time spent on a website, and advertisement details.

The project uses data preprocessing and machine learning techniques to prepare the dataset, train a classification model, and predict whether an advertisement will receive a click.

The main goal of this project is to understand how machine learning classification algorithms can be applied to advertising data.

## Objectives

* Analyze user-related and advertisement-related data.
* Preprocess numerical, categorical, and text-based features.
* Convert categorical data into numerical values using LabelEncoder.
* Convert advertisement text into numerical features using TF-IDF Vectorization.
* Extract useful features from timestamps.
* Train a Random Forest classification model.
* Evaluate the model using accuracy and other classification metrics.
* Test predictions using unseen test data.

## Technologies and Libraries

The following tools and libraries are used in this project:

* Python
* Pandas
* NumPy
* Scikit-learn
* Jupyter Notebook / VS Code

## Dataset

The project uses an advertisement click dataset named `ad_click_dataset.csv`.

The dataset contains information about users, advertisements, and whether an advertisement was clicked.

### Dataset Features

| Column                   | Description                                                      |
| ------------------------ | ---------------------------------------------------------------- |
| Daily Time Spent on Site | Time a user spends on the website                                |
| Age                      | Age of the user                                                  |
| Area Income              | Income associated with the user's area                           |
| Daily Internet Usage     | Daily internet usage of the user                                 |
| Ad Topic Line            | Text describing the advertisement                                |
| City                     | City associated with the user                                    |
| Male                     | Numerical gender indicator in the dataset                        |
| Country                  | Country associated with the user                                 |
| Timestamp                | Date and time associated with the record                         |
| click                    | Target variable indicating whether the advertisement was clicked |

### Target Variable

The target column is `click`.

* `0` = Advertisement was not clicked.
* `1` = Advertisement was clicked.

## Project Workflow

The project follows these main steps:

1. Import the required libraries.
2. Load the dataset.
3. Explore and inspect the data.
4. Preprocess categorical and text features.
5. Extract date and time features.
6. Separate the input features and target variable.
7. Split the dataset into training and testing sets.
8. Train the Random Forest classifier.
9. Evaluate the model.
10. Test predictions on individual records.

## Data Preprocessing

Different preprocessing techniques are used depending on the type of data.

### 1. Label Encoding

LabelEncoder is used to convert categorical columns such as `City` and `Country` into numerical values.

This allows the categorical information to be represented numerically for the machine learning model.

### 2. TF-IDF Vectorization

The `Ad Topic Line` column contains text, so TF-IDF Vectorization is used to convert the text into numerical features.

TF-IDF stands for **Term Frequency–Inverse Document Frequency**.

It represents words numerically according to their importance within the text documents.

### 3. Timestamp Feature Extraction

The `Timestamp` column is converted into datetime format.

The following features are extracted:

* Hour
* Day
* Month
* DayOfWeek

These features represent different aspects of the date and time.

## Machine Learning Model

### Random Forest Classifier

The project uses the Random Forest classification algorithm.

Random Forest is an ensemble learning algorithm that combines predictions from multiple decision trees to produce a final prediction.

It is used here because the task involves predicting one of two possible classes:

* Click
* No click

## Model Training

The dataset is divided into training and testing sets.

The training data is used to train the model, while the testing data is used to evaluate its performance on data that was not used for training.

The trained model predicts whether an advertisement will be clicked based on the input features.

## Model Evaluation

The model is evaluated using classification metrics.

The evaluation includes:

* **Accuracy:** Measures the proportion of correct predictions.
* **Confusion Matrix:** Shows the counts of correct and incorrect predictions for each class.
* **Precision:** Measures how many predicted instances of a class were correct.
* **Recall:** Measures how many actual instances of a class were correctly identified.
* **F1-Score:** Combines precision and recall into a single metric.

### Experimental Result

The current Random Forest experiment achieved:

**Accuracy: 97%**

This is the result observed in the current experiment. Model performance may vary depending on the dataset, preprocessing, train-test split, and evaluation procedure.

## Testing the Model

The model can be tested using individual records from the test dataset.

For example, the model can predict whether the advertisement represented by a test record will be clicked.

The predicted result can then be compared with the actual target value.

* `Predicted Click = 0`: The model predicts that the advertisement will not be clicked.
* `Predicted Click = 1`: The model predicts that the advertisement will be clicked.

Comparing the predicted and actual values helps determine whether the prediction was correct.

## How to Run the Project

### Step 1: Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Replace `YOUR_GITHUB_REPOSITORY_URL` with your repository's actual URL.

### Step 2: Open the Project

Open the project folder in VS Code or Jupyter Notebook.

### Step 3: Install the Required Libraries

```bash
pip install pandas numpy scikit-learn jupyter
```

### Step 4: Add the Dataset

Place `ad_click_dataset.csv` in the appropriate project directory.

Make sure the dataset path in the notebook matches its actual location.

### Step 5: Run the Notebook

Open the notebook and execute the cells in order, starting with the library imports and dataset loading.

## Project Structure

```text
Ad-Click-Prediction/
│
├── ad_click_dataset.csv
├── ad_click_prediction.ipynb
└── README.md
```

The filenames shown above are an example structure. Adjust them to match the actual files in your repository.

## Learning Outcomes

Through this project, I practiced:

* Data loading and exploration using Pandas.
* Preprocessing categorical data using LabelEncoder.
* Text feature extraction using TF-IDF Vectorization.
* Extracting features from datetime values.
* Splitting data into training and testing sets.
* Training a Random Forest classifier.
* Evaluating a classification model using multiple metrics.
* Making predictions on test data.

## Future Improvements

Possible future improvements include:

* Comparing Random Forest with other classification algorithms.
* Improving preprocessing and feature engineering.
* Evaluating the model using cross-validation.
* Investigating class-wise performance using precision, recall, and F1-score.
* Building a simple user interface for making predictions.
* Testing the model on additional unseen data.

## Conclusion

This project demonstrates a machine learning workflow for advertisement click prediction, from data preprocessing and feature extraction to model training, evaluation, and testing.

It provides practical experience with categorical data encoding, text vectorization, datetime feature extraction, and classification using Random Forest.

---

**Project Type:** Machine Learning — Classification
**Language:** Python
**Algorithm:** Random Forest Classifier

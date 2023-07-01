# SmsSpamClassification

# README

This repository contains code for data cleaning, exploratory data analysis (EDA), and data preprocessing for a spam classification task. The dataset used is stored in the `spam.csv` file. The code is written in Python using the `numpy`, `pandas`, `nltk`, and `seaborn` libraries.

## Prerequisites
- Python 3.x
- Required libraries: `numpy`, `pandas`, `nltk`, `seaborn`

## Getting Started
1. Clone this repository to your local machine or download the ZIP file.
2. Install the required libraries using `pip`:
   ```
   pip install numpy pandas nltk seaborn
   ```
3. Run the code in a Python environment, such as Jupyter Notebook or any Python IDE.

## Code Overview
The code performs the following steps:

1. Data Cleaning:
   - Import the necessary libraries (`numpy`, `pandas`).
   - Read the dataset from the `spam.csv` file using `pd.read_csv`.
   - Remove unnecessary columns using `df.drop`.
   - Rename the remaining columns using `df.rename`.
   - Convert the target column to numeric values using `LabelEncoder`.
   - Check for missing values using `df.isnull().sum()` and remove duplicates using `df.drop_duplicates`.

2. Exploratory Data Analysis (EDA):
   - Display the first few rows of the dataset using `df.head()`.
   - Visualize the class distribution using a pie chart using `plt.pie`.
   - Compute additional features such as the number of characters, words, and sentences in each text using the `nltk` library.
   - Generate descriptive statistics for the new features using `df[['num_characters', 'num_words', 'num_sentences']].describe()`.
   - Visualize the distribution of the new features using histograms and pair plots using `sns.histplot` and `sns.pairplot`.
   - Compute the correlation between the features using a heatmap using `sns.heatmap`.

3. Data Preprocessing:
   - Define a text transformation function that converts text to lowercase, tokenizes the text, removes non-alphanumeric characters, stopwords, and performs stemming using the `nltk` library.
   - Apply the text transformation function to the text column in the dataset using `df['text'].apply(transform_text)`.

# README for Google Play Store Data Cleaning Notebook

## Overview
This Python notebook is designed to clean and preprocess the Google Play Store dataset. The dataset contains information about various apps available on the Google Play Store, including details such as app name, category, rating, reviews, size, installs, type, price, content rating, genres, last update, current version, and Android version. The notebook also includes user reviews data, which contains the app name, translated review, sentiment, sentiment polarity, and sentiment subjectivity.

The primary goal of this notebook is to clean the dataset by handling missing values, converting data types, and removing outliers. The cleaned dataset can then be used for further analysis or machine learning tasks.

## Dataset
The dataset consists of two main files:
1. **Google Play Store Apps Dataset (`googleplaystore.csv`)**: Contains information about various apps.
2. **Google Play Store User Reviews Dataset (`googleplaystore_user_reviews.csv`)**: Contains user reviews for the apps.

## Notebook Structure
The notebook is structured into several sections, each focusing on a specific aspect of data cleaning:

1. **Data and Importations**:
   - Import necessary libraries.
   - Load the datasets.
   - Display basic information about the datasets, including columns, shape, first few rows, missing values, and unique categories.

2. **Data Cleaning**:
   - Handle missing values in the apps dataset by filling missing ratings with the mean and filling missing content ratings and types with appropriate values.
   - Convert the size column to a numeric format and handle the "Varies with device" entries.
   - Convert the installs column to a numeric format.
   - Remove outliers in the installs column using the Interquartile Range (IQR) method.
   - Bin the ratings into categories (Low, Average, High).

3. **Outlier Detection**:
   - Identify and display rows where the rating is greater than 6, which are considered outliers.

4. **Central Tendency Metrics**:
   - Calculate and display central tendency metrics (mean, median, mode) for numerical columns (reviews, size, installs).
   - Calculate and display dispersion metrics (range, IQR, variance, standard deviation) for the same columns.
   - Determine the symmetry of the data distribution.

5. **Covariance and Correlation**:
   - Calculate and display the covariance and correlation matrices for numerical columns (rating, reviews, size, installs).

6. **User Reviews Analysis**:
   - Identify the app with the most reviews.
   - Calculate and display central tendency metrics for sentiment polarity.
   - Visualize the sentiment polarity distribution for the app with the most reviews and for all reviews.

## Usage
To use this notebook, follow these steps:

1. **Environment Setup**:
   - Ensure you have Python installed (preferably Python 3.7 or higher).
   - Install the required libraries using pip:
     ```bash
     pip install pandas numpy scikit-learn scipy seaborn matplotlib
     ```

2. **Download the Dataset**:
   - Download the `googleplaystore.csv` and `googleplaystore_user_reviews.csv` files and place them in the same directory as the notebook.

3. **Run the Notebook**:
   - Open the notebook in Jupyter or any compatible environment.
   - Run each cell sequentially to perform the data cleaning and analysis.

4. **Output**:
   - The notebook will output cleaned datasets, summary statistics, and visualizations.
   - The cleaned datasets can be saved for further analysis.

## Key Functions and Methods
- **Data Loading**: `pd.read_csv()` to load the datasets.
- **Handling Missing Values**: `fillna()`, `dropna()`.
- **Data Type Conversion**: `astype()`, `pd.to_numeric()`.
- **Outlier Removal**: IQR method.
- **Binning**: `pd.cut()` to bin ratings into categories.
- **Central Tendency Metrics**: `mean()`, `median()`, `mode()`, `max()`, `min()`, `quantile()`, `var()`, `std()`.
- **Covariance and Correlation**: `cov()`, `corr()`.
- **Visualization**: `sns.boxplot()`, `sns.histplot()`.

## Dependencies
- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical operations.
- **Scikit-learn**: For machine learning and data preprocessing.
- **Scipy**: For statistical functions.
- **Seaborn**: For data visualization.
- **Matplotlib**: For plotting graphs.

## Notes
- Ensure that the dataset files are correctly placed and named as specified.
- The notebook assumes that the dataset files are in the same directory as the notebook. Adjust the file paths if necessary.
- The notebook is designed to be run sequentially. Running cells out of order may result in errors.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Contact
For any questions or issues, please contact the author.

---

This README provides a comprehensive guide to understanding and using the Python notebook for cleaning the Google Play Store dataset. Follow the instructions to set up the environment, run the notebook, and analyze the cleaned data.

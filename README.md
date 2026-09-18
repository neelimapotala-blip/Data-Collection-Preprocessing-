1. Project Title

Data Collection and Preprocessing of Handwritten Digit Dataset

2. Introduction

Data preprocessing is an important step in Machine Learning. Raw data may contain missing values, duplicate records, incorrect data types, invalid values, and other inconsistencies.

In this project, a real-world handwritten digit dataset from the UCI Machine Learning Repository is collected and processed. The dataset contains images of handwritten digits from 0 to 9. The data is cleaned, validated, and transformed into a suitable format for further Machine Learning applications.

3. Objective

The main objectives of this project are:

To collect a real-world dataset from a public source.
To use a dataset containing more than 1,000 samples.
To inspect the quality of the collected data.
To identify and handle missing values.
To identify and remove duplicate records.
To correct inappropriate data types.
To detect invalid values and potential outliers.
To perform suitable feature engineering.
To create a clean dataset for Machine Learning.
To document the complete preprocessing pipeline.
4. Dataset Description

Dataset Name: Optical Recognition of Handwritten Digits

Source: UCI Machine Learning Repository

Dataset Type: Classification

Number of samples used: 1,797

Original features: 64 pixel features

Number of classes: 10

Classes: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9

Each handwritten digit is represented as an 8 × 8 image, resulting in 64 pixel-related features.

The pixel intensity values range from 0 to 16.

Dataset source:
UCI Machine Learning Repository – Optical Recognition of Handwritten Digits.

5. Tools and Technologies

The following technologies were used:

Python
Pandas – data manipulation
NumPy – numerical operations
Scikit-learn – dataset collection and Machine Learning utilities
Matplotlib – visualization
Jupyter Notebook – analysis and documentation
GitHub – project version control and submission
6. Data Collection

The dataset was obtained from the publicly available UCI handwritten digit dataset through the scikit-learn dataset interface.

The collected dataset contains:

Samples       : 1,797
Features      : 64
Target classes: 10
Pixel range   : 0–16

The dataset satisfies the project requirement of having at least 1,000 samples.

7. Data Preprocessing Pipeline

The following preprocessing steps were performed:

Data Collection
       ↓
Data Inspection
       ↓
Data Type Correction
       ↓
Missing Value Checking
       ↓
Duplicate Detection
       ↓
Range Validation
       ↓
Outlier Detection
       ↓
Feature Engineering
       ↓
Clean Dataset
       ↓
Save Processed Data
8. Handling Missing Values

The dataset was checked for missing or null values.

Result:
Missing values before preprocessing : 0
Missing values after preprocessing  : 0

Although this dataset contains no missing values, the preprocessing script includes median imputation so that the pipeline can handle missing numeric values if they occur in a modified dataset.

9. Handling Duplicate Values

The dataset was checked for duplicate rows.

Result:
Duplicate rows found : 0
Duplicate rows removed: 0

Therefore, no records had to be removed because of duplication.

10. Data Type Correction

All dataset columns were checked and converted into appropriate numeric data types.

The 64 pixel features represent numerical pixel intensity values, while the target column represents the digit class.

This ensures that the dataset can be processed correctly by Machine Learning algorithms.

11. Invalid Value Detection

According to the dataset documentation, pixel intensity values should be between 0 and 16.

The dataset was therefore checked for values outside this range.

Result:
Invalid pixel values: 0

No invalid pixel values were found.

12. Outlier Detection

The Interquartile Range (IQR) method was used to identify potential outliers.

The formula used is:

IQR = Q3 - Q1

Lower Bound = Q1 - 1.5 × IQR

Upper Bound = Q3 + 1.5 × IQR

Potential outliers were identified based on individual pixel features.

However, detected unusual pixel patterns were not automatically deleted, because unusual pixel patterns can represent legitimate handwriting characteristics.

This prevents valid handwritten samples from being unnecessarily removed.

13. Feature Engineering

Five additional features were created from the original 64 pixel features.

1. Total Intensity

The sum of all pixel intensity values.

total_intensity = sum of all pixel values

This represents the overall intensity of the handwritten digit.

2. Nonzero Pixels

Counts the number of pixels whose intensity is greater than zero.

nonzero_pixels = count(pixel > 0)

This gives an indication of how much of the image contains handwriting strokes.

3. Mean Pixel

Calculates the average intensity of all pixels.

mean_pixel = average of pixel values
4. Standard Deviation of Pixels

Measures the variation in pixel intensity.

std_pixel = standard deviation of pixel values
5. Horizontal Symmetry Score

Compares the left and right portions of the digit image.

A smaller value indicates greater similarity between the two sides.

14. Before and After Preprocessing
Parameter	Before	After
Samples	1,797	1,797
Original features	64	64
Engineered features	0	5
Missing values	0	0
Duplicate rows	0	0
Invalid pixel values	0	0
Target classes	10	10
Final dataset
Samples           : 1,797
Original features : 64
New features      : 5
Total features    : 69 + target
15. Project Files
Task-2-Data-Collection-Preprocessing/
│
├── data/
│   ├── digits_raw.csv
│   └── digits_cleaned.csv
│
├── preprocessing/
│   └── preprocessing.py
│
├── notebook/
│   └── data_preprocessing.ipynb
│
├── screenshots/
│   ├── 01_class_distribution.png
│   ├── 02_missing_values.png
│   ├── 03_data_quality_checks.png
│   └── 04_example_digit.png
│
├── DATA_DOCUMENTATION.md
├── README.md
├── requirements.txt
└── submission_notes.txt
16. Expected Output

After running the preprocessing program, the output displays information such as:

Initial shape: (1797, 65)

Missing values before: 0
Missing values after: 0

Duplicates found: 0

Invalid pixel values: 0

Preprocessing completed.

Final shape: (1797, 70)

The cleaned dataset is saved as:

data/digits_cleaned.csv
17. Conclusion

This project demonstrates a complete Data Collection and Preprocessing pipeline using a real-world handwritten digit dataset.

The dataset was inspected for missing values, duplicate records, incorrect data types, invalid values, and potential outliers. Feature engineering was also performed to create additional numerical features from the original pixel information.

The final processed dataset is suitable for further Machine Learning tasks such as classification and pattern recognition.

18. Dataset Reference

Alpaydin, E. & Kaynak, C. (1998). Optical Recognition of Handwritten Digits. UCI Machine Learning Repository.

UCI Machine Learning Repository – Optical Recognition of Handwritten Digits

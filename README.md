# Vessel-Identity-Detector
This project is under my summer internship'24 at Bharat Electronics Limited. as a machine learning trainee

---

## Maritime Data Analysis and MMSI Classification

This repository contains code and resources for analyzing maritime data, performing data augmentation and standardization, training a RandomForestClassifier for MMSI classification, and creating various visualizations.

## Project Structure

### 1. `model.ipynb`

This notebook focuses on the preprocessing, training, and evaluation of the RandomForestClassifier for MMSI classification.

- **Data Loading**: Loads the augmented maritime data.
- **Preprocessing**:
  - One-hot encoding of categorical features (`PORT OF ORIGIN`, `PORT OF DESTINATION`, `VESSEL TYPE`).
  - Conversion of `TIMESTAMP` to datetime format and extraction of time features (`HOUR`, `DAY_OF_WEEK`, `MONTH`).
  - Standardization of numerical features (`LATITUDE`, `LONGITUDE`, `COURSE`).
- **Model Training and Evaluation**:
  - Splits the data into training and testing sets.
  - Trains a RandomForestClassifier.
  - Evaluates the model using accuracy score and classification report.
  - Tries different test data split ratios to compare performance.

### 2. `report.ipynb`
#### Data Augmentation and Standardization
This notebook performs data augmentation and standardization to improve model performance.

- **Data Loading**: Loads the historical AIS data.
- **Data Preprocessing**:
  - Removes irrelevant columns (`DATE TIME (UTC)`).
  - Standardizes numerical features (`LATITUDE`, `LONGITUDE`, `COURSE`).
- **Data Augmentation**:
  - Adds noise to the numerical features to create an augmented dataset.
  - Combines the original and augmented datasets.
- **Data Saving**: Saves the augmented and standardized dataset for further use.

### 3. `visualization.ipynb`

This notebook creates various visualizations to understand the maritime data better.

- **Data Loading**: Loads the augmented maritime data.
- **Data Preprocessing**:
  - Converts `TIMESTAMP` to datetime format and extracts time features.
- **Visualizations**:
  - Distributions of `LATITUDE`, `LONGITUDE`, and `COURSE`.
  - Count plots for `PORT OF ORIGIN`, `PORT OF DESTINATION`, and `VESSEL TYPE`.
  - Correlation heatmap for numerical features.
  - Geospatial plot of vessel movements using Plotly.
  - Distributions of vessel movements by `HOUR`, `DAY_OF_WEEK`, and `MONTH`.
  - Histograms, scatter plots, and box plots for training and test data.
  - Feature histograms by `MMSI` for training and test data.

## Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/maritime-data-analysis.git
cd maritime-data-analysis
```

2. Install the required dependencies:

```bash
pip install -r requirements.txt
```

## Usage

1. **Data Augmentation and Standardization**:

   Open `data_augmentation_standardization.ipynb` and run all cells to generate the augmented and standardized dataset.

2. **Model Training and Evaluation**:

   Open `model.ipynb` and run all cells to preprocess the data, train the RandomForestClassifier, and evaluate its performance.

3. **Visualization**:

   Open `visualization.ipynb` and run all cells to create various visualizations to understand the data better.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or new features.


---

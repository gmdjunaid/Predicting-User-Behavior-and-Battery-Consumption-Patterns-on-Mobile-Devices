# Predicting-User-Behavior-and-Battery-Consumption-Patterns-on-Mobile-Devices

## Overview

This project focuses on understanding user behavior on mobile devices and identifying the key factors influencing battery consumption. With mobile devices increasingly central to daily life—serving as primary tools for work, communication, and entertainment—battery life has become a critical performance metric. By leveraging advanced analytics and machine learning methods, this project aims to reveal insights into how different usage patterns contribute to battery drain, and how those insights can inform more targeted and effective battery optimization strategies.

## Problem Statement

Modern mobile devices are indispensable, yet they often face limitations due to battery life. While generic power-saving modes are available, they rarely account for the varied and dynamic ways individuals use their devices. Some users may drain their batteries through heavy gaming or video streaming, while others may consume power steadily throughout the day with continuous browsing or messaging. Identifying the specific behaviors that lead to higher battery usage can guide the development of smarter, more personalized power-management solutions, thus improving user satisfaction and device longevity.

## Objectives

- **Identify Key Variables:** Determine which factors (e.g., app usage time, screen-on time, number of installed apps, etc.) most strongly influence battery consumption.
- **User Segmentation:** Classify users into distinct behavioral categories based on their usage patterns.
- **Prediction and Optimization:** Develop predictive models to estimate battery drain and suggest targeted strategies for optimizing battery life.

## Dataset

- The dataset, `user_behavior_dataset.csv`, includes features such as:
  - **Operating System**  
  - **Device Model**  
  - **App Usage Time (min/day)**  
  - **Screen On Time (hours/day)**  
  - **Battery Drain (mAh/day)**  
  - **Number of Apps Installed**  
  - **Data Usage (MB/day)**  
  - **User Behavior Class**

  Before running the code, ensure that this dataset is placed in the project directory.

## Project Structure

- `user_behavior_dataset.csv` : Input data file  
- `final_project.ipynb` : Main Python script in a jupyter notebook file for data loading, preprocessing, modeling, and evaluation  
- `requirements.txt` : Python dependencies required for this project  
- `README.md` : Project documentation (this file)

## Setup Instructions

### 1. Creating the Virtual Environment

To isolate project dependencies, it is recommended to use a Python virtual environment(or just upload the files into a jupyter notebook online if you dont have a python virtual environment):

```bash
python3 -m venv venv
```

### 2. Activating the Virtual Environment

Activate the virtual environment with the following command:

- On macOS/Linux:
  ```bash
  source ./venv/bin/activate
  ```
- On Windows:
  ```bash
  .\venv\Scripts\activate
  ```

### 3. Installing Required Libraries

All necessary libraries are listed in the `requirements.txt` file. To install them, run:

```bash
pip install -r requirements.txt
```

This ensures you have the correct versions of `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`, `psycopg2`, and any other dependencies.

### 4. Running the Analysis

1. **Data Preprocessing & Modeling:**  
   Run `final_project.ipynb` to:
   - Load and preprocess the dataset
   - Perform exploratory data analysis (EDA)
   - Insert processed data into a PostgreSQL database (if configured)
   - Train classification and regression models
   - Evaluate model performance and visualize results

   ```bash
   python final_project.ipynb
   ```

2. **Exploring Results:**  
   After running the script, generated plots and summaries will help you understand:
   - The distribution and correlations of features
   - The accuracy and F1 scores of classification models
   - The MAE and RMSE of regression models
   - The importance of different features in predicting battery drain

## Results & Insights

- **User Behavior Classification:** The model classifies users based on their usage patterns, helping identify which activities are most indicative of higher battery drain.
- **Predictive Accuracy:** Classification and regression metrics indicate the reliability of the predictive models in identifying and quantifying battery usage behavior.
- **Feature Importance:** Identifying which features (e.g., screen-on time, app usage) contribute the most to battery drain can guide more targeted optimization strategies.

## Future Work

- **Refinement of Models:** Testing more advanced modeling techniques (e.g., XGBoost, deep learning models) and tuning hyperparameters.
- **Additional Features:** Incorporating new variables (e.g., location data, type of apps used) could provide deeper insights into consumption patterns.
- **Real-Time Prediction:** Integrating predictive models into live mobile systems to dynamically adjust settings and prolong battery life.

## Contact & Support

For questions, suggestions, or troubleshooting help, feel free to open an issue in the repository or reach out to the project maintainer.

---

By following these instructions and exploring the results, you will gain valuable insights into user behavior patterns and their impact on battery consumption.

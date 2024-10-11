# Accident Severity Prediction Using Machine Learning

## Table of Contents
- [Project Overview](#project-overview)
- [Data](#data)
- [Methodology](#methodology)
- [Results](#results)
- [Recommendations](#recommendations)
- [Model](#model)
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)

## Project Overview
This project aims to predict the severity of accidents based on various features using machine learning techniques. By analyzing historical accident data, we can identify patterns that may help in understanding the factors contributing to different levels of injury severity. The primary goal is to develop a predictive model that can assist policymakers and transportation safety professionals in making informed decisions to enhance road safety.

## Dataset
The dataset used for this project can be found [here](https://www.kaggle.com/datasets/saurabhshahane/road-traffic-accidents).

## Data
The dataset used for this project contains records of traffic accidents, including various attributes related to the drivers, vehicles, and circumstances of the accidents.  Key features include:
- **Time**: Time of the accident
- **Day_of_week**: Day on which the accident occurred
- **Age_band_of_driver**: Age category of the driver
- **Sex_of_driver**: Gender of the driver
- **Driving_experience**: Experience level of the driver
- **Type_of_vehicle**: Vehicle type involved in the accident
- **Accident_severity**: Severity of the accident (target variable)

The dataset has undergone preprocessing steps to handle missing values and encode categorical variables.

## Methodology
1. **Data Preprocessing**:
   - Dropped columns irrelevant to accident severity.
   - Encoded categorical features using Label Encoding.
   - Split the dataset into training and testing sets.

2. **Model Training**:
   - Implemented SMOTE (Synthetic Minority Over-sampling Technique) to address class imbalance in the dataset.
   - Trained an XGBoost classifier to predict accident severity.

3. **Model Evaluation**:
   - Assessed the model's performance using metrics such as accuracy, precision, recall, and F1-score.
   - Generated a confusion matrix to visualize the classification results.
     
## Results
The model achieved an accuracy of approximately **77.54%**. The classification report indicates the following results:

**Classification Report**:
                 precision    recall  f1-score   support

  Fatal injury       0.00      0.00      0.00        52
Serious Injury       0.26      0.19      0.22       552
 Slight Injury       0.85      0.89      0.87      3091

      accuracy                           0.78      3695
     macro avg       0.37      0.36      0.36      3695
  weighted avg       0.75      0.78      0.76      3695

  
A confusion matrix was generated to visualize the predictions compared to actual values.

## Recommendations
Based on the distribution analysis of accident occurrences, the following recommendations can be made:

1. **Targeted Awareness Campaigns**:
   - Focus on educating young male drivers, especially owner-drivers with little to moderate driving experience. Emphasize safe driving practices and the importance of experience in handling difficult driving conditions.

2. **Enhanced Road Safety Measures**:
   - Implement safety measures at Y-Shape junctions and other road types identified as high-risk areas. This could include better signage, road markings, and possibly traffic lights to manage vehicle flow more effectively.

3. **Monitoring and Analysis of Time Patterns**:
   - Since the majority of accidents occur from noon to late evening, authorities should monitor traffic conditions during these hours closely. Increased police presence or automated speed monitoring can deter reckless driving behavior.

4. **Weather-Related Safety Initiatives**:
   - Given that many accidents occur under normal weather conditions, it’s essential to implement weather-related safety initiatives. This could involve providing resources and guidance for safe driving in varying conditions.

5. **Ongoing Data Analysis**:
   - Continuous analysis of accident data should be conducted to adapt strategies and measures in response to emerging trends, ensuring road safety efforts remain effective.

## Model Storage
Due to the large size of the model file (`rf_model.pkl`), it is not included in this repository. You can download the model from [this cloud storage link](link_to_your_cloud_storage).

### Alternative Access
If you prefer, you can also download the model from a cloud storage service such as Google Drive or Dropbox. Here is the link to access the model: [Download Model](link_to_your_cloud_storage).


## Installation
To run this project, clone the repository and install the required libraries:
in requirement.txt

## Usage
To use the trained model and make predictions, you can run the Streamlit application:
streamlit run app.py

## License
This project is licensed under the Apache License. See the LICENSE file for more details.

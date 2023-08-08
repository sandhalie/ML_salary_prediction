# Predicting Salary based on Demographic Factors and Experience

## Introduction

Welcome to our machine learning project, where we embark on a journey to forecast salaries by leveraging a blend of experience years, department, job title seniority, and qualification levels. This endeavor encompasses the complete spectrum of data-driven salary prediction, spanning data collection, model curation, training and assessment, insightful data visualization, and comprehensive documentation.

Note:  In an effort to ensure fairness and eliminate potential biases, we have made a deliberate decision to exclude age and gender from our predictive model. This approach aligns with our commitment to creating a transparent and unbiased salary prediction system.

## Methodology

### Data Collection

Our data foundation is meticulously crafted, procuring a dataset that encapsulates critical details, including salaries, educational qualifications, and experience years. This dataset is sourced from Kaggle and can be accessed via the following link:
[Salary Prediction Dataset](https://www.kaggle.com/datasets/rkiattisak/salaly-prediction-for-beginer?resource=download)

We employ an Extract, Transform, Load (ETL) process using SQLAlchemy to store this data within a PostgreSQL database

### Model Selection

We will select an appropriate machine learning algorithm from Scikit-learn to construct the salary prediction model, basing our decision on the dataset's characteristics and the prediction problem's nature.

Our predictive model is crafted using both multiple linear regression and random forest regression methods. These models take into account demographic factors as input and yield anticipated salary as output. Our assessment of the model's performance involves the R-squared (R2) score and mean squared error (MSE) metrics.

### Model Training and Evaluation

The selected machine learning model will be trained using the pre-processed dataset. We will split the data into training and testing sets to evaluate the model's performance. Various evaluation metrics such as R-Squared value (R2) and Mean Squared Error (MSE) will be used to assess the model's accuracy.

The hyperparameters of the models are fine-tuned using GridSearchCV to improve their predictive capabilities.

The Multi Linear Regression model achieves an R2 score of 0.9027 with a Mean Squared Error of 233355401.45166123. In contrast, the Random Forest Regressor model achieves an R2 score of 0.8463 with a Mean Squared Error of 368548719.23786736.

It was decided that the Multi Linear Regression model was more accurate due to the higher R2 score.

### Data Visualization

We will create a Tableau dashboard to visualize the relationships between demographic factors, years of experience, educational qualifications, and predicted salaries. The dashboard will provide insights into the factors that contribute to salary predictions and help users explore the data interactively. [Salary Prediction Dashboard](https://public.tableau.com/app/profile/basudeb.ghosh/viz/Project4_update/Story1)

### Deployment

An upcoming enhancement involves deploying the web application and machine learning model via cloud services like Google Cloud SQL, Amazon AWS, or another fitting platform. This advancement aims to provide users with a more intuitive and interactive experience. Through the deployed application, users will be able to easily input their years of experience, education level, department, and seniority. Subsequently, they will receive a salary prediction derived from the trained model, enhancing user-friendliness and interactivity.

### Documentation

Throughout the project, we will maintain clear and detailed documentation of the entire process. This documentation will include the steps taken for data preprocessing, the rationale behind model selection, details of model training and evaluation, creation of the Tableau dashboard, deployment process, and any challenges faced during the project. The complete project, including code, documentation, and relevant files, will be made available to the public via a GitHub repository.

The GitHub repository for this project can be found at:
[ML Salary Prediction Repository](https://github.com/sandhalie/ML_salary_prediction)

## Conclusion

The Predicting Salary based on Demographic Factors and Experience project aims to develop an accurate machine learning model that can predict salaries based on various input factors. Through thorough data analysis, model training, and deployment, we intend to provide a valuable tool for individuals and organizations seeking insights into salary predictions.

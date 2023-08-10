# Predicting Salary based on Demographic Factors and Experience

## Introduction

Welcome to our machine learning project, where we embark on a journey to forecast salaries by leveraging a blend of experience years, department, job title seniority, and qualification levels. This endeavor encompasses the complete spectrum of data-driven salary prediction, spanning data collection, model curation, training and assessment, insightful data visualization, and comprehensive documentation.

Note:  In an effort to ensure fairness and eliminate potential biases, we have made a deliberate decision to exclude age and gender from our predictive model. This approach aligns with our commitment to creating a transparent and unbiased salary prediction system.

## Methodology

### Data Collection

Our data foundation is meticulously crafted, procuring a dataset that encapsulates critical details, including salaries, educational qualifications, and experience years. This dataset is sourced from Kaggle and can be accessed via the following link:
[Salary Prediction Dataset](https://www.kaggle.com/datasets/rkiattisak/salaly-prediction-for-beginer?resource=download)

We employ an Extract, Transform, Load (ETL) process using SQLAlchemy to store this data within a PostgreSQL database

### Pre-requisites and Setup

PostgreSQL Setup:
Install PostgreSQL: Ensure you have PostgreSQL installed on your machine. If not, download and install it from the official PostgreSQL website.
Database Setup: Create a PostgreSQL database named salary_data.
Table Setup: Execute the following SQL command to create a table named salary_data

CREATE TABLE salary_data (
    Age NUMERIC,
    Gender VARCHAR(10),
    "Education Level" VARCHAR(50),
    "Job Title" VARCHAR(100),
    "Years of Experience" NUMERIC,
    Salary NUMERIC,
    Department VARCHAR(100),
    Seniority NUMERIC
);



Alright, first I'll examine the structure of the Salary Data.csv file to determine the exact format, column names, and data types. After that, I'll provide SQL code to create a table matching the format of the CSV. Finally, I'll integrate this information into the README.

Finished working
Show work
I apologize for the oversight. I forgot to import the necessary libraries to handle the CSV. Let's correct that and examine the structure of the Salary Data.csv file again.

Finished working
Show work
Based on the structure of the Salary Data.csv file, we have the following columns:

Age (numeric)
Gender (text)
Education Level (text)
Job Title (text)
Years of Experience (numeric)
Salary (numeric)
Department (text)
Seniority (numeric)
Using this information, I will provide the SQL code to create a table matching this format in PostgreSQL. After that, I'll integrate this SQL code into the README.

Here's the SQL code to create a table named salary_data in PostgreSQL that matches the format of the CSV:

sql
Copy code
CREATE TABLE salary_data (
    Age NUMERIC,
    Gender VARCHAR(10),
    "Education Level" VARCHAR(50),
    "Job Title" VARCHAR(100),
    "Years of Experience" NUMERIC,
    Salary NUMERIC,
    Department VARCHAR(100),
    Seniority NUMERIC
);
You can run this SQL command in the PostgreSQL shell or use a tool like pgAdmin to create the table.

README
Project Overview
This project provides a Jupyter notebook that performs data analysis and visualization on salary data. The data is retrieved from a PostgreSQL database, cleaned, and analyzed to derive insights such as the average annual salary.

Pre-requisites and Setup
PostgreSQL Setup:
Install PostgreSQL: Ensure you have PostgreSQL installed on your machine. If not, download and install it from the official PostgreSQL website.
Database Setup: Create a PostgreSQL database named salary_data.
Table Setup: Execute the following SQL command to create a table named salary_data that matches the format of the provided dataset:
sql
Copy code
CREATE TABLE salary_data (
    Age NUMERIC,
    Gender VARCHAR(10),
    "Education Level" VARCHAR(50),
    "Job Title" VARCHAR(100),
    "Years of Experience" NUMERIC,
    Salary NUMERIC,
    Department VARCHAR(100),
    Seniority NUMERIC
);

Data Import: Import the data from Salary Data.csv into the salary_data table.
Connection Parameters: Ensure that the PostgreSQL database connection parameters (like username, password, and port) match your local setup. For this README, we assume the username and password are both set to "postgres" and the port is "5432". Adjust the connection string in the notebook if your setup is different.

Python and Jupyter Notebook Setup:
Python: Ensure you have Python 3.6 or newer installed. If not, download and install it from the official Python website.
Jupyter Notebook: If you don't have Jupyter Notebook installed, you can install it using pip install jupyter

Python Libraries: Install the required Python libraries using pip install pandas numpy plotly seaborn matplotlib scikit-learn sqlalchemy

Running the Notebook:

Navigate to the directory containing the Main.ipynb notebook.
Launch Jupyter Notebook by running the command:jupyter notebook

Once Jupyter starts, click on Main.ipynb to open the notebook.
Run the cells in sequence from top to bottom to execute the analysis and visualization tasks.


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

Throughout the project, we will maintain clear and detailed documentation of the entire process. This documentation will include the steps taken for data preprocessing, the rationale behind model selection, details of model training and evaluation, the creation of the Tableau dashboard, the deployment process, and any challenges faced during the project. The complete project, including code, documentation, and relevant files, will be made available to the public via a GitHub repository.

The GitHub repository for this project can be found at:
[ML Salary Prediction Repository](https://github.com/sandhalie/ML_salary_prediction)

## Conclusion

The Predicting Salary based on Demographic Factors and Experience project aims to develop an accurate machine learning model that can predict salaries based on various input factors. Through thorough data analysis, model training, and deployment, we intend to provide a valuable tool for individuals and organizations seeking insights into salary predictions.

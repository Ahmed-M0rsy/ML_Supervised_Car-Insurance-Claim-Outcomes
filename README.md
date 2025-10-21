# Car Insurance Claim Prediction

![Car Banner](car.jpg)

This project focuses on building a machine learning model to predict whether a customer will make a claim on their car insurance during the policy period. The goal is to identify the single most predictive feature to create a simple yet effective model for "On the Road," a car insurance company.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Results](#results)
- [Getting Started](#getting-started)
- [Dependencies](#dependencies)

## Project Overview

Insurance companies invest heavily in accurately pricing policies and predicting claims. This project assists "On the Road" insurance by analyzing their customer data to find the single feature that best predicts insurance claims. This allows them to deploy a simple, interpretable, and effective model. The performance of the model is measured by accuracy.

## Dataset

The data for this project is contained in the `car_insurance.csv` file. It includes various customer attributes.

**Dataset Columns:**

| Column | Description |
|---|---|
| `id` | Unique client identifier |
| `age` | Client's age group: 0: 16-25, 1: 26-39, 2: 40-64, 3: 65+ |
| `gender` | Client's gender: 0: Female, 1: Male |
| `driving_experience` | Years of driving experience: 0-9y, 10-19y, 20-29y, 30y+ |
| `education` | Client's level of education: none, high school, university |
| `income` | Client's income level: poverty, working class, middle class, upper class |
| `credit_score` | Client's credit score (0-1) |
| `vehicle_ownership` | Whether the client owns the vehicle: 0: No, 1: Yes |
| `vehicle_year` | Vehicle manufacturing year: before 2015, after 2015 |
| `married` | Marital status: 0: No, 1: Yes |
| `children` | Whether the client has children: 0: No, 1: Yes |
| `postal_code` | Client's postal code |
| `annual_mileage` | Miles driven annually |
| `vehicle_type` | Type of vehicle: sedan, sports car |
| `speeding_violations` | Number of speeding violations |
| `duis` | Number of DUIs |
| `past_accidents` | Number of past accidents |
| `outcome` | Whether a claim was made: 0: No, 1: Yes |

## Methodology

The analysis was conducted in the `notebook.ipynb` Jupyter Notebook. The process involved:

1.  **Data Loading and Exploration:** The `car_insurance.csv` dataset was loaded and examined to understand its structure and features.
2.  **Data Preprocessing:** Missing values in the dataset were identified and handled during model fitting and evaluation.
3.  **Model Training and Evaluation:**
    * A Logistic Regression model was chosen for this classification task.
    * The model was trained and evaluated for each individual feature to determine its predictive power.
    * Accuracy was used as the primary metric to evaluate the performance of each model.

## Results

After training and evaluating a logistic regression model for each feature, the single best-performing feature was identified.

-   **Best Feature:** `driving_experience`
-   **Best Model Accuracy:** 77.71%

This indicates that a customer's driving experience is the most significant individual predictor of whether they will make an insurance claim.

## Getting Started

To get a local copy up and running, follow these simple steps.

1.  Clone the repository:
    ```sh
    git clone [https://github.com/your_username/your_repository.git](https://github.com/your_username/your_repository.git)
    ```
2.  Navigate to the project directory:
    ```sh
    cd your_repository
    ```
3.  Open the `notebook.ipynb` file in a Jupyter environment to see the full analysis.

## Dependencies

The following Python libraries are required to run the notebook:
-   pandas
-   numpy
-   scikit-learn

You can install them using pip:
```sh
pip install pandas numpy scikit-learn

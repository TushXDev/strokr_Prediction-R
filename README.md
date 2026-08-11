Markdown
# 🧠 Stroke Risk Prediction Model & Dashboard

> An end-to-end machine learning project in R that predicts the likelihood of a stroke based on clinical and demographic data, complete with an interactive Shiny web application.

## 📖 Overview
According to the World Health Organization (WHO), stroke is the 2nd leading cause of death globally, responsible for approximately 11% of total deaths. 

This project explores a healthcare dataset to identify the strongest predictors of stroke. It encompasses a complete data science pipeline: exploratory data analysis (EDA), rigorous data preprocessing, the training of multiple machine learning models (Logistic Regression, Random Forest, and Neural Networks), and the deployment of the winning model into an interactive user-facing dashboard.

**Author:** Tushar Kumar

---

## ✨ Key Features
* **Automated Data Pipeline:** Cleanses raw data, handles missing values (e.g., mean imputation for BMI), and applies one-hot encoding for categorical variables.
* **Tidymodels Integration:** Utilizes the `tidymodels` ecosystem for consistent recipe creation, model training, and performance evaluation.
* **Algorithm Comparison:** Benchmarks Logistic Regression, Random Forest, and a Multi-Layer Perceptron (Neural Network) against each other using accuracy, sensitivity, specificity, and precision.
* **Interactive Shiny Dashboard:** A fully deployed web interface allowing users to input patient demographics, health metrics, and lifestyle factors to receive a real-time stroke probability.

---

## 🛠️ Tech Stack & Libraries
* **Language:** R
* **Data Manipulation & Cleaning:** `tidyverse`, `dplyr`, `janitor`, `fastDummies`
* **Machine Learning:** `tidymodels`, `ranger` (Random Forest), `nnet` (Neural Network)
* **Deployment:** `shiny`

---

## 📊 Dataset description
The dataset (`stroke-data.csv`) provides relevant patient information, combining physiological metrics and lifestyle choices. 

**Primary Features:**
* **Demographics:** Age, Gender, Marital Status, Residence Type (Urban/Rural)
* **Health Metrics:** BMI, Average Glucose Level, Hypertension (Binary), Heart Disease (Binary)
* **Lifestyle:** Work Type, Smoking Status

---

## 🚀 Installation & Setup

To run this project locally, you will need R and RStudio installed.

**1. Clone the repository and navigate to the project directory:**
```bash
git clone [https://github.com/yourusername/stroke-prediction-r.git](https://github.com/yourusername/stroke-prediction-r.git)
cd stroke-prediction-r
2. Install required R packages:
Open R or RStudio and run the following command to install all necessary libraries:

R
install.packages(c("tidyverse", "readxl", "janitor", "fastDummies", "tidymodels", "shiny", "ranger", "nnet"))
3. Run the Analysis:

Open the RMarkdown file (stroke_prediction.Rmd).

Run the chunks sequentially or click Knit to generate the final HTML Data Analysis Report.

Note: Ensure the dataset path in read_csv("D:/Stroke_prediction/stroke-data.csv") is updated to match your local directory structure.

4. Launch the Shiny App:

The deployment script requires the trained logistic regression model saved as lg_model.rds in the same directory.

Run the Shiny application code block or execute shiny::runApp() in the directory containing your UI/Server script.

📈 Findings & Conclusions
Core Predictors: Exploratory analysis revealed that clinical metrics—specifically hypertension, existing heart disease, and average glucose levels—are the strongest primary predictors of stroke risk.

Model Performance: After evaluating three distinct architectures, Logistic Regression achieved the best overall performance on the test data, scoring the highest in both Accuracy and Sensitivity (Recall).

Complexity vs. Performance: The Random Forest performed adequately as a runner-up, while the Neural Network demonstrated that simpler, highly interpretable models often perform better on structured tabular clinical data.

Disclaimer: The resulting dashboard is an analytical tool based on machine learning and is strictly for educational/demonstrative purposes. It does not constitute professional medical advice.

📂 Project Structure
Plaintext
├── data/
│   └── stroke-data.csv        # Raw dataset
├── stroke_prediction.Rmd      # Main RMarkdown file with analysis and model training
├── lg_model.rds               # Exported Logistic Regression model weights
├── app.R                      # Shiny dashboard script (if extracted from Rmd)
└── README.md                  # Project documentation

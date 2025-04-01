# PROJECT_ML_JOAQUINVILLAR_ONLINE_DS_THEBRIDGE

## Loan Classification

### 1. Objective 🎯
In this Machine Learning project, the goal is to develop a model that predicts the probability of a credit applicant defaulting on their loan, based on a dataset of clients who have already been granted a loan.

The objective is to identify clients with a high risk of defaulting on their payments, in order to avoid granting loans to similar profiles in the future, thus minimizing credit losses. On the other hand, the model will also help identify good clients, who have repaid or are in the process of repaying their loans, to grant them loans in the future.

### 2. Dataset 📊
The dataset used was obtained from Kaggle and contains information about loans granted to clients, with their respective characteristics and payment status. You can access the dataset here.

The dataset includes information about clients who have repaid their loans (favorable situation) and clients who have defaulted on their loans (unfavorable situation).

Model objective: Identify defaulting clients (class 0, "charged-off") and avoid granting them loans in the future, while rewarding good payers.

### 3. Methodology 📝
- **Data Preprocessing**: The dataset presents an imbalance in the target variable (indicating whether the loan was defaulted or not). The UnderSampling technique was used to balance the data, i.e., reducing the number of examples from the majority class (clients who repaid) to improve model performance.

- **Models used**:

    - **Logistic Regression**: To evaluate the relationship between client features and the probability of default.

    - **Random Forest**: An ensemble model to improve accuracy and robustness.

    - **XGBoost**: An advanced boosting algorithm to optimize predictions, which in this case provided superior performance.

- **Parameter Optimization**: A parameter optimization was performed using Grid Search techniques to improve the results obtained by the model. The final model was trained with the UnderSampling technique to ensure greater fairness in the classification of both classes.

- **Metrics used**:

    - **Confusion Matrix**: To evaluate the performance of the model.

    - **Recall of class 0 (Charged-off)**: Given the dataset imbalance, the recall of class 0 is especially important. We want to ensure that the model correctly identifies defaulting clients.

### 4. Repository Structure 📂
The repository has the following folder structure:
```
src/
│
├── data_sample/              # Muestra del dataset utilizado en el proyecto.
├── img/                      # Imágenes usadas en el proyecto.
├── notebooks/                # Notebooks usados para la experimentación.
├── results_notebook/         # Notebook final que resume todo el proceso.
├── models/                   # Modelos guardados en formato joblib.
└── utils/                    # Funciones y módulos auxiliares.
```

### 5. Video Presentation 🎥
The project also includes a video presentation of the results obtained, covering the following points:

- **Introduction to the problem**: Description of the importance of predicting which clients will not repay their loans to avoid losses.
  
- **Technical problem setup**: How Machine Learning is used to classify clients based on their risk of default.

- **Dataset description**: A brief description of the dataset characteristics and the Exploratory Data Analysis (EDA) process performed.

- **Results**: Comparison between the models tested (Logistic Regression, Random Forest, XGBoost) and justification for the selection of the final model.

- **Conclusions and future improvements**: Reflection on how the model can be improved in the future and decisions that will be made based on the results.

### 6. Final Model 🏆
The final model has been saved in joblib format for later use and deployment.

### 7. Conclusion 💡
This project demonstrates how to apply Machine Learning techniques to real-world problems, in this case, the classification of clients based on their ability to repay loans. Thanks to data analysis and modeling, it is possible to make more informed decisions and reduce the risk of losses in the financial sector.

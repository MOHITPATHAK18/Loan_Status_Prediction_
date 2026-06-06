📌 Project Overview
This project builds a Machine Learning model to predict whether a loan application will be approved or rejected, based on applicant information such as income, education, marital status, and credit history. A Support Vector Machine (SVM) with a linear kernel is used as the classification algorithm.
This type of model can assist financial institutions in automating and streamlining their loan approval process — reducing manual effort and improving decision consistency.

🎯 Objective

Predict the Loan Approval Status (Approved / Rejected) for an applicant based on demographic and financial features using a supervised classification approach.


📂 Dataset

Source: Analytics Vidhya – Loan Prediction Dataset
File Used: train_u6lujuX_CVtuZ9i.csv
Records: ~614 rows | Features: 12 columns

FeatureDescriptionLoan_IDUnique Loan IdentifierGenderMale / FemaleMarriedApplicant Marital StatusDependentsNumber of DependentsEducationGraduate / Not GraduateSelf_EmployedYes / NoApplicantIncomeMonthly Income of ApplicantCoapplicantIncomeMonthly Income of Co-ApplicantLoanAmountLoan Amount RequestedLoan_Amount_TermTerm of Loan in MonthsCredit_HistoryCredit History (1 = Good, 0 = Bad)Property_AreaRural / Semiurban / UrbanLoan_Status✅ Target Variable (Y = Approved, N = Rejected)

🔧 Tech Stack
Tool / LibraryPurposePython 3.8+Core programming languagePandasData loading, cleaning & manipulationNumPyNumerical computationsSeabornData visualizationScikit-learnML model (SVM), train-test split, accuracy scoreJupyter NotebookDevelopment & experimentation environment

🔄 Project Workflow
📥 Data Collection
       ↓
🔍 Exploratory Data Analysis (EDA)
       ↓
🧹 Data Preprocessing
   ├── Drop missing values
   ├── Label encoding (Y/N → 1/0)
   └── Encode categorical features
       ↓
📊 Data Visualization
   ├── Education vs Loan Status
   ├── Marital Status vs Loan Status
   ├── Gender vs Loan Status
   └── Self-Employment vs Loan Status
       ↓
✂️ Train-Test Split (90:10 | Stratified)
       ↓
🤖 Model Training — SVM (Linear Kernel)
       ↓
📈 Model Evaluation (Accuracy Score)

📊 Data Preprocessing Steps

Missing Value Handling — Rows with null values were dropped using dropna()
Label Encoding — Target variable Loan_Status: Y → 1, N → 0
Dependents — Replaced 3+ with numeric value 4
Categorical Encoding — Converted the following features to numeric:

FeatureMappingGenderMale → 1, Female → 0MarriedYes → 1, No → 0Self_EmployedYes → 1, No → 0EducationGraduate → 1, Not Graduate → 0Property_AreaRural → 0, Semiurban → 1, Urban → 2

📈 Data Visualization
Seaborn countplot was used to explore relationships between categorical features and loan approval:

📚 Education vs Loan Status
💍 Marital Status vs Loan Status
🚻 Gender vs Loan Status
💼 Self Employment vs Loan Status


🤖 Model — Support Vector Machine (SVM)

Algorithm: Support Vector Classifier (sklearn.svm.SVC)
Kernel: Linear
Train-Test Split: 90% Training / 10% Testing
Stratified Sampling: Ensures class distribution is preserved in both sets


📉 Model Performance
DatasetAccuracyTraining Data~79–82%Test Data~83% (varies by run)

📝 Accuracy may vary slightly due to random state and dataset version.


🚀 Getting Started
1. Clone the Repository
bashgit clone : (https://github.com/MOHITPATHAK18/Loan_Status_Prediction_)
cd loan-status-prediction-ml
2. Install Dependencies
bashpip install numpy pandas seaborn scikit-learn jupyter
3. Add the Dataset
Download the dataset from Analytics Vidhya and place it in the project root as:
train_u6lujuX_CVtuZ9i.csv
4. Run the Notebook
bashjupyter notebook Loan_Status_Prediction_using_ML.ipynb

📁 Project Structure
loan-status-prediction-ml/
│
├── Loan_Status_Prediction_using_ML.ipynb   # Main Jupyter Notebook
├── train_u6lujuX_CVtuZ9i.csv               # Dataset (add manually)
└── README.md                               # Project Documentation

💡 Key Learnings

Applied end-to-end supervised ML pipeline from raw data to model evaluation
Handled real-world messy data with missing values and categorical encoding
Explored feature relationships through data visualization
Implemented SVM — a powerful linear classification algorithm
Used stratified train-test splitting to maintain class balance


🔮 Future Improvements

 Try other ML algorithms — Logistic Regression, Random Forest, XGBoost
 Perform hyperparameter tuning using GridSearchCV
 Add cross-validation for more robust evaluation
 Build a simple web app using Flask / Streamlit for real-time predictions
 Handle class imbalance using SMOTE or class weights


👤 Author
Mohit Pathak

🎓 BCA Graduate — Aryabhatta Knowledge University
💼 Aspiring Data Analyst
🐙 GitHub: @MOHITPATHAK18
🔗 LinkedIn: mohit-pathak


📜 License
This project is open-source and available under the MIT License.

⭐ If you found this project helpful, please give it a star! ⭐

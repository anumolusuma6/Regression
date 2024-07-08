# Linear Regression Model for Toxicant Exposure Estimation
### Overview
This project aims to predict exposure to a hypothetical toxicant, assessed through urinary concentration, based on employee data and other variables that are easier to measure. The model utilizes linear regression and dummy variables to predict exposure levels without the need for urine sample analysis.

### Data Description
- Employees Dataset
  
Employee: Unique employee identifier

JobCategory: Numerical code (1-4) for job category

Sex: Gender of the employee (M/F)
Shift: Work shift (AM = morning; PM = afternoon).
Status: Employment status (PT = Part-time; FT = Full-time).
Age: Age of the employee at the time of biomarker sample collection.
YearsExperience: Years the employee has worked at the company.
StartAge: Age of the employee at the start of employment.
- Exposures Dataset
Employee: Unique employee identifier
PPE: Type of personal protective equipment used (None, Resp = Respirator, Mask = Face Mask)
UrineConcentration: Concentration of toxicant in urine sample collected at the end of the work shift
### Project Steps
- Data Preparation

Sort and merge Employees and Exposures datasets by the Employee variable to create a combined dataset (COMBINED).
- Exploratory Data Analysis

Generate a QQ plot using SciPy for the UrineConcentration variable in the COMBINED dataset.
Log-transform the UrineConcentration variable to Log_Concentration.
- Correlation Analysis

Calculate correlation matrices for continuous variables (Age, YearsExperience, StartAge) and UrineConcentration.
Model Development

Create dummy variables for categorical variables (JobCategory, Shift, Status, Sex, PPE) in the evaluation dataset.
Develop a linear regression model to predict UrineConcentration based on selected independent variables.
- Model Evaluation

Use the independent dataset (Evaluation.xlsx) to evaluate model predictions.
Create a scatter plot to visualize actual versus predicted UrineConcentration.
### Files Included
Employees.csv: Dataset containing employee information.
Exposures.csv: Dataset containing exposure and urine concentration data.
Evaluation.xlsx: Independent dataset for model evaluation.
### Technologies Used
Python (Pandas, NumPy, SciPy, Matplotlib/Seaborn)
Jupyter Notebook (optional for interactive analysis)
Git (version control)
### Usage
To replicate the analysis:

Clone this repository.
Install necessary dependencies.
Execute the provided scripts or notebooks to perform data preprocessing, model development, evaluation, and visualization.
### Contributing
Contributions are welcome! Please feel free to submit issues or pull requests for improvements.

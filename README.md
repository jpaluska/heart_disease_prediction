# Heart Disease Prediction

This project aims to predict the presence of heart disease in patients based on various medical attributes. The dataset used contains information about patients such as age, sex, chest pain type, blood pressure, cholesterol levels, and more.

## Dataset

The dataset used in this project is the Heart Disease Prediction Dataset from Kaggle. It contains 1328 instances with 14 attributes.

## Exploratory Data Analysis (EDA)

The project begins with a thorough EDA, which includes:
- Checking for missing values
- Analyzing the distribution of the target variable
- Visualizing the relationships between different attributes and the target variable
- Checking for correlations between attributes

## Model Building

Several machine learning models were trained and evaluated on this dataset:
1. Logistic Regression
2. Decision Tree
3. Random Forest
4. Support Vector Machine (SVM)

The models were evaluated using various metrics such as accuracy, precision, recall, and F1-score. Cross-validation was used to assess the models' performance.

## Model Evaluation and Improvement

The initial models showed signs of overfitting, particularly the Decision Tree and Random Forest. To address this, noise was added to the data to check the models' robustness.

Hyperparameter tuning was performed on the SVM model using RandomizedSearchCV to find the best parameters. 

Feature engineering was also applied by adding polynomial interaction terms, which improved the SVM model's performance.

## Model Interpretation

Feature importance was used to interpret the final tuned SVM model. This provided insights into which features were most important in predicting heart disease.

## Results

The final tuned SVM model with polynomial features achieved an accuracy of 94% on the test set, even with added noise. The model's performance was validated using cross-validation with data shuffling.

## Usage

The trained model is packaged and can be used to predict the risk of heart disease for new patients. A sample function `predict_heart_disease` is provided, which takes in patient attributes and returns the predicted risk.

## Future Work

Potential future enhancements could include:
- Collecting more data to further validate the model
- Exploring other advanced machine learning techniques such as Gradient Boosting
- Incorporating expert medical knowledge to guide feature selection and engineering

## Conclusion

This project demonstrates the application of machine learning to predict heart disease risk based on patient attributes. The systematic approach of data exploration, model building, evaluation, and interpretation provides a solid foundation for further development.


==============================
## DATASET INFORMATION

Target: The target column serves as the outcome variable and indicates the presence of heart disease in the patient. A value of 0 signifies the absence of heart disease, while a value of 1 indicates the presence of heart disease.

Age: The age of the patient.

Sex: The gender of the patient.

Chest pain type: A categorical attribute indicating the type of chest pain experienced by the patient. It has four possible values.

Resting blood pressure: The resting blood pressure of the patient.

Serum cholesterol: The serum cholesterol level in mg/dl of the patient.

Fasting blood sugar: Indicates whether the patient's fasting blood sugar is greater than 120 mg/dl.

Resting electrocardiographic results: A categorical attribute representing the results of the resting electrocardiogram. It has three possible values.

Maximum heart rate achieved: The maximum heart rate achieved by the patient.

Exercise induced angina: Indicates whether the patient experienced angina (chest pain) induced by exercise.

Oldpeak: ST depression induced by exercise relative to rest.

Slope: The slope of the peak exercise ST segment.

Number of major vessels: Represents the number of major blood vessels colored by fluoroscopy (ranging from 0 to 3).

Thal: A categorical attribute indicating the thalassemia type of the patient. It has three possible values: 0 for normal, 1 for fixed defect, and 2 for reversible defect.

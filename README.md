# Stroke Prediction Using Machine Learning

## Project Description
This project aims to predict the likelihood of a stroke based on patient characteristics such as gender, age, medical history, and smoking status. The dataset includes one dependent variable (`stroke`) and seven independent variables. Since the dataset is imbalanced, techniques such as SMOTE were applied, and models were further improved through hyperparameter optimization.

---

## Dataset
- **Source**: CSV file (309 KB)
- **Target Variable**: `stroke` (binary classification - stroke occurrence)
- **Key Features**:
  - Missing `bmi` values were filled with the mean.
  - Features were scaled using both normalization and standardization.

---

## Data Preprocessing
1. **Missing Data Handling**:  
   - Replaced missing values in the `bmi` column with the mean.
2. **Scaling**:  
   - Standardization applied to `age`, `bmi`, and `avg_glucose_level`.  
   - Normalization additionally applied to `avg_glucose_level`.
3. **Feature Selection**:  
   - Performed correlation analysis and Recursive Feature Elimination (RFE) to identify the most significant features.

---

## Models Used
- **K-Nearest Neighbors (KNN)**
- **Support Vector Machines (SVM)**
- **Logistic Regression**
- **Decision Tree Classifier**

### Hyperparameter Optimization
- **GridSearchCV** was used for parameter tuning.  
- Overfitting issues observed in KNN and Decision Tree models were reduced by adjusting hyperparameters.

---

## Results
- **SVM** achieved the best performance in terms of accuracy, precision, recall, and F1-score.  
- **KNN** required manual parameter adjustments due to GridSearchCV limitations.  

---

## How to Run
1. Clone the repository:  
   ```bash
   git clone <repository_link>
   cd <repository_name>

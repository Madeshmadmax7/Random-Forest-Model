# Model Evaluation with Cross-Validation and Random Forest

This project focuses on evaluating machine learning models using K-Fold and Stratified K-Fold Cross-Validation.  
The primary model used is Random Forest, and its performance is compared against Support Vector Machine (SVM) and Decision Tree.

---

## Dataset

The project uses the Breast Cancer Wisconsin Diagnostic Dataset.

### Dataset Sources
- Kaggle version:  
  https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data

### Dataset Details
- Total samples: 569  
- Features: 30 numerical features  
- Target labels:  
  - 1 → Malignant  
  - 0 → Benign  

---

## Project Objectives

- Implement K-Fold Cross-Validation  
- Implement Stratified K-Fold Cross-Validation  
- Train and evaluate a Random Forest classifier  
- Perform hyperparameter tuning using GridSearchCV  
- Compare model performance with Decision Tree and SVM  
- Evaluate using accuracy, precision, recall, F1-score, confusion matrix, and ROC curve  
- Visualize performance using bar charts and matrix plots  

---

## Preprocessing Summary

- Loaded the Breast Cancer dataset from CSV  
- Removed irrelevant columns (`id`, `Unnamed: 32`)  
- Converted diagnosis labels (M/B) to numerical values (1/0)  
- Separated features (X) and target (y)  
- Applied feature scaling for SVM using StandardScaler  

---

## Models Used

- Random Forest Classifier  
- Support Vector Machine (RBF kernel)  
- Decision Tree Classifier  

Random Forest was further optimized through hyperparameter tuning.

---

## Cross-Validation Methods

### K-Fold Cross-Validation
- Dataset divided into 5 folds  
- Each fold used once as a test set  
- Produces a reliable mean accuracy score  

### Stratified K-Fold Cross-Validation
- Ensures each fold maintains the original class distribution  
- More appropriate for imbalanced classification tasks  

---

## Final Model Performance (Cross-Validation)

| Model            | Mean Accuracy |
|------------------|---------------|
| Random Forest    | ~0.9526       |
| SVM              | ~0.9772       |
| Decision Tree    | ~0.9104       |

SVM achieved the highest accuracy, with Random Forest close behind.

---

## Visualizations

The project includes the following visualizations:

- Confusion Matrix for the Random Forest classifier  
- ROC Curve with AUC score  
- Horizontal bar chart comparing model accuracy with high decimal precision  

---

## Hyperparameter Tuning

Random Forest hyperparameters were tuned using GridSearchCV.  
The following parameters were optimized:

- Number of trees  
- Maximum depth  
- Minimum samples per split  
- Minimum samples per leaf  

### Best Parameters Identified
- `n_estimators = 200`  
- `max_depth = None`  
- `min_samples_split = 5`  
- `min_samples_leaf = 1`  

---

## Conclusion

This project demonstrates the importance of using cross-validation techniques for reliable machine learning model evaluation.  
SVM produced the highest accuracy, while Random Forest showed strong performance and stability, particularly after tuning.  
Decision Tree performed moderately but exhibited higher variance and signs of overfitting.

The overall workflow includes preprocessing, model training, cross-validation, hyperparameter tuning, evaluation, and visualization, providing a complete approach to model assessment.

---

## Author

Machine Learning Model Evaluation Project  
Contributions and suggestions are welcome.

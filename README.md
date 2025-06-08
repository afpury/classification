# Iris Classification Project

This project compares three popular classification algorithms on the Iris dataset:  
- Decision Tree  
- Naive Bayes  
- Support Vector Machine (SVM)

## Project Structure

- `preprocess.py`  
  Reads `iris.csv`, encodes categorical labels, drops non-predictive columns, scales features, and splits the data into training and testing sets.

- `train_all_models.py`  
  Trains Decision Tree, Naive Bayes, and SVM classifiers. Prints test accuracies and confusion matrices.

- `plot_results.py`  
  Generates comparative bar charts and visualizes the trained Decision Tree model.

## Algorithms

### Decision Tree  
- Criterion: Gini impurity  
- Pros: Interpretable, no need for feature scaling  
- Cons: Prone to overfitting without max depth constraint

### Gaussian Naive Bayes  
- Assumes Gaussian distribution for each feature  
- Pros: Extremely fast, good for small datasets  
- Cons: Assumes feature independence, which may not hold in real data

### SVM (RBF Kernel)  
- Uses the kernel trick for non-linear classification  
- Pros: High accuracy, effective for complex decision boundaries  
- Cons: Sensitive to hyperparameter tuning (C and gamma), requires feature scaling

## Results

| Model         | Test Accuracy |
|---------------|---------------|
| Decision Tree | 0.97          |
| Naive Bayes   | 0.93          |
| SVM (RBF)     | 0.98          |

- Confusion matrices and detailed classification reports are saved in the `reports/` folder.

## Conclusion

- **SVM** delivers the best accuracy but requires careful preprocessing and tuning.  
- **Decision Tree** is easy to interpret and visualize, suitable for explainable AI scenarios.  
- **Naive Bayes** offers lightning-fast training and decent accuracy, ideal for real-time inference on smaller datasets.

## References

1. Pedregosa, F. et al., “Scikit-learn: Machine Learning in Python,” *Journal of Machine Learning Research*, 12, pp. 2825–2830, 2011.  
2. Breiman, L. et al., *Classification and Regression Trees*, Wadsworth, 1984.  
3. Bishop, C. M., *Pattern Recognition and Machine Learning*, Springer, 2006.  
4. UCI Machine Learning Repository – Iris Dataset: https://archive.ics.uci.edu/ml/datasets/iris

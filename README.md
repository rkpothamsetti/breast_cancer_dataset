
Breast Cancer Prediction using Logistic Regression
==================================================

This project demonstrates how to build and evaluate a logistic regression classifier on the Breast Cancer Wisconsin dataset.

---------------------------
1. Dataset Preparation
---------------------------
- Dataset columns include various statistical measurements of cell nuclei.
- Target variable: `diagnosis`
    - 'M' = Malignant (encoded as 1)
    - 'B' = Benign (encoded as 0)
- Irrelevant columns like `id` and `Unnamed: 32` are dropped.

---------------------------
2. Preprocessing Steps
---------------------------
- Features (X) and Target (y) are separated.
- Dataset is split into 80% training and 20% testing using `train_test_split()`.
- All features are standardized using `StandardScaler` for better model convergence.

---------------------------
3. Model Training
---------------------------
- A `LogisticRegression` model is trained on the standardized training data.
- The model is then used to predict on the test set.

---------------------------
4. Model Evaluation
---------------------------
- Metrics used:
  - Confusion Matrix
  - Classification Report (Precision, Recall, F1-Score)
  - ROC-AUC Score
- The ROC Curve is plotted to visualize the trade-off between True Positive Rate and False Positive Rate.

---------------------------
5. Threshold Tuning
---------------------------
- The default threshold of 0.5 is adjusted to 0.3 to increase sensitivity.
- New predictions (`y_custom_pred`) are generated based on this custom threshold.
- The model is re-evaluated using the same set of metrics to understand the impact of threshold change.

---------------------------
6. Sigmoid Function
---------------------------
- The logistic regression model uses the sigmoid function to convert linear outputs into probabilities:
  σ(z) = 1 / (1 + e^(-z))
- This allows binary classification by setting a threshold (typically 0.5 or tuned value).

---------------------------
How to Run
---------------------------
1. Install required packages:
   pip install pandas numpy matplotlib scikit-learn

2. Load your dataset into a DataFrame:
   df = pd.read_csv("your_dataset.csv")

3. Copy and paste the code blocks from the notebook/script in order.

4. Observe the evaluation metrics and ROC plot for model performance.

---------------------------
Optional Improvements
---------------------------
- Use cross-validation for robust performance estimation.
- Try different thresholds and evaluate precision-recall trade-offs.
- Explore other classifiers (RandomForest, SVM, etc.) for comparison.

# breast_cancer_dataset

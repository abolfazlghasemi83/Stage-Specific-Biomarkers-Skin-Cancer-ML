Prerequisites

Install the required Python libraries before running the pipeline.

Required Libraries:

    pandas
    numpy
    scikit-learn
    scipy
    openpyxl
    xgboost
    imbalanced-learn
    tensorflow

Example:

pip install pandas numpy scikit-learn scipy openpyxl \
            xgboost imbalanced-learn tensorflow



Algorithm 1: Machine Learning Pipeline for Biomarker Identification

Input:
    Dataset_Path
    Target_Column = "target"

Output:
    Excel file containing:
        • Model Name
        • Top 20 Biomarkers
        • Normalized Feature Importance
        • Accuracy
        • Precision

──────────────────────────────────────────────────────────────
Step 1. Load Dataset
──────────────────────────────────────────────────────────────

Procedure LOAD_DATA(Path, Target_Column)

    Read Excel dataset

    IF Target_Column exists THEN
        X ← all predictor variables
        y ← target column
    ELSE
        X ← all columns except last
        y ← last column
    END IF

    IF y contains categorical labels THEN
        Encode labels into integers
    END IF

    Return X, y, Feature_Names

End Procedure


──────────────────────────────────────────────────────────────
Step 2. Feature Importance Estimation
──────────────────────────────────────────────────────────────

Procedure FEATURE_IMPORTANCE(Model, X, y)

    Fit Model using X and y

    IF Model provides coefficients THEN

        Importance ← absolute value of coefficients

        IF multiclass coefficients THEN
            Average coefficients across classes
        END IF

    ELSE IF Model provides feature_importances_ THEN

        Importance ← feature_importances_

    ELSE

        Compute Permutation Importance

            Baseline ← Accuracy(Model, X)

            FOR each feature j

                Randomly shuffle feature j

                NewAccuracy ← Accuracy(Model)

                Importance(j) ← Baseline − NewAccuracy

            END FOR

    END IF

    Return Importance

End Procedure


──────────────────────────────────────────────────────────────
Step 3. Model Evaluation
──────────────────────────────────────────────────────────────

Procedure EVALUATE(Model, X, y)

    Perform Stratified 3-Fold Cross Validation

    Obtain predictions using Cross Validation

    Accuracy ← Accuracy Score

    Precision ← Weighted Precision Score

    Return Accuracy, Precision

End Procedure


──────────────────────────────────────────────────────────────
Step 4. Define Machine Learning Models
──────────────────────────────────────────────────────────────

Models ←

{
C5,
SVM,
Neural Network,
C&R Tree,
Feature Selection,
CHAID,
QUEST,
Time Series,
TCM,
Random Tree,
Tree-AS,
Decision List,
Linear,
Linear-AS,
Regression,
PCA/Factor,
Discriminant,
Logistic,
Generalized Linear,
GLMM,
GLE,
Cox,
Bayesian Network,
SLRM,
Apriori,
CARMA,
Sequence,
K-Means,
Kohonen,
TwoStep,
TwoStep-AS,
Anomaly Detection,
KNN,
STP,
Linear SVM
}


──────────────────────────────────────────────────────────────
Step 5. Execute All Models
──────────────────────────────────────────────────────────────

Standardize all features

FOR each Model in Models

    TRY

        IF Model = Anomaly Detection THEN

            Train only using positive samples

            Predict all samples

            Convert prediction labels

            Accuracy ← Compute Accuracy

            Precision ← Compute Weighted Precision

            Importance ← Vector of Ones

        ELSE

            Importance ← FEATURE_IMPORTANCE(Model)

            Accuracy, Precision ← EVALUATE(Model)

        END IF

        Normalize Importance

        Select Top 20 Features

        FOR each Selected Feature

            Save

                Model Name

                Feature Name

                Normalized Importance

                Accuracy

                Precision

        END FOR

    CATCH Exception

        Continue with next model

    END TRY

    Release Memory

END FOR


──────────────────────────────────────────────────────────────
Step 6. Export Results
──────────────────────────────────────────────────────────────

Export all collected records into

results_35models.xlsx

End Algorithm

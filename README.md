🍷 Wine Type Classification using Neural Networks
=================================================

This project builds a binary classification model using a neural network to distinguish between red and white wines based on their physicochemical properties. The dataset is sourced from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Wine+Quality).

📊 Dataset Overview
-------------------

The dataset contains chemical characteristics and quality ratings for red and white wines. Each row represents a wine sample with the following features:

| Feature                | Description                           |
|------------------------|---------------------------------------|
| fixed acidity          | Tartaric acid level                  |
| volatile acidity       | Acetic acid level                    |
| citric acid            | Citric acid content                  |
| residual sugar         | Remaining sugar after fermentation   |
| chlorides              | Salt concentration                   |
| free sulfur dioxide    | Free SO₂ level                       |
| total sulfur dioxide   | Total SO₂ level                      |
| density                | Liquid density                       |
| pH                     | Acidity level                        |
| sulphates              | Sulfate level                        |
| alcohol                | Alcohol percentage                   |
| quality                | Quality score (0–10)                 |
| type                   | 1 = Red wine, 0 = White wine         |

📌 Example entry:

| fixed acidity | volatile acidity | citric acid | ... | alcohol | quality | type |
|---------------|------------------|-------------|-----|---------|---------|------|
| 7.4           | 0.70             | 0.00        | ... | 9.4     | 5       | 1    |

🧠 Model Summary
----------------

The neural network is built using **Keras (TensorFlow backend)** and consists of:

*   **Input Layer**: 12 features
    
*   **Hidden Layers**: 2 dense layers (12 and 9 neurons) with ReLU activation
    
*   **Output Layer**: 1 neuron with sigmoid activation for binary classification
    

### 🔧 Preprocessing Steps:

*   Combine red and white wine datasets from UCI repository
    
*   Normalize features using StandardScaler
    
*   Stratified train-test split (70/30) to maintain class distribution
    
*   SMOTE was imported but not used in the final model due to performance considerations
    

### 📈 Model Evaluation:

*   **Loss Function**: Binary cross-entropy
    
*   **Optimizer**: Adam
    
*   **Metrics**: Accuracy
    
*   **Training**: 20 epochs, batch size of 16
    
*   **Evaluation**: Confusion matrix and classification report for precision, recall, and F1-score
    
*   **Overfitting Check**: Comparison of train and test accuracy to assess model generalization
    

### 📊 Visualization:

*   Histogram of alcohol content distribution for red and white wines
    
*   Confusion matrix visualization using Matplotlib


🔍 Results
----------

*   Training Accuracy: 99.67%
    
*   Testing Accuracy: 99.69%
    

📝 Notes
--------

*   The dataset is imbalanced, but SMOTE was not applied in the final model to avoid potential performance degradation.
    
*   The model can be further tuned by adjusting hyperparameters (e.g., number of epochs, batch size, or layer architecture).
    
*   Future improvements could include feature selection or experimenting with other models like Random Forest or XGBoost.
    

📚 References
-------------

*   [UCI Wine Quality Dataset](https://archive.ics.uci.edu/ml/datasets/Wine+Quality)
    
*   [Keras Documentation](https://keras.io/)
    
*   [Scikit-learn Documentation](https://scikit-learn.org/)


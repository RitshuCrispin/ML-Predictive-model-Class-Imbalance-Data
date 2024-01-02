# ML-Predictive-model-Class-Imbalance-Data
Predictive model for customer retention that measures F1 and AUC-ROC. Class balance techniques are applied: Subsampling and Threshold Adjustment.

# Project description
Beta Bank customers are leaving, little by little, every month. Bankers discovered that it is cheaper to save existing customers than to attract new ones.

## Objective 
Predict if a customer will leave the bank soon. You have the data on the past behavior of clients and the termination of contracts with the bank.

Create a model with the maximum *F1* value possible. To pass the review, you need an *F1* value of at least 0.59. Check F1 for the test set.

Additionally, you should measure the *AUC-ROC* metric and compare it to the *F1* value.

## Conclusions
1. In the initialization stage of the project, the data delivered was reviewed where it was observed that there were null values in the `tenure` column; However, it was validated that this did not impact the proportion of the target column, so it was decided to purge these values and thus have a clean dataset.
2. In the preparation of the dataset, the characteristic and objective variables were generated, all the data were transformed into numerical data applying One-Hot and scalar standardization techniques and finally, the dataset was segmented into 3 sets: training, validation and testing.
3. It was validated that there was an imbalance in the training classes in a proportion of 80% = 0 and 20% = 1. With this data imbalance we trained 3 models resulting in F1 probabilities that were not so low but with many prediction errors.
4. To balance the classes we apply 2 techniques: subsampling and threshold adjustment. For each of the techniques we trained the 3 models where the best model was the random forest applying the threshold adjustment to 0.345 and n_estimators=100. Obtaining a value F1= 0.635262.
5. Finally, we apply the best model obtained with the test set, achieving slightly more correct predictions and the following result:
     -F1: 0.48
     - ROC_AUC: 0.73

![output](https://github.com/RitshuCrispin/ML-Predictive-model-Class-Imbalance-Data/assets/130596539/9be300bb-9afe-44fe-a3d5-235d78353c07)

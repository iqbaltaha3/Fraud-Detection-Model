# Fraud-Detection-Model

The dataset contains 6,362,620 rows with various columns, including features like transaction type, amount, and balances, as well as the target variable isFraud.

To address the class imbalance problem, where fraudulent transactions are rare, I opted for downsampling. This technique involves reducing the number of samples from the majority class (non-fraudulent transactions) to match the number of samples in the minority class (fraudulent transactions). This creates a balanced dataset for training the model.

I transformed and prepared the features for the model, which included normalizing or scaling the transaction amounts and balances. This ensures that all features are on a similar scale, making it easier for the model to learn from the data.

I initially experimented with various algorithms including Decision Tree, Random Forest, SVM, and XGBoost. However, these algorithms were overfitting the data, meaning they were too closely fitting the training data and not generalizing well to new data. As a result, they were not suitable for this particular problem.

Therefore, I decided to use Logistic Regression for its simplicity and interpretability in binary classification problems. Logistic Regression estimates the probability of a transaction being fraudulent by applying a logistic function to a linear combination of input features.

I trained the Logistic Regression model on the balanced dataset created by downsampling the majority class. This involved fitting the model to the data and allowing it to learn the patterns associated with fraudulent transactions.

To assess the performance of the model, I used various metrics including accuracy, classification report, and confusion matrix:

Accuracy measures the proportion of correctly classified transactions. Classification Report provides details on precision, recall, and F1-score for both classes (fraudulent and non-fraudulent). Confusion Matrix shows the number of true positives, true negatives, false positives, and false negatives, giving a more detailed view of the model's performance. Based on these evaluation metrics, I may refine the model further by adjusting parameters or exploring other algorithms if necessary. The goal is to ensure the model effectively detects fraudulent transactions with a good balance between precision and recall.

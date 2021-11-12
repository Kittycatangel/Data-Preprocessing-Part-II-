# Data-Preprocessing-Part-II

## Train/test split

Comparing predictions to true labels in the test set can be understood as the unbiased performance evaluation of our model before we let it loose in the real world. In this blog, we will prepare a new dataset, the Wine dataset. After we have preprocessed the dataset, we will explore different techniques for feature selection to reduce the dimensionality of a dataset.

## Bring features into same scale : normalization and standardization

Feature scaling is a crucial step in our preprocessing pipeline that can easily be forgotten. Decision trees and random forests are two of the very few machine learning algorithms where we don’t need to worry about feature scaling. Those algorithms are scale-invariant. However, the majority of machine learning and optimization algorithms behave much better if features are on the same scale.

Now, there are two common approaches to bring different features onto the same scale: normalization and standardization.

## Selecting important features to avaid overfitting

If we notice that a model performs much better on a training dataset than on the test dataset, this observation is a strong indicator of overfitting. Overfitting means the model fits the parameters too closely with regard to the particular observations in the training dataset but does not generalize well to new data, and we say the model has a high variance. The reason for the overfitting is that our model is too complex for the given training data. Common solutions to reduce the generalization error are listed as follows:

• Collect more training data

• Introduce a penalty for complexity via regularization

• Choose a simpler model with fewer parameters

• Reduce the dimensionality of the data

### L1 and L2 regularization as penalties against model complexity

L2 regularization is one approach to reduce the complexity of a model by penalizing large individual weights, where we defined the L2 norm of our weight vector w.
It can be applied with machine learning models like logistic regression.

### Sequential feature selection algorithms

For machine leraning models where we can not use l1, l2 regularizers i.e., KNN classifier.
An alternative way to reduce the complexity of the model and avoid overfitting is dimensionality reduction via feature selection, which is especially useful for unregularized models. There are two main categories of dimensionality reduction techniques: feature selection and feature extraction. Via feature selection, we select a subset of the original features, whereas, in feature extraction, we derive information from the feature set to construct a new feature subspace.

### Assessing feature importance with random forests

Another useful approach to select relevant features from a dataset is to use a random forest. Using a random forest, we can measure the feature importance.







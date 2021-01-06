# k-Fold Cross-Validation

Cross Validation is a stastical model to evaluate the skill of machine learning models using limited data samples.
Click [here](https://machinelearningmastery.com/k-fold-cross-validation/#:~:text=Cross%2Dvalidation%20is%20a%20resampling,is%20to%20be%20split%20into. "k-Fold Cross-Validation") to know more.

## Procedure

- Shuffle the dataset randomly.
- Split the dataset into **k** groups.
- For **each** unique group:
    - Take the group as a hold out or **test data set**.
    - Take the remaining groups as a **training data set**.
    - Fit a model on the training set and evaluate it on the test set.
    - Retain the **evaluation score** and discard the model.
- Summarize the skill of the model using the sample of model evaluation scores.

**Note**: It is essential that any preparation of the data prior to fitting the model occur on the **assigned training dataset within the loop** rather than on the broader data set.

## Configuration of k

There are **three** common tactics for choosing the value of k:

- **Representative**: The value for k is chosen such that each train/test group of data samples is large enough to be statistically representative of the broader dataset.

- **k = 10**: The value for k is fixed to 10, a value that has been found through experimentation to generally result in a model skill estimate with low bias and a modest variance.

- **k = n**: The value for k is fixed to n, where n is the size of the dataset to give each test sample an opportunity to be used in the hold out dataset. This approach is called **leave-one-out cross-validation**.
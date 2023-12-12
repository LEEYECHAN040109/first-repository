# Data segmentation:
The train_test_split function randomly divides the given datasets X and y into training and test data.
The test_size=0.01 parameter represents the percentage of test data in the entire dataset; 1% of the total data is used as test data.
Random_state=0 is the seed value used for random segmentation, which results in the same random segmentation with multiple executions of the code.

**X_train, X_test, y_train, y_test = sklearn.model_selection.train_test_split(X, y, test_size=0.01, random_state=0)**

# Model learning and prediction:
The SVC model is used to build a support vector machine, where the gamma value is set to 1.0 to initialize the model.
Use the fit method to train SVC models using X_train and y_train.
Use the trained model to make predictions about the X_test data and store the results in the y_pred variable.

**svc_model = SVC(random_state=0, gamma=1.0)
svc_model.fit(X_train, y_train)
y_pred = svc_model.predict(X_test)

with open('svc_model.pkl', 'wb') as file:
    pickle.dump(svc_model, file)**

i chose this model because  know that the svc model is an effective model for text classification,
prediction in the field of image classification, and pattern recognition and shows strong performance on datasets for various kinds.

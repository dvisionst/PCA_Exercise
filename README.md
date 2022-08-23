# PCA_Exercise

## 1. Load the Data
You can load the dataset using this code:

load the dataset
from sklearn.datasets import fetch_openml
mnist = fetch_openml('mnist_784')
view the shape of the dataset
mnist.data.shapecopy
The dataset has shape (70000, 784), meaning we are working with 70,000 images with 784 dimensions!

Note that you can access the X data using `mnist.data` and access the target using `mnist.target`.

If you get an error using the above code, you can also load the data using:

from keras.datasets import mnist
load data
(X_train, y_train), (X_test, y_test) = mnist.load_data()
reshape data
X_train = X_train.reshape(X_train.shape[0], -1)
X_test = X_test.reshape(X_test.shape[0], -1)copy

## 2. Prepare the Data
Prepare the data for modeling.  Scale and apply PCA to your data, while retaining 95% of the variance.  Be sure not to leak information.



## 3. Create 2 KNN models. 
   a. One that that uses the PCA transformed data to predict which number each image shows.

   b. One that uses the original data, without the PCA transformation (but, remember you still need to scale the data!)



## 4. Evaluate and compare the models.  
Use separate cells to make predictions using each model.  Include the cell magic command: `%%time` at the top of your cells when making predictions to see which model can create predictions faster, the one trained on PCA data or the one trained on non-PCA data.  Evaluate both models using multiple appropriate metrics.



'%%time' will output under the cell a count of how long it takes the code in that cell to run.

%%time
preds_pca = pca_model.predict(X_test)copy
%%time
preds_no_pca = no_pca_model.predict(X_test)copy

## 5. Answer the Following Questions in Text:
   a. Which model performed the best on the test set?

   b. Which model was the fastest at making predictions?

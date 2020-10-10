# Hepatitis-C-detection-and-its-progress
Trained the model using dense neural network and predicted the presence of Hepatitis-C and its progress using hcv_dataset. It is a multi class classification with different classes explaining the presence of Hepatitis c and its progress.

# Preprocessing steps

Our target label is categorical variable Hepatitis C and it progress. There are 5 classes in the target varaible. There are 13 features, 615 records. Dropped the column unnamed from the dataset as all the values are unique ids.
There were missing values in ALB,ALP,ALT,CHOL,PROT columns. Imputed the missing values with their corresponding means.
Partitioned the data in to train,test splits using train_test_split from model selection. Used 80 percent for training the data and 20 percent for validation.Used random state to shuffle the data
Analysed the target variable of the dataset and found that the classes were imbalanced. For instance the category '0:Blood Donor' has count=533 (the highest) and the '0s: Suspect Blood Donar' count =7 (the lowest) in the entire 615 records.
In order to balance the classes , used oversampling method called SMOTE for the training data and trained using it.
# Analysis
Developed the models using different values for hyperparameters like different depths of network,width of the network, different activation functions. Applied l1,l2 regularization techniques as the models were overfitting(they seem to be memorizing the data records instead of learning the underlying pattern.SO, finally got the best accuarcy of 97 percent using L2- regularization and recall of 91.8 percent with prediction in all the classes.

# heart-disease-prediction-using-knn
Heart disease prevention has become more important than ever. In order to ensure that more people may live healthy lives, effective data-driven methods for 
predicting cardiac problems can enhance the overall research and preventive process. Machine learning is useful in this situation. 
The heart illnesses are predicted with the use of machine learning, and the forecasts are rather accurate.

The project involves the necessary data processing and analysis of the patient dataset for heart disease. The model in this project is trained using KNN algorithm

Why KNN(K-Nearest Neighbor)
The K-NN method makes the assumption that the new case and the existing cases are comparable, and it places the new instance in the category that is most like the
existing categories.A new data point is classified using the K-NN algorithm based on similarity after all the existing data has been stored. 
This means that applying the K-NN method, fresh data may be quickly and accurately sorted into a suitable category.

Goal: Determine if a patient should receive a heart disease diagnosis. This has a binary result.
Patient diagnosed with Heart Disease, positive = 1.
Patient not diagnosed with heart disease, negative = 0 

Steps 
Step 1. Importing required libraries and modules.

Step 2. Importing dataset with pandas library.

Step 3. Data exploration 

     => Exploring data set (information about data set)
     => Checking predictors attributes to understand columns better since no null value was observed in the previous step
     => Describing the dataset to get correlation between target attribute and predictor attributes.
     => checking length of target attribute (ie patient suffering from heart disease = 1 and not = 0) 
Step 4. Feature scaling (data visualization) 

     => to check the correlation of features in data set using seaborn library and matplotlib to plot the graph
     We can see there is a positive correlation between chest pain (cp) & target (our predictor). This makes sense since, the greater amount of chest pain 
     results in a greater chance of having heart disease. Cp (chest pain), is an ordinal feature with 4 values: 
     Value 1: typical angina ,Value 2: atypical angina, Value 3: non-anginal pain , Value 4: asymptomatic. 
     In addition, we see a negative correlation between exercise induced angina (exang) & our predictor. 
     This makes sense because when you exercise, your heart requires more blood, but narrowed arteries slow down blood flow.
    
     => Plotting histogram for every column attribute 
     It shows how each feature and label is distributed along different ranges, which further confirms the need for scaling. 
     Next, wherever you see discrete bars, it basically means that each of these is actually a categorical variable. 
     We will need to handle these categorical variables before applying Machine Learning. 
     
     =>converting some categorical variables into dummy variables and scaling all the values before training the Machine Learning models. 
     We use the get_dummies() method from pandas.
     Next, we need to scale the dataset for which we will use the StandardScaler. 
     The fit_transform() method of the scalar scales the data and we update the columns. 
     
     => Checking target class proximity 

Step 5. Splitting data into training and testing set in the ratio of 7:3 respectively => Checking size of testing and training set

KNN model 

This classifier looks for the classes of K nearest neighbors of a given data point and based on the majority class, it assigns a class to this data point. 
However, the number of neighbors can be varied. I varied them from 1 to 20 neighbors and calculated the test score in each case. 
     
     => Importing KNeighborsClassifier module from sklearn.neighbors library 
     => plotting graph for K values 
     => listing mean score values
     =>Support Vector Classifier 
By varying the distance between the data points and the hyperplane, this classifier seeks to create a hyperplane that can divide the classes as much as feasible. 
The hyperplane is chosen depending on a number of kernels. I experimented using the linear, poly, rbf, and sigmoid kernels.
In conclusion, the linear kernel scored 84.6% and had the best performance on this dataset.





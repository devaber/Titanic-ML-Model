# Titanic-ML-Model
building a model to predict if a passernger would survive at the titanic using logistic regression algorithm <br>
this work is done through google colab <br>
first upload the "titanic_ML(task) to colab, <br>
then on the side bar click right and choose "upload", <br>
to upload the "train" file <br>
now you're all ready to start! <br>
<h3>Importing the Dependencies</h3> <br>
in this section you just need to run the code written already <br>
<h3>Reading the data</h3> <br>
run the existing codes <br>
<h3>Data Preprocessing</h3> <br>
in this section we will set data by fixing it's flaws. <br>
<h6>Missing Vlaues</h6> <br>
we'll start with "Age" column and fill it with the mean value of "Age" calumn using <br>
the "filllna" function: <br>

```data['Age'] = data['Age'].fillna(data['Age'].mean())``` <br>

![image](https://github.com/user-attachments/assets/7dbe54ff-c0a5-4191-b729-09ed737b1ad4) <br>

then check how many missing values we have in the "Age" column, it should be zero <br>
do the same with "Emparked" column: <br>

```data['Embarked'] = data['Embarked'].fillna(data['Embarked'].mode())``` <br>

 ![image](https://github.com/user-attachments/assets/a2ee9cd5-b3db-4f99-8a52-ad1c989e74ee) <br>

<h6>Useless Columns</h6> <br>
Now drop the unnececary columns which are "Name","PassengerID": <br>

```data.drop('PassengerId', axis=1, inplace=True)``` <br>

```data.drop('Name', axis=1, inplace=True)``` <br>

![image](https://github.com/user-attachments/assets/ed520a48-dea7-4722-bcb8-4fd6cdc17c85) <br>

<h6>Duplicates</h6> <br>
check if there are any duplicates: <br>

```duplicateRows = data[data.duplicated()]```<br>

![image](https://github.com/user-attachments/assets/d32939e3-b89c-4d1e-94f8-e2c0476aaa5b) <br>

<6>Data Analysis</h6> <br>
here we'll explore data and their relationships <br>
run the codes to see the graphs showing the relation between data. <br>
<h3>Model Building</h3> <br>
in this section we'll split data into training and testing sets to build and evaluate our model<br>
using "train_test_split" function<br>

```train_test_split(data, test_size=None, train_size=None, random_state=None, shuffle=True, stratify=None)``` <br>

![image](https://github.com/user-attachments/assets/266ccb2d-d208-4a49-8b28-f220d5f81f1c) <br>

<h6>Model Training</h6> <br>
now the "logistic regression" algorithm will learn from training data to make predictions<br>

```from sklearn.linear_model import LogisticRegression``` <br>

```model = LogisticRegression()```<br>
 ![image](https://github.com/user-attachments/assets/0f07b7c0-40a9-47f8-b3c6-bb77c7e0ee9c) <br>

 <h3>Model Evaluation</h3> <br>
 Finally use the "accuracy score" to measure the proportion of correct predictions out of all predictions <br>
 ```from sklearn.metrics import accuracy_score``` <br>

 ```print("Your Logistic Regression model has an accuracy of {}".format(accuracy_score))```<br>

 ![image](https://github.com/user-attachments/assets/303db8dd-7c31-4030-9b10-c3d71ce7728d) <br>







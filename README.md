# Machine-Learning
These are some basic machine learning projects with some conceptual explanation we wil first start with something very basic i.e Linear Regression
## Linear Regression
Linear Regression model is one of simplest model. It uses the slope equation for training the model and find correlation between the Dependent Variables and  the Independent Variables 

Equation:
<a href="https://www.codecogs.com/eqnedit.php?latex=y&space;=&space;b_{0}&space;&plus;&space;b_{1}*x_{1}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?y&space;=&space;b_{0}&space;&plus;&space;b_{1}*x_{1}" title="y = b_{0} + b_{1}*x_{1}" /></a>

y= Dependent Variable 
<a href="https://www.codecogs.com/eqnedit.php?latex=b_{0}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?b_{0}" title="b_{0}" /></a> = Constant
<a href="https://www.codecogs.com/eqnedit.php?latex=b_{1}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?b_{1}" title="b_{1}" /></a> = Coefficient
<a href="https://www.codecogs.com/eqnedit.php?latex=b_{1}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?b_{1}" title="x_{1}" /></a> = Independent Variable 

### Project 1:
### [Salary - Experience Plot](https://github.com/apul1421/Machine-Learning-/blob/master/linear_regressionpractice.py)
#### Data Preprocessing(Common for all the  models) 
1. First import the dataset [download data](https://github.com/apul1421/Machine-Learning-/blob/master/Salary_Data.csv)
2. Split the data into training as well as test set
3. Do feature scaling(if required)

#### Training the model 
4. Fitting Simple Linear Regression to the Training Set 
  Salary = <a href="https://www.codecogs.com/eqnedit.php?latex=b_{0}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?b_{0}" title="b_{0}" /></a> = Constant + <a href="https://www.codecogs.com/eqnedit.php?latex=b_{1}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?b_{1}" title="b_{1}" /></a>*Experience
5. Predicting the test set result 
6. Visualising the result

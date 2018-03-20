# Machine-Learning
These are some basic machine learning projects with some conceptual explanation we wil first start with something very basic i.e Linear Regression
## Simple Linear Regression
Linear Regression model is one of simplest model. It uses the slope equation for training the model and find correlation between the Dependent Variables and  the Independent Variables 

<b>Equation:</b>
<a href="https://www.codecogs.com/eqnedit.php?latex=y&space;=&space;b_{0}&space;&plus;&space;b_{1}*x_{1}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?y&space;=&space;b_{0}&space;&plus;&space;b_{1}*x_{1}" title="y = b_{0} + b_{1}*x_{1}" /></a>

y= Dependent Variable <br>
<a href="https://www.codecogs.com/eqnedit.php?latex=b_{0}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?b_{0}" title="b_{0}" /></a> = Constant <br>
<a href="https://www.codecogs.com/eqnedit.php?latex=b_{1}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?b_{1}" title="b_{1}" /></a> = Coefficient <br>
<a href="https://www.codecogs.com/eqnedit.php?latex=b_{1}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?b_{1}" title="x_{1}" /></a> = Independent Variable <br>

### Project 1:
### [Salary - Experience Plot](https://github.com/apul1421/Machine-Learning-/blob/master/linear_regressionpractice.py)
#### Data Preprocessing(Common for all the  models) 
1. First import the dataset [(download data)](https://github.com/apul1421/Machine-Learning-/blob/master/Salary_Data.csv)
2. Split the data into training as well as test set
3. Do feature scaling(if required)

#### Training the model 
4. Fitting Simple Linear Regression to the Training Set 
   ##### Equation of the problem set:<br>
   <a href="https://www.codecogs.com/eqnedit.php?latex=Salary&space;=&space;b_{0}&space;&plus;&space;b_{1}*Experience" target="_blank"><img src="https://latex.codecogs.com/gif.latex?Salary&space;=&space;b_{0}&space;&plus;&space;b_{1}*Experience" title="Salary = b_{0} + b_{1}*Experience" /></a>
5. Predicting the test set result 
6. Visualising the result

## Multiple Linear Regression
Unlike Linear Regression model in which one independent variable used to have correlation with a dependent variable Multiple Regression model contains many Independent variable which depends on Dependent variable.<br>

<b>Equation:</b><br>
<a href="https://www.codecogs.com/eqnedit.php?latex=y&space;=&space;b_{0}&space;&plus;&space;b_{1}*x_{1}&plus;b_{2}*x_{2}&plus;....&plus;b_{n}*x_{n}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?y&space;=&space;b_{0}&space;&plus;&space;b_{1}*x_{1}&plus;b_{2}*x_{2}&plus;....&plus;b_{n}*x_{n}" title="y = b_{0} + b_{1}*x_{1}+b_{2}*x_{2}+....+b_{n}*x_{n}" /></a>
<br>
<a href="https://www.codecogs.com/eqnedit.php?latex=y" target="_blank"><img src="https://latex.codecogs.com/gif.latex?y" title="y" /></a> = Dependent Variable <br>
<a href="https://www.codecogs.com/eqnedit.php?latex=b_{0}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?b_{0}" title="b_{0}" /></a> = Constant <br>
<a href="https://www.codecogs.com/eqnedit.php?latex=b_{1}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?b_{1}" title="b_{1}" /></a> = Coefficient <br>
<a href="https://www.codecogs.com/eqnedit.php?latex=b_{1}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?b_{1}" title="x_{1}" /></a> = Independent Variable <br>

### Project 2:
### [Startup Funding Example](https://github.com/apul1421/Machine-Learning-/blob/master/multiple_linear_regression_practice.py)
->As an investor its important to consider all the dynamics of a Company before investing in it ,so here in this example we will develop a model which will predict the dependency of several independent variables on profit of a startup <br>[Sample data download](https://github.com/apul1421/Machine-Learning-/blob/master/50_Startups.csv)

<b>Dependent Variable</b><br>
1. Profit <br>

<b>Independent Variable </b><br>
1. R&D Spend<br>
2. Admin Spend<br>
3. Marketing Spend<br>
4. State<br>

Since State here is a categorical variable so we need to make Dummy Variable out of it i.e. <br>

<b>Categorical Variable</b>
<table style="width:100%">
  <tr>
    <th>State</th>
  </tr>
  <tr>
    <td>New York</td>
  </tr>
  <tr>
    <td>California</td>
  </tr>
</table>

<b>Dummy Variable</b>
<table style="width:100%">
  <tr>
    <th>New York</th>
    <th>California</th>
  </tr>
  <tr>
    <td>1</td>
    <td>0</td>
  </tr>
  <tr>
    <td>0</td>
    <td>1</td>
  </tr>
</table>
<br>
<b>What will happen is we consider both the Dummy Variables in the model?</b><br>
If we consider both the dummy variable(i.e New York and California) in the model then model will suffer from a phenomenon called as Dummy Variable Trap.
In Dummy Variable trap there is a phenomenon Multicollinearity i.e when one or more Independent variables in a linear regression predict another. As a result of this model cannot distinguish the effect of D1 from D2.So to avoid this problem always omit one variable from the model ,so if there are 2 variables omit 1<br>
<a href="https://www.codecogs.com/eqnedit.php?latex=D_{2}&space;=&space;1-D_{1}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?D_{2}&space;=&space;1-D_{1}" title="D_{2} = 1-D_{1}" /></a><br>
Where D1 and D2 are two Dummy Variables<br>

<b>In a model we need to throw/omit columns. But why?</b><br>
1. If a model contains lots of stuff then its a garbage model.<br>
2. If there are more variables then it is difficult to explain all the variables dependeny.<br>

### Five methods to build a model<br>
-> All In<br>
-> Backward Elimination(In this example we will focus on this method)<br>
-> Forward Elimination<br>
-> Bidirectional Elimination<br>
-> Score Comparison<br> 

<b>Backward Elimination</b><br>
Step-1:Select a significance level to stay in the model(eg: SL = 0.05)<br>
Step-2:Fit full model with all predictors<br>
Step-3:Consider the predictor with highest P-value. If P>SL go to Step-4 or go to FIN<br>
Step-4:Remove the predictor<br>
Step-5:Fit model without this variable (Move to step-3)<br>

## Polynomial Linear Regression
In a polynomial Linear Regression we have one variable having different power<br>
<b>Equation:</b><br>
<a href="http://www.codecogs.com/eqnedit.php?latex=\small&space;y&space;=&space;b_{0}&plus;b_{1}x_{1}&plus;b_{2}x_{1}^{2}&plus;......&plus;b_{n}x_{1}^{n}" target="_blank"><img src="http://latex.codecogs.com/gif.latex?\small&space;y&space;=&space;b_{0}&plus;b_{1}x_{1}&plus;b_{2}x_{1}^{2}&plus;......&plus;b_{n}x_{1}^{n}" title="\small y = b_{0}+b_{1}x_{1}+b_{2}x_{1}^{2}+......+b_{n}x_{1}^{n}" /></a><br>

#### When to use Polynomial Regression?<br>
As told earlier if the data is fitting the best fit line like the below example we choose Linear Regression 
<img src="http://108.61.119.12/wp-content/uploads/2014/05/simple-linear-regression.png" width="400" height="220"><br>
But if the data shows curve effect something like below then we choose Polynomial Regression<br>
<img src="http://www.statisticshowto.com/wp-content/uploads/2015/01/excel-polynomial-regression-300x180.png"><br>

#### Why is Polynomial Linear Equation called Linear ?
Here linear refers to the coefficient because our end goal is to find out b coefficients so that later we can plug x and get y.<br>

### Project 3:
### [Salary Bluff Check](https://github.com/apul1421/Machine-Learning-/blob/master/polynomial_regression_practice.py)<br>
[Download Data](https://github.com/apul1421/Machine-Learning-/blob/master/Position_Salaries.csv)<br>
In this example the problem statement is  that a person is joining a new company where he asks for salary of more then $160K as in his previous company he is used to get 160K for 20+ years experience .However HR wants to find whether he telling truth regarding his previous companies salary so HR gets the data of the previous companies salary chart.<br> 

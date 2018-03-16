# Machine-Learning
These are some basic machine learning projects with some conceptual explanation we wil first start with something very basic i.e Linear Regression
## Linear Regression
Linear Regression model is one of simplest model. It uses the slope equation for training the model and find correlation between the Dependent Variables and  the Independent Variables 

Equation:
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
Equation:<br>
<a href="https://www.codecogs.com/eqnedit.php?latex=y&space;=&space;b_{0}&space;&plus;&space;b_{1}*x_{1}&plus;b_{2}*x_{2}&plus;....&plus;b_{n}*x_{n}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?y&space;=&space;b_{0}&space;&plus;&space;b_{1}*x_{1}&plus;b_{2}*x_{2}&plus;....&plus;b_{n}*x_{n}" title="y = b_{0} + b_{1}*x_{1}+b_{2}*x_{2}+....+b_{n}*x_{n}" /></a>
<br>
<a href="https://www.codecogs.com/eqnedit.php?latex=y" target="_blank"><img src="https://latex.codecogs.com/gif.latex?y" title="y" /></a> = Dependent Variable <br>
<a href="https://www.codecogs.com/eqnedit.php?latex=b_{0}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?b_{0}" title="b_{0}" /></a> = Constant <br>
<a href="https://www.codecogs.com/eqnedit.php?latex=b_{1}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?b_{1}" title="b_{1}" /></a> = Coefficient <br>
<a href="https://www.codecogs.com/eqnedit.php?latex=b_{1}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?b_{1}" title="x_{1}" /></a> = Independent Variable <br>

### Project 2:
### [Startup Funding Example](https://github.com/apul1421/Machine-Learning-/blob/master/linear_regressionpractice.py)
->As an investor its important to consider all the dynamics of a Company before investing in it ,so here in this example we will develop a model which will predict the dependency of several independent variables on profit of a startup <br>

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


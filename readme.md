## Find publicly available data for key *supply-demand* factors that influence US home prices *nationally*

<hr>

## Supply Factors : 

### Target : CSUSHPISA 
This variable serves as a proxy for home prices and represents the home price index for the United States.

### Features :
Construction Spending , Building Permit , Privately-Owned-completed-home , Vacant Housing , 


<hr>
<pre>
TLRESCONS         0.891138
PERMIT            0.372613
COMPUTSA          0.280040
EVACANTUSQ176N   -0.604815
MSACSR            0.150796
CSUSHPISA         1.000000
Name: CSUSHPISA, dtype: float64
</pre>
<hr>

### Findings : 

**Construction Spending:**<br>
The correlation between Construction Spending(TLRESCONS) and House Prices (CSUSHPISA) is a perfect positive correlation .This means that as Construction Spending increases house price also increases .

**PERMIT:**<br>
There is a positive correlation between BUILDING PERMIT and House Prices CSUSHPISA, but the relationship is not very strong. 


**Privately-Owned: (COMPUTSA)**<br>
There is a positive correlation between private house completed and house prices, but the relationship is weaker. They do not sell their personalized build house often.

**Vacant Housing :(EVACANTUSQ176N)**<br>
incerasing vacent house decrease the cost of the house . 



## Demand Factors : 

### Target : CSUSHPISA 
This variable serves as a proxy for home prices and represents the home price index for the United States.

### Features :
Interest Rate RealEstate , GDP , Employement , Mortgage Rate , Population , Rent Prices ,Housing Affordability Index

<hr>
<pre>
POPTHM                    0.686593
GDP                       0.866411
InterestRateRealEstate    0.942871
MORTGAGE15US             -0.149296
UMCSENT                  -0.139488
CSUSHPISA                 1.000000
Name: CSUSHPISA, dtype: float64
</pre>
<hr>

### Findings : 

**Interest Rate RealEstate:**<br>
The correlation between InterestRateRealEstate and House Prices (CSUSHPISA) is a perfect positive correlation .This means that as InterestRateRealEstate increases house price also increases .

**GDP:**<br>
When GDP in a region increases, House price of that area tends to increase as well
eg New-York housing price increase


**Mortgage Rate (MORTGAGE15US )**<br>
 mortgage rate increases (higher interest rates), it's associated with a slight decrease in housing prices

**Population**<br>
As population increase of region the price of houses increase.


## Model Training :

two custom dataset file
1. Supply dataset 
2. Demand dataset

seperatly trained model on both of the factor 

<hr>

#### 1.Supply model: 
<pre>
Model Selection Results:
Linear Regression: MSE=32.98992401847717
Decision Tree: MSE=412.20206228468004
Random Forest: MSE=151.18601839380693

Best Model: Linear Regression
Best Model MSE on Testing Set: 31.8603355323733

R-squared score: 0.9679179321149581
</pre>
<hr>

#### 2.Demand model:

<pre>
Model Selection Results:
Linear Regression: MSE=55.27894160763727
Decision Tree: MSE=64.59382664943017
Random Forest: MSE=40.96991422280513

Best Model: Random Forest
Best Model MSE on Testing Set: 30.204057197372467

R-squared score: 0.9747825731064546
</pre>

<hr>

### Result: 
**Both the model have similar result approx 97% accurate thus stating both supply and demand is very important in detemrming the price of houses.**

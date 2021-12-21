# Antenna-design-using-ML

In the given project, First I am import some important python libraries those are gonna used in project for different proposes i.e pandas is used to read and write dataset and perform some operations like concatenation, merge and other useful operations to dataset. Numpy is to perform mathematical and numerical computation and sklean packages for train test spilit of dataset, for finding RMSE and MAE and accuracy etc also importanting machine learning algorithms such as linear regression and it’s type, DecisionTreeRegressor and RandomFOrestRegressor.
In First step I read data set and store into data variable and after that I check uniques values does a column have using nunique() method.
In second step I prep data for train and test and for that purpose before test test splilit I dop TestFreq and strength and want to check model accuracy on rest of attributes to predict signal strength.
For that scenario I applied models LinearRegression, ElasticNet, Lasso, DecisionTreeRegressor, RandomForestRegressor and found that we can create such model that only use the parameters that are not the test frequency but found that the model accuracy on above machine learning algorithms is very low. Maximum accuracy achieved by RandomFOrestRegressor which give is round about 31%.

RMSE of LinearRegression model is: 2.676241886875816 
R2 value of LinearRegression is: 0.28721183022604246 
RMSE of ElasticNet model is: 2.7188484952980243 
R2 value of ElasticNet is: 0.26433554803939263 
RMSE of Lasso model is: 2.762681278365111 
R2 value of Lasso is: 0.24042384111534953 
RMSE of DecisionTreeRegressor model is: 2.6278146757974685 
R2 value of DecisionTreeRegressor is: 0.31277456777177237 
RMSE of RandomForestRegressor model is: 2.624496871014825 R2 value of RandomForestRegressor is: 0.314508815216624 


The conclusion which I can conclude from above experiment is that Yes it's possible to create that kind of model but we will get too much bad results because the variable test frequency plays a vital role to estimate signal strength. 

For better understanding I repeate same experiment and this time includes test frequenecy parameter aswell and for five regression model results and their R^2 values which give us a very clear picture how much important this attribute is for statical models.


RMSE of LinearRegression model is: 2.7611782684314625 R2 value of LinearRegression is: 0.25005662488174607 
RMSE of ElasticNet model is: 2.7941026554043513 
R2 value of ElasticNet is: 0.2320652935067815 ************************************************** 
RMSE of Lasso model is: 2.811382906304811 
R2 value of Lasso is: 0.2225372690799633 ************************************************** 
RMSE of DecisionTreeRegressor model is: 0.9954226952977892 
R2 value of DecisionTreeRegressor is: 0.9025336603929535 ************************************************** 
RMSE of RandomForestRegressor model is: 0.9306109888387203 
R2 value of RandomForestRegressor is: 0.91481248834547

DecisionTreeRegressor and RandomForestRegressor are the best models among the these five models. However RandomForestRegressor model resulted much better their error is pretty low. Moreover 90%+ R^2 is also a good value.

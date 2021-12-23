**BENAMER AMIRA RAYANE**

**Initial Training**

**What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?**

It does not work, since there are negative predicted values. To success the submission, it is required to put all negative values equal to 0.

**What was the top ranked model that performed?**

The first raw submission 

**Exploratory data analysis and feature creation**

**What did the exploratory analysis find and how did you add additional features?**

Categorical features are considered as numerical ones. Time also is considered as one component. Extract sub features from datetime  into day, month, year, hour.

**How much better did your model preform after adding additional features and why do you think that is?**

0.47357 

**Hyper parameter tuning**

**How much better did your model preform after trying different hyper parameters?**

0.50735 

**If you were given more time with this dataset, where do you think you would spend more time?**

EDA by analysing the correlation between features to be able to propose suitable models.

Hyper parameters phase by trying different values. 

**Create a table with the models you ran, the hyperparameters modified, and the kaggle score.**

|**Model**|**Hpo1**|**Hpo2**|**Hpo3**|**Score** |
| :- | :- | :- | :- | :- |
|**initial**|**Default-values**|**Default-values**|**Default-values**|<p></p><p></p><p>1.39495  </p>|
|**Add\_features**|**Default-values**|**Default-values**|**Default-values**|<p></p><p></p><p>0.47357</p>|
|**hpo**|<p>'num\_epochs': 10</p><p>'activation': ag.space.Categorical('relu', 'softrelu', 'tanh')</p><p>learning\_rate': ag.space.Real(1e-4, 1e-2, default=5e-4, log=**True**)</p><p>'layers': ag.space.Categorical([100], [1000], [200, 100], [300, 200, 100])</p><p>'dropout\_prob': ag.space.Real(0.0, 0.5, default=0.1)</p><p>'GBM': gbm\_options,</p><p>`                   `'NN': nn\_option</p>|<p>num\_trials = 5  </p><p>search\_strategy = 'auto' </p><p></p>|**Default-values**|<p>0.50735 </p><p></p>|

### **Create a line plot showing the top model score for the three (or more) training runs during the project.**
### ![](model_train_score.png)


### **Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.**
###![](model_test_score.png)

## **Summary**
It was good to try autogluon since it allows to assess the performance of different models. However, testing other models as multi-variate linear regression, Decision tree and other might also be a good choice. I


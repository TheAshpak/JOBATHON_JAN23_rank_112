# Job A Thon jan 2023

Detailed approach for Job-A-Thon conducted by Analytics Vidhya on Jan 2023

## Library Used



```

1) XGBoost
2) CatBoost Encoder (category-encoders)
3) Pandas 
4) Sklearn
5) NumPy

```
## Approach

### Data Preprocessing and Feature Engineering:
```
1) Generate more features using feature concatenation on all Categorical data
2) Visualized outliers presence in nnumerical column , it was seen that data was heavily skewed on right side (+Vely Skewed)
3) Winsorized outliers present in Target variable(CLTV) and Claim_amount on both tail to make data more Guassian
4) With the help of 'category-encoders' endoded all categorical features with respect to target variable(CLTV) as 'One hot encoding' and label encoding wasn't performing well and unable to make any relation withing data 

```
### Model Selection
```
1) Trained Multiple regression models ex : Linear regression , KNN regressor , Extra tree regressor , Decision Tree regressor , SVR (SVM) , XGBoost , Adaboost
few Ensemble Models - Voting regressor , Stacking Regressor , etc
2) After trying Multiple models it was found that 'divide and conquer' based models were performing better than other algorithems
3) Decision tree was performing better as compared to other single models , so tried algorithems based on Decision tree
4) XGboost was giving better R2_score and was not overfitting after some hyperparameter tuning so chose XGboost as the final model

```
### Final Observation
* Coefficient of determination (R2_score) is prone to number of variables , as number of variables increases R2_score tends to increase , so in this problem Adjusted R2_score would have been better evaluation metric as it penalize model for each redundant feature.


Thanks For Reading and Visiting :)

## Housing Insights for the King County, WA Area

Buying a house can be a tricky process, extremely for first time buyers. If only there was something that could be done to make it easier! Well luckily for the people wanting to purchase a home in King County, there is! With a multiple linear regression model, data can be filtered to predict a price within certain grading and condition ranges that new householders can use. Below we'll go through the process of how the model was formed as well as include what criteria was used.

**Methodology**

The files used:
1. King County House Sales dataset (kc_house_data.csv)
2. Column Names (column_names.md)
3. King County Grading and Condition Scales (https://info.kingcounty.gov/assessor/esales/Glossary.aspx?type=r)

**Cleaning Up the Columns**

From the dataset there was a healthy amount of options to choose from, but basing it on beginning buyers there were some columns that were dropped and/or refined. The columns that ended up being used were price, bedrooms, bathrooms, square footage of living space, square footage of lot, floors, waterfront,	condition, grade, and lastly square footage of basements. Further filtration was done on the price range for buyers to be one million dollars and under so that not all of the buyer's saving are theoretically drained just purchasing the house. In addition, we want to reassure these people that the homes they could search for in this model would be of quality. Therefore, using the condition and grading system provided by the King County area, the model is sorted to be at least a grade of 6 (where there are a few lower quality materials and more simplistic designs) to a highest of 10 (higher quality of features and usually more square footage) on the King County grading scale and the condition to be at least a 3 (or in words, an average home that needs only minor repairs).

**Corralling Correlations and Transforming Data**

Keeping the transformation train going on our data, the next step was to log transform price followed by getting dummy variables for our categorical columns (specifically grade and condition). These changes helped our model by creating more of an apples to apples situation between the variables as well as making sure that the subgroups of the sample are represented. Lastly, interactions were checked among our x variables to ensure that if there was an interaction in our model, that it had a positive influence on it. It should be noted however, that just because a variable may be correlated does not necessarily mean that they interact. Shown in the graph below is the positive interaction between the x variables living and lot.

!![InteractionBetweenLiving Lot](https://user-images.githubusercontent.com/79724188/128173825-bd5d0865-a28a-4063-a0a2-4aa77b764e35.png)

**Final Model**

At the end of the modifications to the model, to ensure that it was predicting our results accurately and confidently, a QQ plot and a normality plot were made. These demonstrate the residuals are looking nice and normally distributed. This is a good sign that this means there aren't any high or low outliers as well as variances that are relatively equal. 

![QQPlot](https://user-images.githubusercontent.com/79724188/128173962-9dbafd2f-a747-4051-b6ad-c92d3ed1fce1.png)
![NormalityPlot](https://user-images.githubusercontent.com/79724188/128173978-53e8f69d-e39a-46b1-bfc5-f39b4dd6a576.png)

Furthermore, below is the final model and it's test/train split results.

![FinalModelOLS](https://user-images.githubusercontent.com/79724188/128440170-af2044ad-81d0-4647-ad16-8388b4747917.png)
![FinalModelSklearn](https://user-images.githubusercontent.com/79724188/128440182-ccd88d3e-ebb8-4694-a2b3-ff328102e3c1.png)

**Conclusion**

With the final model it is evident that 44.7% of the variations in the dependent variable y (price) are explained by the independent variables in our model. Also, the root mean squared error (RMSE) for our model showed that the predicted difference between values and it's actual values were quite close with Train RMSE equaling roughly 143595.06 and the Test RMSE coming out to be around 143352.60. This indicates that our model is adequate in predicting home prices for new time buyers in the King County area of Washington.

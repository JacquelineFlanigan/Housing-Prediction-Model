## Housing Insights for the King County, WA Area

Buying a house can be a tricky process, extremely for first time buyers. If only there was something that could be done to make it easier! Well luckily for the people wanting to purchase a home in King County, there is! With a mupltiple linear regression model, data can be filtered to predict a price within certain grading and condition ranges that new householders can use. Below we'll go through the process of how the model was formed as well as include what criteria was used.

**Methodology**

The files used:
1. King County House Sales dataset (kc_house_data.csv)
2. Column Names (column_names.md)
3. King County Grading and Condition Scales (https://info.kingcounty.gov/assessor/esales/Glossary.aspx?type=r)

**Cleaning Up the Columns**

From the dataset there was a healthy amount of options to choose from, but basing it on beginning buyers there were some columns that were dropped and/or refined. The columns that ended up being used were price, bedrooms, bathrooms, square footage of living space, square footage of lot, floors, waterfront,	condition, grade, and lastly square footage of basements. Further filtration was done on the price range for buyers to be one million dollars and under so that not all of the buyer's saving are theoretically drained just purchasing the house. In addition, we want to reassure these people that the homes they could search for in this model would be of quality. Therefore, using the condition and grading system provided by the King County area, the model is sorted to be at least a grade of 6 (where there are a few lower quality materials and more simplistic designs) to a highest of 10 (higher quality of features and usually more square footage) on the King County grading scale and the condition to be at least a 3 (or in words, an average home that needs only minor repairs).

**Corraling Correlations and Transforming Data**



**Final Model**


**Conclusion**

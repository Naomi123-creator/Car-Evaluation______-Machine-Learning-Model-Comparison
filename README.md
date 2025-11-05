# Car-Evaluation______-Machine-Learning-Model-Comparison


This project aims to evaluate car acceptability (e.g., unacceptable, acceptable, good, very good) based on various features such as buying price, maintenance cost, number of doors, capacity (persons), luggage boot size, and safety rating.

Using the Car Evaluation Dataset, I implemented and compared several machine learning models to predict the car’s overall acceptability.

Dataset Summary
	•	Rows: 1,727
	•	Columns: 7
	•	Target Variable: class (unacc, acc, good, vgood)
	•	Features:
	•	buying, maint, doors, persons, lug_boot, safety
	•	No missing or duplicate values.

 Data Preprocessing
	1.	Loaded dataset using Pandas.
	2.	Renamed columns for clarity.
	3.	Converted categorical numeric-like values:
	•	"5more" → 5 in doors
	•	"more" → 5 in persons
	4.	Label-encoded categorical variables.
	5.	Split data into training and testing sets (80% / 20%).


 Observations
	•	XGBoost produced the highest accuracy (98.55%), outperforming all other models.
	•	Random Forest also performed strongly (96.82%), confirming that tree-based ensemble models handle this categorical data effectively.
	•	Linear and probabilistic models (Logistic Regression, Naïve Bayes) performed below 70%, showing they may not capture non-linear relationships in this dataset.
	•	The data has strongly categorical and hierarchical relationships, which favor tree-based algorithms.


 What I Learned
	•	Proper data encoding is crucial when working with categorical data.
	•	Ensemble methods like Random Forest and XGBoost are powerful for structured datasets with categorical attributes.
	•	Accuracy alone doesn’t tell the whole story — evaluating confusion matrices and feature importance can provide deeper insight (planned for next iteration).
	•	XGBoost’s superior accuracy and efficiency make it the most suitable model for deployment.

 Conclusion

✅ Final Model Chosen: XGBoost Classifier (Accuracy: 98.55%)
It provides the best balance of accuracy and generalization for predicting car evaluation categories.

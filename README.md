
📊 Sales Forecasting for a German Drugstore Chain (2013–2015)

This project was part of my MSc program at the Alliance Manchester Business School, which focuses on daily sales prediction for 1,115 German drugstore stores, using historical data spanning from 2013 to 2015.
Multiple machine learning & deep learning models were implemented, analysed, and compared to build a robust forecasting solution.

🚀 Project Objectives

Forecast daily sales for 6 weeks across retail outlets.

Identify key factors that influence sales.

Build machine learning models and compare their results.

Generate business recommendations based on data insights.

📂 Dataset Overview

1,048,575 observations

Retail data across 1,115 stores

Includes variables on sales, customer count, holidays, promotions & more.

Time range: January 2013 – August 2015 

Data Analytics project report

🔧 Data Pre-Processing Performed

Step	Description:
Missing Value Handling: Filled using random forest imputation for selected fields.
Date Formatting	Converted Date column into structured DateTime.
Scaling & Encoding	StandardScaler + One-Hot Encoding for categorical columns.
Outlier Detection	Identified 27,506 outliers via boxplots.
Train-Test Split	70% training

(Ref: Data Pre-processing section - pg.4–6) 

Data Analytics project report

📈 Exploratory Data Analysis (EDA) Highlights

Sales maximum = 41,551, mean = 5,767.83

Promotions strongly drive sales upward.

Monday shows the highest sales; Sunday shows the lowest due to closures.

Store Type B + Assortment C performed best.

PCA & Correlation analysis show a strong relation between Sales ↔ Customers.

(Refer: Analysis visuals pg.7–10) 

Data Analytics project report

🧭 Clustering

To model stores better, K-Means clustering was implemented → Optimal clusters = 4

Cluster	Performance
Cluster 0	Low sales
Cluster 1	Moderate
Cluster 2	High
Cluster 3	Highest performing

(Ref: Clustering pg.11) 

Data Analytics project report

🤖 Models Implemented

Model 	                  | RMSE (Validation)     |	RMSPE     |	Notes
Multiple Linear Regression                                    |	High error,	Underperformed,	Could not capture variability
Random Forest             |	1437–1737	            |23–30%	    |Better, but still limited
XGBoost ⭐                |1118–1342	            |13.7–23%	  |Best performing model
Deep Neural Network       |	Higher Error	                    |Over-generalising	
RNN/LSTM                  | Good temporal handling|17–27% 	|Better than DNN but < XGBoost

📌 XGBoost selected as final model because it achieved the best accuracy across all clusters.
(Ref: Modelling pg.12–19) 

Data Analytics project report

🏁 Final Recommendations

✔ Deploy XGBoost as the primary forecasting model
✔ Use cluster-based model training to enhance prediction quality
✔ Integrate additional features (product mix, customer demographics)
✔ Use forecasts for staffing, inventory, promo strategy & pricing

(Ref: Conclusions pg.20) 

Data Analytics project report

📷 Project Structure (Suggested for GitHub)
📁 Sales-Forecasting-Drugstore
│── 📄 README.md
│── 📄 Data Analytics Project Report.pdf
│── 📁 notebooks/
│── 📁 data/
│── 📁 models/

🔥 Tech Stack
Category	Tools Used
Programming & Analysis	Python, Pandas, NumPy
Modeling	XGBoost, RandomForest, Sklearn, Neural Networks, LSTM
Visualization	Matplotlib, Seaborn
ML Techniques	Encoding, Scaling, PCA, K-Means Clustering

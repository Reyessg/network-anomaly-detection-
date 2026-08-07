# network-anomaly-detection-
A data science and machine learning project using supervised and unsupervised modeling methods to detect anomalies in the UNSW-NB15 dataset. 
## Objective
The objective of this project was to accurately detect attacks within a system of 175,341 network connections. 
## Dataset
The UNSW-NB15 dataset consisted of training and testing sets, alongside an excel sheet providing definitions of each feature. We began the pre-processing step by identifying any numerical or categorical features that stood out, outliers, or null values. Furthermore, the relationship between variables and their correlation to one another was analyzed to locate the most important ones in the study. Upon further analysis, a class imbalance was noted between attacks and normal traffic in the system with attacks measuring at 119,341 connections and normal traffic measuring at 56,000 connections.
## Methods
The models used to find anomalies were both supervised and unsupervised. The unsupervised models used were DBSCAN and Isolation Forest while the supervised models used were Random Forest(RF), XGBoost, and Support Vector Machine (SVM). SMOTE was then used on RF to balance the dataset and analyze any differences.
## Results
Results were heavily dependent on the multi-dimensionality of the dataset. For example, DBSCAN and SVM were not as much of an accurate depiction of the dataset as compared to the other models. Upon initial assumption, RF was preferred among all models because it had a consistent high recall. However, after evaluation with ROC/AUC, XGBoost proved the better model as it had a higher true positive rate on all possible thresholds, with a rate of 0.98. 
## Project Structure 
- `notebooks/01_data_exploration.ipynb` - data loading, cleaning, and visualization
- `notebooks/02_unsupervised.ipynb` - DBSCAN and Isolation Forest
- `notebooks/03_supervised.ipynb` - Random Forest, XGBoost, SVM, SMOTE, and model evaluation
## Libraries used 
pandas, numpy, seaborn, matplotlib, sklearn, xgboost, imblearn.over_sampling

## Citation 
Moustafa, Nour, and Jill Slay. "UNSW-NB15: a comprehensive data set for network intrusion detection systems (UNSW-NB15 network data set)." Military Communications and Information Systems Conference (MilCIS), 2015. IEEE, 2015.

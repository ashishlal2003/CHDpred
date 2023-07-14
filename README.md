# CHDPred
Find the video recording here in this Drive link: https://drive.google.com/file/d/1pd5_OYsc8uzyb3Iyy87daAW2o1FkO6Wx/view?usp=sharing
The webapp is hosted on: https://chdpred.onrender.com

## Guidance Note

The problem that we are trying to solve is to detect if a person is suffering from CHD(Coronary Heart Disease) in the next 10 years of time based on certain input parameters. The Jupyter Notebook can be found in this repository to refer to.

I personally picked this from the health domain available on the Kaggle datasets. Upon analysing the dataset briefly, I came to a conclusion that the target value that we could be looking for is the CHD column and its output is always going to be binary (either 1 or 0).

Based on this initial information, I realized that we are now going to be looking towards creating Classification models, in this case Decision Tree Classifier, Random Forest Classifier and XGBClassifier. Such classification models train the dataset into giving not a range value like regression, but a classification value like binary in our case.

I initialized the project by setting up a new Conda virtual environment and importing the required dependencies. After loading the dataset, I went ahead with certain data preprocessing steps, like removing irrelevant features, checking and handling null values using the ‘most-frequent’ strategy. Then, I performed EDA (Exploratory Data Analysis) which in this case wasn’t required too much to an extent, but a basic heatmap showed me how and which features have potential correlations with the target feature.

Then I trained the models the way I described earlier and compared their Accuracy, Precision, Recall and F1-scores. Through this I finalized on the Random Forest Classifier. Then I exported this model into a Pickle file (.pkl) to be integrated into the basic Flask web application.

# Wine Quality Prediction

This project focuses on predicting the quality of white wines based on various chemical properties using the Random Forest Classifier algorithm. The dataset 'winequality-white.csv' contains information about different features of white wines, such as fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, free sulfur dioxide, total sulfur dioxide, density, pH, sulphates, alcohol, and the quality rating given by experts.

### The dataset, features and target value
    
Two datasets were created, using red and white wine samples, we will only focus on the *white wine* dataset for our study.
The inputs include objective tests (e.g. PH values) and the output is based on sensory data (median of at least 3 evaluations made by wine experts). Each expert graded the wine quality between **0** (*very bad*) and **10** (*very excellent*). The features in the dataset are:

+ **_fixed acidity_**: Most acids involved with wine or fixed or nonvolatile (do not evaporate readily).
+ **_volatile acidity_**: The amount of acetic acid in wine, which at too high levels can lead to an unpleasant, vinegar taste.
+ **_citric acid_**: Found in small quantities, citric acid can add 'freshness' and flavor to wines.
+ **_residual sugar_**: The amount of sugar remaining after fermentation stops, it's rare to find wines with less than 1 gram/liter and wines with greater than 45 grams/liter are considered sweet.
+ **_chlorides_**: The amount of salt in the wine.
+ **_free sulfur dioxide_**: The free form of SO2 exists in equilibrium between molecular SO2 (as a dissolved gas) and bisulfite ion; it prevents microbial growth and the oxidation of the wine.
+ **_total sulfur dioxide_**: Amount of free and bound forms of S02; in low concentrations, SO2 is mostly undetectable in wine, but at free SO2 concentrations over 50 ppm, SO2 becomes evident in the nose and taste of wine.
+ **_density_**: The density of the wine is close to that of water, depending on the percent alcohol and sugar content.
+ **_pH_**: Describes how acidic or basic a wine is on a scale from 0 (very acidic) to 14 (very basic); most wines are between 3-4 on the pH scale.
+ **_sulphates_**: A wine additive which can contribute to sulfur dioxide gas (S02) levels, which acts as an antimicrobial and antioxidant.
+ **_alcohol_**: The alcohol percentage present in the wine.
+ **_quality_**: Output/target variable (based on sensory data, score between 0 and 10).


## Installation

### Prerequisites:

Before running the code, make sure you have the following libraries installed in your Python environment:

+ numpy
+ pandas
+ seaborn
+ sklearn
+ matplotlib

### Installation:

To install the required libraries, use the following command:


```bash
  pip install *requirements.txt*
```
### Dataset
The dataset winequality-white.csv contains information about various features of white wine and their corresponding quality ratings. Each row in the dataset represents a wine sample with specific features. The 'quality' column is the target variable we want to predict.
This dataset is available from the **_[UCI machine learning repository](https://archive.ics.uci.edu/ml/datasets/wine+quality)_**. 


## How to Use
1. Clone the repository:

```bash
  git clone https://github.com/IshitaChoudhuri/WineQualityPrediction.git

```
2. Run the Jupyter notebook:
 
```bash
  jupyter notebook WineDetection.ipynb
```


## Code Explanation

The Jupyter notebook WineDetection.ipynb contains the step-by-step implementation of the wine quality prediction model. Here's a brief explanation of each section:

+ **_Importing Libraries:_** All the required libraries are imported to perform data analysis and build the prediction model.
Reading Input Data: The dataset winequality-white.csv is loaded into a pandas DataFrame called wine.

+ **_Describing the Data:_** Statistical summary of the data is obtained using the describe() function.

+ **_Taking Info from Data:_** Information about the DataFrame is retrieved using the info() function.

+ **_Plotting the Data:_** Various bar plots are created to visualize the relationship between wine quality and different features.

+ **_Count the No. of Instances of Each Class:_** The count of 'good' and 'bad' quality samples is calculated.

+ **_Making Just 2 Categories:_** Good and Bad: Wine quality is categorized into 'good' and 'bad' based on specific cutoffs.

+ **_Alloting 0 to Bad and 1 to Good:_** The 'quality' category is encoded into numerical values.

+ **_Balancing the Two Classes:_** The dataset is balanced by selecting an equal number of samples from both 'good' and 'bad' quality categories.

+ **_Checking the Counts of Classes in the New DataFrame:_** The count of 'good' and 'bad' quality samples in the new balanced DataFrame is verified.

+ **_Checking the Correlation Between Columns:_** The correlation between each feature and the 'quality' column is calculated.

+ **_Splitting the Data into Train and Test Sets:_** The data is split into training and testing sets for model training and evaluation.

+ **_Training the Wine Quality Prediction Model:_** RandomForestClassifier is used for training the model. Hyperparameter tuning is performed using GridSearchCV.

+ **_Model Evaluation:_** The trained model is evaluated using metrics like confusion matrix, classification report, and accuracy score.

+ **_Feature Importance:_** The feature importances of the RandomForestClassifier are visualized using a bar plot.

+ **_Correlation Matrix:_** The correlation between features is displayed using a heatmap.

+ **_Distribution of Wine Quality:_** The distribution of 'good' and 'bad' quality samples is visualized.

+ **_Scatter Plots:_** Scatter plots are used to explore the relationships between features and wine quality.

+ **_KDE Plots:_** Kernel Density Estimation plots are used to understand the distribution of features for 'good' and 'bad' quality wines.

+ **_Violin Plots:_** Violin plots are used to visualize the distribution of selected features for 'good' and 'bad' quality wines.

  
## Lessons Learned

### While building this project, I learned several key concepts and skills:

1. **_Data Preprocessing:_** I learned how to handle and preprocess data to prepare it for model training. This involved handling missing values, encoding categorical variables, and scaling features.

2. **_Model Selection and Hyperparameter Tuning:_** I explored different classification models and used GridSearchCV for hyperparameter tuning to find the best parameters for the RandomForestClassifier.

3. **_Data Visualization:_** I gained experience in using various plotting libraries like Seaborn and Matplotlib to visualize data and understand relationships between features.

4. **_Dealing with Class Imbalance:_** Balancing the dataset to avoid class imbalance was a crucial step to improve model performance. I used sampling techniques to balance the two classes.


### Challenges Faced and Overcoming Them:

1. **_Data Cleaning:_** The dataset contained some missing values that needed to be handled carefully. I addressed this challenge by imputing missing values using appropriate techniques.

2. **_Hyperparameter Tuning:_** Finding the optimal hyperparameters for the RandomForestClassifier required extensive experimentation. GridSearchCV allowed me to systematically search through parameter combinations.

3. **_Class Imbalance:_** The dataset had an imbalanced distribution of 'good' and 'bad' quality samples. I overcame this challenge by sampling equal numbers of samples from both classes to create a balanced dataset.

4. **_Interpreting Feature Importance:_** Understanding the importance of different features in predicting wine quality was initially challenging. However, visualizing the feature importances using bar plots helped in gaining insights.



## Contributions

Contributions to the Wine Detection Project are welcome. If you find any bugs, issues, or want to add new features, please submit a pull request or create an issue on the project's repository.

If you have any further questions or need assistance, please contact ishitachoudhuri3@gmail.com


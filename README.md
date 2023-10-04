# CodSoft_Task3
Task 3 performed at CodSoft Internship period<br>

## AIM:
Build a machine learning model to identify fraudulent credit card transactions. 

### Libraries:
- numpy
- pandas 
- matplotlib.pyplot
- seaborn 
- plotly
- datetime
- math
- matplotlib
- sklearn

### DataSet:
- The datasets contain transactions that have 492 frauds out of 284,807 transactions. So the dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions. When we try to build the prediction model with this kind of unbalanced dataset, then the model will be more inclined towards to detect new unseen transaction as genuine as our dataset contains about 99% genuine data.<br>
- The datasets contain transactions that have 492 frauds out of 284,807 transFraud and Genuine transaction Day wiseactions. So the dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions. When we try to build the prediction model with this kind of unbalanced dataset, then the model will be more inclined towards to detect new unseen transaction as genuine as our dataset contains about 99% genuine data.<br>
- As our dataset is highly imbalanced, so we shouldn't use accuracy score as a metric because it will be usually high and misleading, instead use we should focus on f1-score, precision/recall score or confusion matrix.

### Data Exploration and Preprocessing
- The shape and descriptive statistics for the dataset were displayed using df.shape and df.describe().
- A pair plot was created to visualize the relationship between Fraudulent and Non-Fraudulent Distribution seaborn.pairplot.
- Boxplot Showing Relationship between Amount Distribution for Fraud and Genuine transactions using sns.boxplot().

### Feature Engineering
- Feature engineering on Time.
  1. Converting time from second to hour
  2. Calculating hour of the day
  3. Calculating First and Second Day
  4. Fraud and Genuine transaction Day wise
- Comparison between Transaction Frequencies vs Time for Fraud and Genuine Transactions.<br>
   Graph generated shows that most of the Fraud transactions are happening at night time (0 to 7 hours) when most of the people are sleeping and Genuine transaction are happening during day time (9 to 21 hours).

### Scale Amount Feature
1. Scale amount by Log
2. Scale amount by Standardization
3. Scale amount by Normalization
4. Saving preprossed data as serialized files
   - Load preprocessed data
### Model Building
1. Splitting data into Training and Testing samples
2. Logistic Regression
   - Logistic Regression with imbalanced data
   - Predict from Test set
   - Model Evolution<br>
     Actually there are originally 144 fraud transactions and 85299 genuine transactions in the test dataset. However, our model predicted only 101 fraud transaction. Also, it should be kept in mind that these        101 predicted fraud transaction may not be identified correctly. It means that these predicted 101 fraud transactions are NOT only from 144 originally fraud transaction, but they may also be from genuine         transactions as well.
   - Model Evolution Matrix

### Undersampling for improving results
1. Logistic Regression with Random Undersampling technique
2. Undersampling only on train dataset
3. Model Evolution<br>
     Actually there are originally 144 fraud transactions and 85299 genuine transactions in the test dataset. However, our model predicted only 101 fraud transaction. After applying Undersampling to the Logistic Regression to train Dataset, count of Fraud transaction increased from 101 to 133. The model accuracy reached 97.406%, its is demonstared using confusion matrix.
4. Model Evolution Matrix

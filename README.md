# Sales-Client-Project

## BUISNESS CASE: 
BASED ON GIVEN FEATURE WE NEED TO PREDICT THE LEAD CATEGORY OF CUSTOMER[HIGH POATENTIAL, LOW POTENTIAL]

### INTRODUCTION OF PROJECT
* FicZon Inc is an IT solution provider with products ranging from on-premises products to SAAS based solutions. 
* FicZon major leads generation channel is digital and through their website. 
* FicZon business is majorly dependent on the sales force effectiveness. 
* As the market is maturing and more new competitors entering the market, FicZon is experiencing the dip in sales. 
* Effective sales is dependent on lead quality and as of now, this is based on manual categorization and highly depended on sales staff. 
* Though there is a quality process, which continuously updates the lead categorization, it’s value is in for post analysis, rather than conversation.
* FicZon wants to explore Machine Learning to pre-categorize the lead quality and as result, expecting significant increase in sales effectiveness

### PROJECT GOAL
1. Data exploration insights – Sales effectiveness.
2. ML model to predict the Lead Category (High Potential , Low Potential)

### PROJECT IS DEVICE INTO CERTAIN STEPS:
1. Featching data from data-base.
2. Domain analysis.
3. EDA: [Univariate, Bivariate & Multivariate analysis condition]
4. Data preprocessing/Feature Engineering.
5. Feature selection.
6. Model creation.
7. Model Evaluation.
8. Model Saving.

### DOMAIN ANALYSIS:

#### Sales effectiveness:
Sales effectiveness refers to the ability of a company's sales professionals to “win” at each stage of the customer's buying process, and ultimately earn the business on the right terms and in the right timeframe. Improving sales effectiveness is not just a sales function issue; it's a company issue, as it requires deep collaboration between sales and marketing to understand what is working and not working, and continuous improvement of the knowledge, messages, skills, and strategies that sales people apply as they work sales opportunities.

Sales effectiveness has historically been used to describe a category of technologies and consulting services aimed at helping companies improve their sales results.

#### Sales force effectiveness:
The purpose of sales force effectiveness is to increase company revenues through increased customer acquisition, product/service sales, and up-selling/cross-selling additional products and services. The purpose of sales force effectiveness metrics is "to measure the performance of a sales force and of individual salespeople.

When analyzing the performance of a salesperson, a number of metrics can be compared. These can reveal more about the salesperson than can be gauged by his or her total sales. When analyzing the performance of a sales team, an increase in revenue-per-rep can indicate improvement in salesforce effectiveness.

#### Target variable == Status
* In target veriable 11 labels are present (Junk Lead,Not Responding,CONVERTED,Just Enquiry,Potential,Long Term,In Progress Positive,In Progress Negative,LOST,Open,converted ) 
* This all labels is tell about the customer lead category [high potential, low potential] 

1.Created:
* This is unique feature in data tell about activity related to the selling and no of goods sold in certain date as well as time.

2.Product ID:
* Id of particular product.

3.Source:
* The source is contain imformation about the customer systematic search like call, live chats, and campaign.

4.Mobile:
* This is a unique feature contain a Mobile no of customer.


5.Email:
* This also unique feature contain a Email-id of customer.


6.Sales Agent:
* Sales agent is a front line customer service, A person or a company that acts as a sales agent on behalf of the exporting company ( principal ), introducing its products to potential buyers in the external market, in exchange for a commission based on the value of the business deals arranged and paid to the principal.

7.Location:
* The Location of sale field always has the main business address in it and has to be changed manually. This also means that the sales tax is computed based on the main business address and not the actual location of the sale.
* This feature contain lots of different location.

8.Delivery mode:
* Modes of Delivery of goods Delivery of goods may be made in any of the following three ways: 
1. Actual Delivery: Also known as physical delivery, actual delivery takes place when the goods are physically handed over by the seller or his/her authorized agent to the buyer or his/her agent authorized to take possession of the goods.

2. Symbolic Delivery: Where the goods are bulky and heavy and it is not possible to physically hand them over to the buyer, delivery thereof may be made by indicating or giving a symbol. Here the goods itself are not delivered, but the means of obtaining possession of goods is delivered.

3. Constructive Delivery: In this case neither physical nor symbolic delivery is made. In constructive delivery the individual possessing the products recognizes that he holds the merchandise for the benefit of, and at the disposal of the purchaser. Constructive delivery is also called attornment.


9. Status:
* This is a target variable tell about the lead category of customer.[high potential, low potential]


### DATA SUMMARY:
* The data is supervised and categorical as well as all feature is nominal including target variable.
* In this data three feature are unique so we can not perform any analysis on this feature.
* All feature is contain lots of different label so we compressed and merged the labels such that only the main ones were included
* In this data some feature contain blank spaces so we need to replace with NAN values.
* No scaling required as well as no need to handle outlier
* Use freqency encoding technique to handle categorical feature
* No need to handle duplicates because of Im mereged and compressed label.

### BASIC CHECKS:
*	In this data total 7422 observation with 9 feature.
*	3 unique feature.[date&time, email, mobile no]
*	No constant column in data

### EXPLOTARY DATA ANALYSIS:
* In EDA first is univariate analysis in that we get all unique labels and range of selling product as well as impoertant insights of labels,so lots of feature contain different labels this labels are belong to same category so I'm compressed and merged the labels.
* Im not perform any bivariate and multivariate analysis because of no continious feature avialable on this data.but i apply certain condition on data to get important insights.

### DATA PREPROCESSING:
*	In this data set blank spaces are available so I converted to NaN values.
*	Impute NaN value with mode because all feature is categorical.
*	Compressed and merged label because the labels are belong to same category.
*	Handle categorical data.

### FEATURE ENGINEERING:
*	Drop all unique column [ Created, Email, Mobile no]
*	Changing the data type 
*	Get correlation and plot heat map

### SAVE PRE-PROCESS DATA:
*	Save all pre-process data









### MODEL CREATION AND EVALUATION:
*	In this data I will be experimenting with seven algorithm
*	Logistic regression model is not perform well on training as well as testing side
*	KNN model is perform well on training side but not perform well on testing side so that’s why I use bagging but the score is sightly improve
*	Decision tree training accuracy is around 84% but the testing accuracy is 71% after using hyperparameter tunning score is not improve
*	Random forest training accuracy is around 84% but the testing accuracy is 72% after using hyperparameter tunning score is 73% 
*	Gradient boosting classifier model training accuracy is around 74% but the testing accuracy is 74% so gradient boosting classifier is perform well on testing as well as training side
*	XGBoost model is perform well on training side but in testing side not perform well
*	ANN model training and testing score is low

### CONCLUSION:
*	From above all model I will be select Gradient boosting model because it well perform on training as well as testing side so I can say that this model is low bias and low variance model 

### MODEL SAVING:
*	Save the model using pickle 





                                                                    



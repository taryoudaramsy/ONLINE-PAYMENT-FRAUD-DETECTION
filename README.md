 ONLINE PAYMENT FRAUD DETECTION FOR BLOSSOM BANK PLC
 
INTRODUCTION
Online banking fraud has become increasingly common in recent years. It occurs when fraudsters gain access to and transfer funds from an individual’s online bank account. Customers may also be duped by fraudsters into making fraudulent fund transfers themselves.
Online banking fraud can occur through:
ID theft: When fraudsters steal their victims’ identities to open an account in the victim’s name or take over the victim’s account
Phishing: This is when customers are directed by fraudsters to fake websites that look exactly the same with the real bank websites and tricked them into revealing personal information, including bank details.
Malware: These are malicious software, such as a virus or Trojan, which can be hidden in free downloads and attachments. They interrupt online banking sessions and present customers with a fake, but apparently genuine screen, prompting customers to input passwords that can be captured.
Vishing: This happens when fraudsters phone their potential victims and pose as Staff of a Bank, prompting customers to disclose their financial information, which they will later use for their own fraudulent purposes.

PROJECT DESCRIPTION
Blossom Bank, also known as BB PLC, is a multinational financial services group that offers retail and investment banking, pension management, asset management and payments services, headquartered in London, UK.
Blossom Bank wants to build a Machine Learning model to predict online payment fraud, which will boost customers' confidence in the Bank, increase profitability and also assist the Bank guide against online fraud risks.

DATA DICTIONARY (Description of the Columns)
• step: represents a unit of time where 1 step equals 1 hour
• type: type of online transaction
• amount: the amount of the transaction
• nameOrig: customer starting the transaction
• oldbalanceOrg: balance before the transaction
• newbalanceOrig: balance after the transaction
• nameDest: recipient of the transaction
• oldbalanceDest: initial balance of recipient before the transaction
• newbalanceDest: the new balance of the recipient after the transaction
• isFraud: fraud transaction

STEPS TAKEN
Data Inspection
-	Loaded the csv data using pd.read_csv(‘online payment fraud’)
-	Checked the rows, to know the variables in the head and tail rows
-	Checked the data info to know the total number of columns and the data type of each column (object, float or integer)

Data Cleansing
-	Checked for missing values
-	In this data set, there are no missing values and no unnecessary records to delete or replace

Exploratory Data Analysis
-	Visualized relationships between the label and some key features
-	Conducted univariate and multivariate analysis using histogram, bar charts and scatter plot diagram

Feature Engineering
-	This is the process of extracting useful features from the existing data
-	Columns with only integers (numeric columns) were selected and columns with object were excluded
-	Converted categorical data column ‘type’ into numerical, using One-Hot Encoding
-	Joined the encoded variables back to the main dataframe using pd.concat()
-	Removed the initial categorical columns after encoding using data1.drop()

Model Selection, Training and Validation
-	Our target is ‘isFraud’ column
-	Trained models are X_train, X_test, y_train and y_test
-	Machine Learning Algorithms were imported and Initialized
-	The Machine Learning models used are Random Forest Classifier, KNeighbors, Naive Bayes Classifier and Decision Tree Classifier

CHALLENGES ENCOUNTERED
During Feature Engineering, an error was encountered when converting categorical data into numerical using One-Hot Encoding. The resulting dataframe was eating up my RAM. So I dropped some columns (nameOrig and nameDest) that are not needed to encode, to reduce the data size.



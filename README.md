# FASTag Fraud Detection
<p align="center">
![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/ca4ca1b1-ec59-410f-982c-eb3640712524)
</p>

**Data** - [Fastag Fraud Detection Dataset](https://www.kaggle.com/datasets/thegoanpanda/fastag-fraud-detection-datesets-fictitious/data). 

## What is FASTag ?

FASTag is an electronic toll collection system in India, operated by the National Highway Authority of India (NHAI). FASTags stickers are typically placed on the inside of the vehicle's windshield, usually on the top, near the rearview mirror. It employs radio frequency identification (RFID) technology to enable automatic deduction of toll charges from a prepaid or linked account as a vehicle passes through a toll plaza.

![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/a41469e8-2a50-4b49-b686-e02236598a6d)

Regarding fraud associated with FASTag, there have been instances where fraudsters have attempted to exploit vulnerabilities in the system. Some common frauds include:

- **Cloning**: Fraudsters may attempt to clone legitimate FASTags or their unique identification numbers to use them for unauthorized toll payments.
- **Phishing**: Scammers may use phishing techniques, such as fake emails or messages posing as FASTag service providers, to trick users into revealing their FASTag account details, allowing the fraudsters to access and misuse those accounts.
- **Tampering**: Criminals may try to tamper with or alter FASTag stickers or devices to manipulate toll charges or steal sensitive information.
- **Identity Theft**: Identity theft can occur if someone obtains another person's personal information and uses it to apply for a FASTag or gain unauthorized access to an existing account.

To mitigate these risks, it's essential to:

- Purchase FASTags exclusively from authorized sources.
- Safeguard account details to prevent unauthorized access.
- Regularly monitor transactions for any discrepancies.
- Exercise caution and refrain from clicking on unsolicited links or messages.
- Promptly report any suspicious activity to the relevant provider or authorities.
    
**Data** - ![Fastag Fraud Detection Dataset](https://www.kaggle.com/datasets/thegoanpanda/fastag-fraud-detection-datesets-fictitious/data). 

## Project Objectives
1. Data Exploration
2. Exploratory Data Analysis
3. Feature Engineering
4. Model Development
5. Real-time Fraud Detection
6. Explanatory Analysis

## Before Feature Engineering
<img src="https://github.com/gentallman/gold_stock_trend/assets/78334851/c18190ab-b9aa-4bf5-b7a8-3bd0d974c31d" width="50%" height="50%">


## After Feature Engineering
<img src="https://github.com/gentallman/gold_stock_trend/assets/78334851/4ddfea97-406e-470e-a905-0720fd419c17" width="50%" height="50%">


## Model Development
<img src="https://github.com/gentallman/gold_stock_trend/assets/78334851/21497614-8256-470b-8154-953cd5a2c474" width="50%" height="50%">


<img src="https://github.com/gentallman/gold_stock_trend/assets/78334851/2364f3eb-b040-48d6-99e1-0d261ba3381d" width="50%" height="50%">


<img src="https://github.com/gentallman/gold_stock_trend/assets/78334851/54ab4446-02e4-40b7-a43a-9aa10d78db2a" width="50%" height="50%">

## Performance Metrices

<img src="https://github.com/gentallman/gold_stock_trend/assets/78334851/6dccfb55-6b65-421a-9dba-78d34c881484" width="50%" height="50%">       


## **Best Model**
**Gradient Boosting**     

<img src="https://github.com/gentallman/gold_stock_trend/assets/78334851/fe2ca4d4-56e5-4f50-b260-bb77cdc85629" width="27%" height="27%"> 

**Feature Importance Graph for gradient boosting classifier**

<img src="https://github.com/gentallman/gold_stock_trend/assets/78334851/303c818e-3ace-4c6b-a703-ff796135df85" width="50%" height="50%">

Transaction amount and amount paid are the primary factors that significantly contribute to predicting fraud in the Gradient Boosting classifier. Another highly effective classifier is the Random Forest model. Additionally, incorporating features such as vehicle speed, dimensions, and the hour of the fraudulent transaction can also influence prediction accuracy.

## Development of a Prototype for Real-Time Fraud Detection

The idea behind real-time fraud detection for FASTag is to continuously monitor transactions made through FASTag devices and promptly identify any fraudulent transactions as they happen.

- Data Collection: Gather real-time FASTag transaction data including transaction amount, vehicle details, and timestamp.
- Model Development: Create a machine learning model trained on historical FASTag data using algorithms like Random Forest, Logistic Regression, or Gradient Boosting.
- Real-time Prediction: Implement a system to continuously monitor FASTag transactions, using the model to predict fraud in real-time.
- Alerting Mechanism: Set up alerts to notify relevant parties when potential fraud is detected, via email, SMS, or monitoring dashboards.
- Evaluation and Monitoring: Continuously assess system performance, monitoring key metrics like detection rate and false positives.
- Integration: Integrate the fraud detection system seamlessly into existing FASTag infrastructure.
- Compliance and Regulations: Ensure system compliance with relevant regulations and security standards.

<img src="https://github.com/gentallman/gold_stock_trend/assets/78334851/cc66ecdf-e1c0-4ad1-bf8d-ae13db7217c6" width="80%" height="80%">

This implementation utilizes the Flask framework. The Gradient Boosting model is exported to a .pkl file, which is then loaded into the Flask application. By considering the values of 'amount_paid' and 'transaction_amount' along with a specified threshold, the system determines whether a transaction is legitimate or fraudulent. In the event of fraud, pertinent information such as timestamp, transaction details, and vehicle speed is recorded. Integration with CCTV cameras enables capturing the license plate of the vehicle.

Implementing real-time FASTag fraud detection enhances fraud prevention and minimizes financial losses.




## Explanatory Analysis

Based on the analysis provided, several insights into the factors contributing to fraudulent transactions can be derived:

1. Geographical Distribution: The data indicates that Karnataka (State Code: KA) has the highest count of fraud compared to other states included in the dataset. This suggests that fraudulent activities may be more prevalent in certain regions.

2. Toll Booth Analysis: The majority of fraudulent transactions occur at the B-102 tollbooth, followed closely by the C-103 tollbooth. Conversely, tollbooths such as A-101 have fewer reported fraudulent transactions. This indicates that certain tollbooths may be more susceptible to fraudulent activities.

3. Vehicle Types: Fraudulent activities are commonly associated with heavy vehicles such as SUVs, buses, trucks, and vans. Motorcycles, on the other hand, have not been linked to any recorded fraud cases across all toll booths. This suggests that the type of vehicle involved may influence the likelihood of fraudulent transactions.

4. Time of Day Analysis: The analysis reveals that fraudulent activities are most common between 10 AM and 4 PM, with over 40 fraudulent activities recorded during these hours. Conversely, fraudulent activities significantly decrease during the early morning hours between midnight and 5 AM. This indicates that the time of day may play a significant role in the occurrence of fraudulent transactions.

5. Feature Importance Analysis: The feature importance graph suggests that several factors, including amount_paid, transaction_amount, vehicle_speed, vehicle_dimension, hours, and month, are most influential in predicting fraud. This indicates that these features may serve as important indicators or predictors of fraudulent transactions.

## Challenges

- Consistently high performance across all models suggests potential overfitting to the training data, where the models capture noise rather than true data patterns. 
- Additionally, data imbalance, where one class like fraudulent transactions is significantly less represented than others, can distort model performance. 
- Complex models, especially with limited data, are more susceptible to overfitting, further complicating the issue.

## Contact

Author: Smit Rana


LinkedIn: [linkedin.com/in/smit98rana/](https://www.linkedin.com/in/smit98rana/)https://www.linkedin.com/in/smit98rana/


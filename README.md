# FASTag Fraud Detection
<p align="center">
  <img src="https://github.com/akhilchibber/Fastag-Fraud-Detection/blob/main/Fastag.jpeg?raw=true" alt="earthml Logo">
</p>

**Data** - ![Fastag Fraud Detection Dataset](https://www.kaggle.com/datasets/thegoanpanda/fastag-fraud-detection-datesets-fictitious/data). 

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
![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/97328acb-45d4-43a9-8702-80b58d09b0cf)

## After Feature Engineering
![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/ad23362a-8c35-410c-b312-d07915b4bff8)

## Model Development
![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/21497614-8256-470b-8154-953cd5a2c474)
![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/2364f3eb-b040-48d6-99e1-0d261ba3381d)
![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/54ab4446-02e4-40b7-a43a-9aa10d78db2a)

**Best Model**
Gradient Boosting
![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/6dccfb55-6b65-421a-9dba-78d34c881484)
![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/fe2ca4d4-56e5-4f50-b260-bb77cdc85629)
![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/303c818e-3ace-4c6b-a703-ff796135df85)
Transaction amount and amount paid are the primary factors that significantly contribute to predicting fraud in the Gradient Boosting classifier. Another highly effective classifier is the Random Forest model. Additionally, incorporating features such as vehicle speed, dimensions, and the hour of the fraudulent transaction can also influence prediction accuracy.![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/e30b6da1-af4b-49fd-8334-3fac04bbfe17)

## Development of a Prototype for Real-Time Fraud Detection
![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/cc66ecdf-e1c0-4ad1-bf8d-ae13db7217c6)
This implementation utilizes the Flask framework. The Gradient Boosting model is exported to a .pkl file, which is then loaded into the Flask application. By considering the values of 'amount_paid' and 'transaction_amount' along with a specified threshold, the system determines whether a transaction is legitimate or fraudulent. In the event of fraud, pertinent information such as timestamp, transaction details, and vehicle speed is recorded. Integration with CCTV cameras enables capturing the license plate of the vehicle.




## Contributing
We welcome contributions to enhance the functionality and efficiency of this script. Feel free to fork, modify, and make pull requests to this repository. To contribute:

1. Fork the Project.
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`).
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the Branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request against the `main` branch.

## License

This project is licensed under the MIT License - see the `LICENSE` file for details.

## Contact

Author: Akhil Chhibber

LinkedIn: https://www.linkedin.com/in/akhilchhibber/


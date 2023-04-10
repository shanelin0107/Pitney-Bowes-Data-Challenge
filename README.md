# Pitney-Bowes-Data-Challenge

# Introduction
Pitney Bowes, a global shipping and mailing company, provides technology, logistics, and financial servicesto small businesses, retailers, enterprises, 
government, and the majority of Fortune 500 companies for simplifying the process of mail and parcel delivery. Since the meters involved the business operation for their clients,
determining prospective equipment failure will prevent the cause of disruption for their clients.

The Baruch Data Challenge with Pitney Bowes required each group to design a mdoel to predict which meters will fail wiihin the next 7 days.

Pitney Bowes provides 2 files:
1. train.csv- Sample data for meters with a flag whether they fail within the next 7 days
2. test.csv- Sample data without fail flag.

# Timeline
<img width="583" alt="Screen Shot 2023-04-10 at 3 11 27 PM" src="https://user-images.githubusercontent.com/104215135/230977908-b77e1c2b-1d2f-42fd-a736-0811754fff51.png">

# Data
Original train fuile has 55 attributes including one categorical variable "deviceid" , one traget variable "fail_7" with binary values, one Boolean variable "charge_cycle_time_below_12", two datetime variables "LastRecord" and :Date_Deployed" and 49 float variables.

Considering that the time difference between the LastRecord and DateDeployed would be abn importnat factor, we created a new attribute, UsedDate.

As more than 40K observations are still to much, we prepare a 1000 small data subset from the train file to do Random Forest Regression. And get result as follow:
![Variable Importances](https://user-images.githubusercontent.com/104215135/230979467-d0982238-0146-4d52-92ff-0c36e7f0e157.png)



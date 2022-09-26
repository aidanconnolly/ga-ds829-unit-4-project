# Project 4 Proposal
## Problem Statement
At its core, the purpose of this project is to assist an international pharmaceutical company in using self-submitted customer data to determine trends in purchases. This could include:

- Identifying what customer characteristics suggest which treatment a customer will purchase
- Highlighting relationships between treatment types if a customer might purchase more than one
- Exploring geographical affinities toward certain treatments
- Determining which customer traits can be used in predicting lifetime value

The project will hopefully be taken further to incorporate email data down the road, but as that data is not yet available, it will likely not be included in this project.

## Hypothesis/Assumptions

Our hypothesis is that a customer who receives more relevant email marketing will be more likely to interact with the emails and purchase treatment. This could be through:

- Incorporating past treatment information into the email content and offers (i.e. “Because you purchased this…”)
- Using specific member characteristics to target content (i.e. “Clinics in Toronto are offering discounts this weekend…” or “It’s your birthday next week! Treat yourself to…”)
- Predicting customer affinities through purchase behavior and customer characteristics (i.e. “We think you’ll enjoy…” or “For our top customers, we’re offering…”)

Some assumptions include:

- The data received from the customers is accurate
- Customers are not sharing accounts
- Customers email addresses are accurate

## Goals and success metrics

The end goal for this project is to use the insights from this analysis to increase customer engagement. Ideally, this would be measured through an increase in customer registrations and the number of treatments purchased by each customer.

To accomplish this, the insights from this project will be used to inform and improve email marketing campaigns in the future. By learning what treatments a customer might have an affinity toward, emails can be more accurately targeted. Additionally, information about past treatments can be used to personalize email content. And finally, predictions about a customer’s lifetime value can inform decisions about providing incentives to purchase (like coupons).

## Risks or limitations

The treatments are provided by independent facilities, so the collection of data regarding treatments is limited to customer submissions. This has been incentivized by providing loyalty rewards in return, but there is nothing guaranteeing a specific customer’s treatment will be accounted for in the dataset. 

Because this data is customer-submitted, there’s always the potential for data errors to be present. Luckily, with the customer data being used for loyalty purposes, all submissions are individually reviewed before being approved, greatly reducing the likelihood of erroneous treatment submissions being accepted. However, there is still the chance of erroneous member characteristic data. Additionally, it is almost guaranteed that there will be a lack of data due to it not being submitted by customers.

This may also incorporate some bias into the analysis, as we have no way of analyzing the types of customers who receive treatment but don’t choose to submit their treatment data. It also means we may infer some faulty findings if we analyze the number of times a customer is treated. For example, if a customer only has one treatment listed, it may be because they’ve only submitted one treatment.

## Dataset

The dataset consists of the following schema (at the moment):

### Registrations

- Registration ID
- Member ID
- Registration datetime
- Postal code
- Country

### Member

- Member ID
- Created datetime
- Last updated datetime
- Date of birth
- Gender
- Language
- Points balance
- Points expiration datetime
- Account closure datetime
- UTM string during account creation
- Referrer URL during account creation
- Email consent
- SMS consent

### Point Redemptions

- Redemption ID
- Created datetime
- Last updated datetime
- Member ID
- Points redeemed
- Points value

### Treatment Tables

For each type of treatment, there are the following common fields:

- Treatment submission ID
- Created datetime
- Last updated datetime
- Member ID
- Treatment datetime
- Treatment facility postal code
- Treatment area
- Total purchase amount
- Spend on specific treatment
- Points earned
- Points expiration date
- Treatment validation status
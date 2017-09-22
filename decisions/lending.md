# Peer-to-Peer Lending

## Overview
Peer-to-Peer ("P2P") lending companies allow investors to purchase unsecured loans that are made to individuals. They provide data on individual borrowers and allow investors to select which loans they want to fund. If most of the individuals re-pay the loan, P2P provides an attractive return to investors. P2P Fund, LLC is a fund established to invest in P2P loans and they will use the DecisionCoin network to determine which loans to fund. 

## Bounty
300 ETH payable (roughly $10,000 at time of this writing) to the algorithm that predicts default risk most effectively (minimized log-loss).  

## Royalty
The algorithm writer will receive 30% of net investment returns that exceed the target return rate (LendingClub's standard return).  

## Data set
The data set consists of a historical record of consumer loans and the record of payments. These files contain complete loan data for loans issued 2007-2015, including the current loan status (Current, Late, Fully Paid, etc.) and latest payment information. The file containing loan data through the "present" contains complete loan data for all loans issued through the previous completed calendar quarter. Additional features include credit scores, number of finance inquiries, address including zip codes, and state, and collections among others. The file is a matrix of about 890 thousand observations and 75 variables. 

[Download data set](/lending/data-set.zip)

## Data providers
Owners of data that 

## Target
The competition  

## Deadline

Peer-to-Peer ("P2P") lending companies allow investors to purchase unsecured loans that are made to individuals. They provide data on individual borrowers and allow investors to select which loans they want to fund. If most of the individuals re-pay the loan, P2P provides an attractive return to investors. P2P Fund, LLC is a fund established to invest in P2P loans and they will use the DecisionCoin network to determine which loans to fund. 

1. P2P Fund, LLC provides a historical data set of funded P2P loans and offers a 1 DC bounty for the best performing model.  

2. DecisionCoin encrypts the training data, consisting of the historical data set of funded P2P loans, allowing data scientists to build models that predict the probability of default for each loan. 

3. Each model is distributed to available DecisionCoin miners that have compute resources and we evaluate the performance of each model.  

5. An API is created using the winning model and an encrypted version of the model distributed for execution. When the fund wants to evaluate new loans, it calls the API and pays DC.  

Key questions:
* When can models be used by someone else? Is it for sale by the original sponsor, or someone else? 
* Do we draw a distinction between models that can be used by only one person? Are all models shared? 
* Who prices the model usage? How does it work? Should be priced on value. 
* Value = abs(P[Default]old - P[Default]new) * loan amount
* Price should reflect the data contribution made by the fund
* Providing 100% of the data means they get free execution. (

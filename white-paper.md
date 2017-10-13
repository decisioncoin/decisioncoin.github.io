# Whitepaper (work in progress)
(not really a white paper but a working document for development. Feedback welcome)

## Abstract
DECIDE is a decentralized network for making better decisions through algorithms. The network enables businesses, data scientists and data owners to collaborate to build the most effective models for decisioning. It uses smart contracts to track and reward participants fairly. We propose a new token DecisionCoin (DC) to reward participants and incentivize the ecosystem.   

## Introduction

Algorithmic decisioning (or the more buzzy "machine learning") is huge and will continue to grow. A few examples that will make good Decisions: 
 
* Banks want to estimate the probability that a borrower will default on a loan
* Radiologists want to identify a tumor in a lung CT-scan
* Airport security want to determine whether a passenger deserves additional screening
* Subscription services want to predict which of their subscribers are at risk of churning
* Web publishers want to forecast web traffic to accurately assess demand
* Realtors want to predict home sale prices
* Marketers want to estimate the likelihood a user will click on an ad

Commercial solutions exist in each category but they suffer from the same problem: it's difficult to determine which solution provides the best solution. This is true for a couple of reasons:

1. Bad software sometimes has great salespeople, and vice-versa.
2. Testing a new solution against the status quo takes time, effort and expertise
3. Implementing a new solution in a production environment is difficult and time-consuming. 
 
DECIDE solves these problems through a blockchain that maintains a consensus record of the best model for a given problem and a standardized API that makes it easy to run the most effective model in production at all times.   

## Key Entities: Decisions, Models, & Requests

There are three key entities within the DECIDE network: Decisions, Models, & Requests.  

### Decisions
Decisions describe a problem to solve with a predictive model. They consist of data and the problem to be solved, and are looking for algorithmic solutions: 

* **Predicted variable** The target variable that the Solution predicts. e.g. Estimated default probability for a borrower
* **Labeled data set** The historical data set to be used for training and evaluation. e.g. The historical record of all borrowers with whether they defaulted or not. This is divided into a test data set that is publicly available and a training data set that is used by miners to evaluate the accuracy of the model. 
* **Evaluation criteria** The measure that should be used to determine model accuracy. [Logarithmic loss](http://scikit-learn.org/stable/modules/generated/sklearn.metrics.log_loss.html) is a commonly used metric for classifiers but we should support a cost matrix that will allow the Decision to specifically weight error from false positives, false negatives, et al.  

### Models 
Models are the proposed solutions to Decisions. They expose an API that, given one or more labeled items of data, will respond with their estimate of the predicted variable. 
 
* **Decision** The address of the Decision this solves. 
* **Endpoint** The endpoint where the model lives. (This is hashed so it can only be evaluated by a qualified miner.) 
* **Score** The score when the Model was evaluated against the testing data set.   
* **Minimum price** The minimum amount of DC required to execute the model on a single Request.  
* **Payment address** The address that should receive payment. 

### Requests
Requests are the individual decisions that businesses want to make using Models. Businesses submit Requests for evaluation by the best Model within their pricing parameters. 

* **Decision** 
* **Maximum price** The maximum amount of DC that the business is willing to pay for having each record evaluated by the model. 
* **Number of records** The number of records the business wishes to evaluate. 
* **Expiration time** How long the Request will remain open. 
* **Payment address** The address that provides payment for the model execution. This will be a proxy that holds Max Price * # of records and will distribute payment after model execution. 

## Putting it all together: Matchmaking & Model Evaluation
During each epoch, miners will do the following: 

1. Identify any expired Requests and eliminate them. 
2. Identify all matching Requests and Models, execute the models, and transfer DC appropriately. 
3. Test any new Models that have been submitted for existing Decisions. (More detail on this process to come, including staking & bounty mechanisms)

## Data Enrichment
Data enrichments can make Models more accurate by enhancing the training data. This can be one of two things: 

1. Append additional data to data records. e.g. A credit score or custom risk model may be appended to a borrower's record.   
2. Provide additional labeled training data that can be used to improve performance. 
 
Like Models, we track the effectiveness of each Enrichment towards improving model accuracy. Enrichments contact 

* **Decision** The address of the Decision this enriches. 
* **Model** The address of the Model this enriches. Enrichment's impact is model dependent.
* **Endpoint** The endpoint where the data enrichment lives (for appends)
* **Score improvement** The increase in score when the data enrichment is used. 
* **Minimum price** The amount of DC required to use the data enrichment on a single Record.  

## Model Ownership, Staking and Bounties 

Ownership of an accurate Model in a Decision with high demand can be highly lucrative. The DecisionCoin token is designed to encourage a wide range of activity regarding trading and monetizing this interest. The same mechanisms also apply to data enrichments. 

### Ownership resale
Ownership stakes in a Model or Data Enrichment can be re-sold at any time. Each owner has the ability to put a price on their ownership and sell a stake. This allows for a healthy dynamic between risk capital that supports the creation of new algorithms and businesses that can best exploit the profit potential of those algorithms.   
   
### Bounties & Staking
While some data scientists will want to benefit from an ownership stake over time, others may be interested in selling their code for an immediate bounty payment. Speculators can create bounties that will pay qualified Models for their code. The DECIDE network will determine when parameters are met and provide a Proxy for that transfer. 

Anyone can create a bounty by staking DC and ownership of the resulting Model is shared among those who provided the stakes. Owners determine how data will be sourced, the criteria for identifying the best algorithm, bounties payable to data owners and data scientists, and how the algorithm may be used.  Decisions must have a minimum bounty committed (currently 1000 DC) or a minimum volume of requests (currently 100 DC) before they go live. This will ensure the Decision is high-value enough to attract the attention of talented data scientists.

Open question
1. Economic split among owner, model builder, data providers and execution cost.  
2. Exclusivity (i.e. Whether the solution is available as a public API or is reserved for the owners.)  

Owners of the Model can also elect to change these at any time.

## Token

DecisionCoin will initially be an [ERC-20](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-20-token-standard.md) token that enables the DECIDE network to solve problems.

That said, there are significant advantages to an dedicated blockchain. Ethereum's cost for data and processing may prove prohibitive and a mining scheme that supports the token directly is much more attractive. We will evaluate whether to migrate to a standalone blockchain in the next six months. [Need to layout criteria for this switch] 

### Links
* [Crowd-sourced Ethereum reading](https://github.com/Scanate/EthList/blob/master/README.md)
* [Coinlist imperative of blockchain token compliance](https://medium.com/@rzurrer/coinlist-the-saft-the-imperitive-of-blockchain-token-compliance-f5ce9cdbc238)
* [Pre-pub Bitcoin text book](https://d28rh4a8wq0iu5.cloudfront.net/bitcointech/readings/princeton_bitcoin_book.pdf)
* [Law](https://www.coinbase.com/legal/securities-law-framework.pdf)
* [Safe ICO practices] (https://medium.com/@wmougayar/safe-ico-practices-sip-c77a0c28f5d6)
* [Argon Group pitch](./research/Argon 2017-07 ICO Considerations.pdf/)
* [Pantera ICO fund deck](./research/Pantera ICO Fund Presentation.pdf)
* [Coinbase State of Blockchain](./research/State-of-Blockchain-Q2-2017-.pdf)
* [What I look for in Cryptocoins](https://jordancooper.blog/2017/05/23/what-i-look-for-in-cryptocoins/)

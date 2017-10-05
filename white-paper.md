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

Commercial solutions exist in each category but they suffer from the same problem: it's difficult to determine which solution provides the best* solution. This is true for a couple of reasons:
1. Bad software sometimes has great salespeople, and vice-versa.
2. Testing the efficacy of a new solution against the status quo takes time, effort and expertise
3. Implementing a new solution in a production environment is difficult and time-consuming. 
 
DECIDE solves these problems through a consensus blockchain that maintains a record of the best* solution for a variety of problems and a standardized API that makes it easy to run the most effective model in production at all times.   

*The best solution is often the most accurate, but may also include other considerations like cost, absence of false positives/negatives, etc.  

## Decisions

Decisions are the key entities within the DECIDE network. Decisions are [DAOs](https://en.wikipedia.org/wiki/Decentralized_autonomous_organization) that are established to solve a specific decisioning problem.  

Anyone can create a new Decision by staking DC and ownership of the economic interest is shared among those who provided the initial stakes. Owners determine how data will be sourced, the criteria for identifying the best algorithm, bounties payable to data owners and data scientists, and how the algorithm may be used.  

Each Decision is governed by smart contracts that describe how it works:
1. Target metric (including minimum thresholds, deadline). 
2. Bounty payable for data 
3. Bounty payable to best algorithm
4. Economic split among owner, model builder, data providers and execution cost.  
5. Exclusivity (i.e. Whether the solution is available as a public API or is reserved for the owners.)  
6. Endpoint for model evaluation

Owners of the DAO can also elect to change these at any time.

### Ownership privileges
The owner(s) of the Decision have the ability to execute the model. 

### Minimum bounties
Decisions must have a minimum bounty committed (currently 1000 DC) before they go live. This will ensure the contest is high-value enough to attract the attention of talented data scientists.   

### Ownership resale
Ownership stakes in a Decision can be re-sold at any time. Each owner has the ability to put a price on their ownership. This allows for a healthy dynamic between risk capital that supports the creation of new algorithms and businesses that can best exploit the profit potential of those algorithms.   

## Mining

Miners can earn DC by executing models. Each  


## Token

DecisionCoin is an [ERC-20](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-20-token-standard.md) token that enables the DECIDE network to solve problems.

There are real advantages to an independent blockchain. We will evaluate whether to migrate to a standalone blockchain in the next six months. [Need to layout criteria for this switch] 

### Coin Allocation:
* 40% - Bounties and Data Incentives
* 30% - Team
* 10% - Marketing
* 10% - Administration & ICO process
* 5% - Contractors 
* 5% - Contingency 

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

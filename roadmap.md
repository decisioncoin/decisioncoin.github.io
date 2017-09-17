# Technical roadmap

## Token development
- Create token (ERC20)
-- Determine supply
-- Any other viable alternatives?
-Define & develop smart contract(s)
--Distribute bounty to winning modeler
--Distribution execution fees to  

## Models
- What do standardized models look like? (R, Python, et al). 
- Are there standards for portability? 
- Support open neural network standard? 

## Pipeline from model to API
- Automatically create a version of each executable model on AWS. We will mark this up by 100% of the execution cost but we can use this to help others launch fast.
- Develop CloudFormation script to execute models on AWS
1 Developed models transform to AWS Lambda function
2 API gateway created
3 Handle authentication / tokenization & how it interacts with blockchaim

* Outside AWS distribution: create a docker image that can execute model

## Solutions we will solve
For each problem domain, we will create a page that looks like the following: 
https://www.kaggle.com/c/state-farm-distracted-driver-detection

DC owners can stake their coins in support of problems that need either an improved solution or data and receive a portion of the proceeds.   

For each domain:
- Problem description
- Bounty (in DC)
- Data dictionary
- Training data
- Test data
- Execution price
- API documentation (if solution is available) 

## Problems
- Cheaters. This can be:
1. A maliciously targeted algorithm that demonstrates superior performance when it shouldn't. This will self-correct, but we need to have solutions here.  
2. Bad data. This could be accidental or malicious, but we need algorithms to detect potential cheaters and a mechanism for punishing them. 
--- Can we reverse a transaction through consensus? Is this a bad idea? 
- Overfitting

## Encryption of data sets
- [Homomorphic encryption](https://en.wikipedia.org/wiki/Homomorphic_encryption) allows data to be shared and manipulated without giving away the secret
-- Need proof of concept that will execute a model and return data 
-- Fully homomorphic encryption expands data size dramatically
-- Partial homomorphic encryption is simpler and can 
- Numerai is using encryption using two neural nets. (One net finds features and the other attempts to decrypt the signal.)
- Unclear that this is "truly" protected but worth investigating


## Things we need to solve / evaluate
1. Allow a provider of compute resources to execute models withouth getting access to the underlying model (homomorphic encryption?)
2. Encrypt a data set so that a data scientist can work on a solution withouth sharing the data publicly
3. Very large data sets
4. Very fast execution (e.g. real-time bidding) 
5. How to trickle payment over time to share rish


TODO: Convert these to github issues in core repo.
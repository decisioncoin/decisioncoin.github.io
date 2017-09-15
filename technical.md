# Technical development

## Token creations
-Create token (ERC20?)
-Are there other viable alternatives

## Define & develop smart contract(s)
-Need to figure out best practices here


## Pipeline from model to API
We should automatically create a version of each executable model on AWS. We will mark this up by 100% of the execution cost but we can use this to help others launch fast.
Develop CloudFormation script to execute models on AWS
1 Developed models transform to AWS Lambda function
2 API gateway created
3 Handle authentication / tokenization & how it interacts with blockchaim

For each domain:
-Data dictionary
-Training data
-Test data

What do standardized models look like? (R, Python, et al). 
Are there standards for portability? 
Support open neural network standard? 

## Problems
-Overfitting
-Cheaters. This can



## Things we need to solve / evaluate
1 - Allow a provider of compute resources to execute models withouth getting access to the underlying model (homomorphic encryption?)
2 - Encrypt a data set so that a data scientist can work on a solution withouth sharing the data publicly
3 - Very large data sets
4 - Very fast execution (e.g. real-time bidding) 
5 - How to trickle payment over time to share rish


TODO: Convert these to github issues in core repo.
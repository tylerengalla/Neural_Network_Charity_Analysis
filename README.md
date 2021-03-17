# Neural_Network_Charity_Analysis

## Overivew
Use Deep Machine Learning and Neural Networks to create a binary classifier that is capable of predicing whether organizations applying for funding from our company, Alphabet Soup, will be successful. 

We've been given a CSV containnig more than 34,000 organizations that have recieved funding from Alphabet Soup over the years. The columns capture metatdata about each organization such as the following: 

- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special consideration for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively


## Results
### Data Preprocessing
- Target Variable: IS_SUCCESSFUL—Was the money used effectively or `y = application_df["IS_SUCCESSFUL"].values`
- Feature Variables: `X = application_df.drop(["IS_SUCCESSFUL"],1).values`
- Noisy Features: EIN and NAME—Identification columns

### Compiling, Training, and Evaluating the Model
- For our model we tested 2 and 3 hidden neuron layers and tested with activation functions such as 'relu' and 'sigmoid' 
- I was unsuccessful in reaching out target model performance within my 3 attempts of tinkering the hidden layers, activation functions, and removing additional potential noisy features. With more time and attempts I'm sure the goal of 75%+ accuracy could be hit. 


## Summary 
Optimizing a Machine Learning and Neural Network model takes time and doesn't happen within 3 attempts. 
- From my original model, in my first attempt to get the accruacy above 75%, I increased the number of hidden layers by 1 as well as increasing the number of nodes per layer which gave me a marginal increase in accuracy. 
- In attempt 2, I then went to switch up my activaion functions from sigmoid to tanh, while keeping the nodes and layers from my first attempt, which restulted in a significantly worse accuracy. 
- Our third and final attempt was back to our first attempt activation function of sigmoid with an increase of nodes per hidden layer while attempting to remove additional columsn that may be noisy. This resulted in my worse accuracy score of 63%. 

This means we probably removed columns that aren't actually noisy that hurt our model so to reach our goal I'd probably start by only removing one additional column at a time vs multiple and go from there. 


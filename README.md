# deep-learning-challenge


## Analysis

My goal for this project was to develop and optimize a model to help the Alphabet Soup nonprofit select applicants that were successful in their own ventures.

### Preprocessing

Each applicant had multiple fields that I was interested in such as:
- APPLICATION_TYPE — Alphabet Soup application type
- AFFILIATION — Affiliated sector of industry
- CLASSIFICATION — Government organization classification
- USE_CASE — Use case for funding
- ORGANIZATION — Organization type
- STATUS — Active status
- INCOME_AMT — Income classification
- SPECIAL_CONSIDERATIONS — Special considerations for application
- ASK_AMT — Funding amount requested
- IS_SUCCESSFUL — Was the money used effectively

The main target for the model is the "IS_SUCCESSFUL" column that I wanted the model to effectively predict. The data also included the name and ID number of the applicants which were dropped because they have no effect on the outcome. The "CLASSIFICATION" and "APPLICATION_TYPE" were reorganized to show only the most relevant types

### Compiling, Training, and Evaluation

The model split the data into a large training set and then used that training set to try and predict whether the applicant is successful or not of the smaller testing set. I used only two hidden layers because when adding more layers the model's accuracy decreased and computation time increased. The first layer with 16 neuons the second with 10 then the activation layer had 1. Decreasing the number in each layer simplifies the process and cuts down on computation time. However, I was not able to get the model to 75% accuracy. I rebinned the data and added hidden layers and even tried different activation functions and optimizers. I think with a couple more trys the model would slowly increase with taking the best of each run.

## Summary

A neural network model may be too complex and overkill for this type of data. There isn't enough dimensions to justify having to use TensorFlow. I would suggest using a supervised learning model such as random forests to get a more accurate prediction without the high computational costs when using a neural network model. 








source for finding values counts of CLASSIFICATION
- https://stackoverflow.com/questions/22320356/pandas-get-values-from-column-that-appear-more-than-x-times


source for activation list
- https://www.tensorflow.org/api_docs/python/tf/keras/activations

source for optimizer list
- https://www.tensorflow.org/api_docs/python/tf/keras/optimizers
# Neural_Network_Charity_Analysis
---
Creating a `deep-learning`, `neural network` to analyze and classify the success of charitable donations

## Challenge Overview
---
The purpose of this analysis is to build a deep learning neural network with at least 75% predictive accuracy of determining the success or failure of charitable donations to non-profit companies. This neural network is built to help a foundation make future decisions on which companies should receive charitable grants, based on historical data. The dataset provided contained information from 34,000 organizations and captured metadata, both categorical and continous features, that could potentially be used to build a model with high preditive accuracy.

_Features included:_
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

_Target variable_:
  - IS_SUCCESSFUL—Was the money used effectively


## Features and Data Resources
---
- Data Source: `charity_data.csv`
- Data Tools: `AlphabetSoupCharity.ipynb`, `AlphabetSoupCharity_Optimization`
- Software: `imbalanced-learn`, `skikit-learn`, `TensorFlow` `Jupyter Notebook` and `Python.9.2.3`

## Challenge Deliverables
---
- Deliverable 1: Preprocessing Data for a Neural Network Model
- Deliverable 2: Compile, Train, and Evaluate the Model
- Deliverable 3: Optimize the Model
- Deliverable 4: A Written Report on the Neural Network Model (README.md)

## Results
---
_Data Preprocessing_
- Target variables: 
   - "IS_SUCCESSFUL"
  
- Feature variables: 
   -"APLICATION_TYPE"
   - "CLASSIFICATION"
   - "USE_CASE"
   - "ORGANIZARION"
   - "STATUS"
   - "INCOME_AMT"
   - "SPECIAL_CONSIDERATIONS"
   - "ASK_AMT"
   
- Removed/droped variables:
   - 'EIN'
   - 'NAME'
    

- _Compiling, Training and Evaluating the Model_
    __Best performance characteristics:__
    - Number of hidden layers: 2
    - Number of neurons per layer: 100 (hidden nodes layer1), 40 (hidden nodes layer2)
    - Activation functions used: Relu, Relu, Sigmoid (Output layer)

<img width="797" alt="model_metrics1" src="https://user-images.githubusercontent.com/77628698/123284858-6dbfe000-d4c1-11eb-9e6e-b348ca41bcd3.png">

<img width="820" alt="model_metrics2" src="https://user-images.githubusercontent.com/77628698/123284873-71ebfd80-d4c1-11eb-8fb6-c76cf870e0fc.png">

<img width="692" alt="plot_accuracy" src="https://user-images.githubusercontent.com/77628698/123286108-7a910380-d4c2-11eb-824f-7285e844f0a0.png">

 __Attemps Taken to Improve Performance:__
 - Attempt 1:

<img width="801" alt="attemp1 1" src="https://user-images.githubusercontent.com/77628698/123286011-62b97f80-d4c2-11eb-98b4-10fb2ee02d25.png">

<img width="854" alt="attemp1 2" src="https://user-images.githubusercontent.com/77628698/123286031-6816ca00-d4c2-11eb-9dc4-cdc03008a915.png">

<img width="835" alt="attempt1 3" src="https://user-images.githubusercontent.com/77628698/123286060-6f3dd800-d4c2-11eb-83eb-b3996c53b419.png">

- Attempt 2:

<img width="693" alt="attempt2 1" src="https://user-images.githubusercontent.com/77628698/123286163-88df1f80-d4c2-11eb-8058-eb0394f3883f.png">

<img width="799" alt="attempt2 2" src="https://user-images.githubusercontent.com/77628698/123286189-8da3d380-d4c2-11eb-9576-9cc39c77e930.png">


## Summary
---
Overall, due to possible overfitting of features and reducing variance and rare occurances of variables, my model was not able to acheive the 75% predictive accuracy threshold requested by the challenge prompt. Through the process of attempting to optimize the model, I saw first hand that sometimes it is prefferable to keep the model less complicated with fewer hidden layers, epochs and neurons--the complexity of the deep learning neural network should appropriately match that of the input data, thus corroborating the notion that a deep learning model only needs a couple hidden layers to acheive high predictive accuracy on both training and testing data. 
For further analysis, I would use a SVM model to solve the classification problem (effective charity donations). Using SVMs are beneficial because they specialize in identifying a singular output or target variable, which is what this dataset calls for. SVMs also adequately build models with linear or non-linear data, a benefit when working with categorical metadata.

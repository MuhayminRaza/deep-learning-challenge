# deep-learning-challenge

**Analysis Report**

**Overview of the Analysis**
The purpose of this challenge was to use the features provided in the dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup. The dataset had a number of columns: 
- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special considerations for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively

  After preprocessing the data, the model was compiled, trained and evaluated and then optimized.

  **Results**

**Variables**
Target variable: IS_SUCCESSFUL

Feature Variables: 
- APPLICATION_TYPE
- AFFILIATION
- CLASSIFICATION
- USE_CASE
- ORGANIZATION
- STATUS
- INCOME_AMT
- ASK_AMT

Neither targets or features: N/A

Results:
  
<img width="637" alt="image" src="https://github.com/MuhayminRaza/deep-learning-challenge/assets/131730274/cdef241b-f180-4126-9770-ab6587b64327">

Figure 1: Starter Model

<img width="624" alt="StarterModel2" src="https://github.com/MuhayminRaza/deep-learning-challenge/assets/131730274/3a104b5c-4c11-4b43-a101-d37c5a129f69">

Figure 2: The evaluation of the model shows an accuracy of 73.17%.


During the optimization, for Attempt #1, the epoches were kept the same at 100 (see Figure 3) and later increased to 200 (see Figure 4). 

<img width="464" alt="opt_attempt_1" src="https://github.com/MuhayminRaza/deep-learning-challenge/assets/131730274/6bf3ff6d-7e97-4310-9e00-611a0ff8a7e8">

Figure 3: epoch = 100

<img width="427" alt="opt_attempt_2" src="https://github.com/MuhayminRaza/deep-learning-challenge/assets/131730274/30b6984c-b01d-49d4-b5b8-a7efb8bb4277">

Figure 4: epoch = 200

Figure 4 shows a larger accuracy % - attempts were made at changing the epoches (100 to 200) and the output shape (90/40) to (100/40), however the effect on the accuracy did not seem too significant. In the end, the target of 75% accuracy was not reached. 


**SUMMARY**

In the first model, the accuracy was about 73.17%. In the optimization attempts, the model was no able to reach the 75% threshold despite changes in the layers, neurons and epoches. 

A different model may be needed such as logistic regression as it is a relatively good model for binary classification. 





The following code was written with the help of a TA and ASKBCS: 

nn.add(tf.keras.layers.Dense(units=hidden_node_1, activation='relu', input_dim = input_features))

nn.add(tf.keras.layers.Dense(units=hidden_node_2, activation='relu'))

nn.add(tf.keras.layers.Dense(units=1, activation='sigmoid'))

# AlphabetSoupCharity
Module 20 Challenge

## Overview
For this challenge, we were helping to analyze each donation to determine which charities should receive the money. That way we can confirm that the foundation's resources are being used effectively. We used a nueral network to predict the sucess of the potential projects.

## Results

### Data Preprocessing
- Target variable: IS_SUCCESSFUL
- Model features: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT
- Variables removed: EIN, NAME

### Compiling, Training and Evaluating the Model
- The initial model run had 2 hiddent layers. The first hidden layer had 80 nuerons while the second had 30 nuerons. I employed the relu activation for the hidden layers and the sigmoid activation for the output layer. 
- The accuracy for the firts model was only 65% and our target was 75% so it was not successful.
![image](https://user-images.githubusercontent.com/115592394/225463892-144e7eef-64ae-4912-adf5-166a55104651.png)

- Our first optimization model reduced the applicatio_counts to 400 and the classification_counts to 1200. I also increased the nuerons in the hidden layers to 100 and 40. This actually resulted in a decreased accuracy at 63%.
![image](https://user-images.githubusercontent.com/115592394/225464305-32015f0e-3929-4da6-9294-97263bcd4528.png)

- For the second optimization model I kept everything the same except I increased the number of Epochs to 100 from 50. This resulted in an increased accuracy score of 70% but that still did not meet our target. 
![image](https://user-images.githubusercontent.com/115592394/225464580-348bada0-3cb2-40f8-bddb-2b50619f7b0f.png)

- The third optimization model saw me reduce the application_counts and classification_counts even further to 300 and 800 respectively. Additionally, the nuerons in the hidden layers were increased to 125 and 50 while the Epochs remained at 100. This changed reduced the accuracy back down to 63%.
![image](https://user-images.githubusercontent.com/115592394/225464843-ca1d3e93-eb12-4321-b0da-4ab1dae167fc.png)

## Summary
We were ultimately unsuccessful in meeting our target accuracy of 75%. In order to reach that target, I would run some new optimizations with new activation functions or even adding in a new 3rd hidden layer to see if that will provide the boost we need. 

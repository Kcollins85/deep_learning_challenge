# deep_learning_challenge

## Overview:

In this analysis we are looking to create a Neural Network model that can predict whether applicants will be successfully funded by Alphabet Soup using a historic dataset.


## Results

### Data Preprocessing

I used "Is Successful" as my target (y) variable for this model, all other columns were used as the features (X) variable

Fields "EIN" and "Name" were removed from the data as they were neither target nor features.
I also considered removing Use Case and Organisiation as I didn't believe this would be suitable to the dataset. (should these be removed??)

### Compiling, Training, and Evaluating the Model

Model 1: AlphabetSoupCharity
Using the rule of thumb that for every feature you should use 2-3 neurons for optimal results, I started with 2 hidden layers and below set up for my initial model:
- Layer 1:86, activation "relu"
- Layer 2: 129, activation "relu"
- Final Layer: 1, activation "sigmoid"
- I ran the model for 100 epochs

![image](https://user-images.githubusercontent.com/116396662/234175233-8f4beabf-54ca-47b7-bc72-c08747d86d43.png)

Based on the above I got a loss of 0.5695, and accurary of 0.7284.  The loss rate of 0.5695 means we still have alot of work to do to optimise the model.

Model 2: AlphabetSoupCharity_Optimisation
For the 2nd model, I tried to reduce the number of columns for "classification" as well as add another layer to the model.
Still using the rule of thumb that for every feature you should use 2-3 neurons for optimal results. below was my set up for my second model:
- Layer 1: 80, activation "relu"
- Layer 2: 120, activation "relu"
- Layer 3: 80, activation "relu"
- Layer 4: 120, activation "relu"
- Final Layer: 1, activation "sigmoid"
- I ran the model for 100 epochs

![image](https://user-images.githubusercontent.com/116396662/234175258-06fb0329-5bc4-44a9-b237-e5e4ef5c0fbf.png)

Based on the above I got a loss of 0.5956, and accurary of 0.7289.  This had a higher loss rate, however similar accuracy rate to the first model.  As the loss rate was higher here, and we still haven't hit the 75% accuracy mark, there is more testing to be done.

Model 3:AlphabetSoupCharity_Optimisation2
For the final model, I tried to switch things up a bit given going by the rule of thumb advice doesn't seem to be working for this analysis.  Below wwas the set up for my final model:
- Layer 1: 120, activation "relu"
- Layer 2: 240, activation "relu"
- Layer 3: 240, activation "relu"
- Layer 4: 150, activation "relu"
- Final Layer: 1, activation "sigmoid"
- I ran the model for 50 epochs

![image](https://user-images.githubusercontent.com/116396662/234175271-0173dd97-262c-4a11-9787-d0314c7ab078.png)

Based on the above I got a loss of 0.567 and accuracy of 0.728.  This had similar results to the first model.

## Summary: 

Summarise the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

It seems as though this is a tough dataset to crack. It likely needs alot of layers to split out the data.  It is like that using the Keras Tuner Function to run through multiple options will be the best starting point on this dataset.



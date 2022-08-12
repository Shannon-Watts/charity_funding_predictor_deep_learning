# Deep Learning: Neural Networks 
## Charity Funding Predictor Report


The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. I created a binary classifier to predict whether applicants will be successful if funded by Alphabet Soup.

## Results: Data Preproccessing 

- The target variable for the model was the successfulness of the funding application.
- The feature variables included: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT   
- The variables that were removed from the data were 'EIN', an organisation number, and the NAME of the organisation as they are neither targets or features. 

## Results: Compiling, Training, and Evaluating the model
- In the first optimization 2 layers were used with 
- The model did not achieve the target model performance until the number of neurons in the layers were increased substantiially. I increased the number of neurons in multiples until I reached a number where the model performance exceeded the target performance. 
- In addition to increasing the number of neurons I also increased the number of epochs from 120 to 200. I began with 120 as a good general rule for choosing the number of epochs is 3 times that of the number of features. Howeever, this number seemed to low and the performance of the model would not reach optimization. Therefore I increased the number slightly. I believe the reason for this is the complexity of the model. 

The optimal model contained the following:
Layers: 2
Neurons: 
Activation functions: relu and sigmoid 
Epochs: 200

## Summary 
Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

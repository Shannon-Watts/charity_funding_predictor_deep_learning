# Deep Learning: Neural Networks 🧠
## Charity Funding Predictor Report


The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. I created a binary classifier to predict whether applicants will be successful if funded by Alphabet Soup.

## Results: Data Preproccessing 

- The target variable for the model was the successfulness of the funding application.
- The feature variables included: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT   
- The variables that were removed from the data were 'EIN', an organisation number, and the NAME of the organisation as they are neither targets or features. 

## Results: Compiling, Training, and Evaluating the model
In the first optimization 2 layers were used with a small number of neurons and 100 epochs, with the reul and sigmoid activation functions. 

I then tried various differetiations of neurons and epochs but the accuracy did not exceed approx 73%
![image](https://user-images.githubusercontent.com/100214297/184418169-c24710a4-079b-4f76-8f25-1bd5754b8b34.png)

The model did not achieve the target model performance until the number of neurons in the layers were increased substantiially. I increased the number of neurons in multiples, however, this did not improve accuracy.

Then I tried to increase the epochs from 120 to 200. II began with 120 as a good general rule for choosing the number of epochs is 3 times that of the number of features. Howeever, this number seemed to low and the performance of the model would not reach optimization. Therefore I increased the number slightly to account for the complexity of the model. 

![image](https://user-images.githubusercontent.com/100214297/184417410-0480e54d-dc8f-4a98-b7e9-8546cb3371b0.png)

Upon evaluation, however, I noticed that the accuracy tended to flatten once the number of epochs exceeded 100. This was the main reason why I introduced a third hidden layer as the reason the model was not reaching the target performance. 

By introducing a third hidden layer the model was aiming to combat the complexity of the data, however, despite adding in a third layer and increasing the number of neurons in the hideen layers the model did not reach the target performance. 

I changed the activation function from sigmoid to tanh. The result of changing the activation function and then reducing the number of neurons in the hideen layer meant that less epochs could be used, however, the model performance target was still not reached. 

Therefore, I decided to use keras hyperparameter tuning to run through trials and establish the best parameters for the model:

![image](https://user-images.githubusercontent.com/100214297/184427274-30fdfe6f-dc70-43c4-9f89-9155a3efe2be.png)


The optimal model contained the following:
Layers: 3
Neurons: 
Activation functions: relu and sigmoid 
Epochs: 200

## Summary 
Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

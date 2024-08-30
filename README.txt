Business Problem:
We are attempting to determine which features of a used car most impact the price of it. 


Methodology:
Using data from the vehicles.csv file in the data/ folder, I cleaned the data and split it into a train and test set. I built several machine learning models using the training data and predicting the price. From these models, I chose the best one by finding the one that minimized mean squared error on the test data, as that is an industry best practice. 


I then used permutation_importance to determine the top 2 impactful features. As a final validation, I built the same type of model as the best model chosen before, but only trained it on these 2 features. 


The full notebook and analysis can be found at https://github.com/AbbyWilson/price_of_a_car/blob/main/price_of_a_car_analysis.ipynb


Findings:
The permutation_importance indicated that cylinders and condition are the most important features in determining the price of a used car. In fact, when I built a model using just these two features, the mean squared error only increased a bit and the model actually performed better than some of the other models I had built on all features. 


Recommended Next Steps:
As we now know that cylinders and condition are the two most important features impacting the price of a used car, I have a few recommendations. One - source cars that are in good condition. Second, as I do not know much about how cars are made, I would recommend using your industry knowledge to determine which number of cylinders is most appealing. If you are not sure, we can consider doing further analysis to try to understand which number is best.


A note if replicating or re-running this analysis - consider re-cleaning the data to replace the cylinders column directly with integers representing the number of cylinders, instead of the one hot encoding version. I would recommend this in future if another analysis were to be done as it is just a bit cleaner. However, I don’t expect output to be meaningfully different as it is just a different way to represent the same information.
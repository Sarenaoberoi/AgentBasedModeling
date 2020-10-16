## Random Forest

#### Decision Trees

Before we begin talking about the number of applications of the Random Forest, it is important to understand the the decision tree. Decision Trees are the basis of the Random Forest, and together, make up a a forest. A decision tree is a common tool used to determine the best option from different consequences. Depending on the specificities of the model, a decision tree can incllude a number of different aspects when choosing an option, including the probability of the certain event occuring, cost effectiveness, and more. One problem that is often observed with the applicaiton of decision trees, is overfitting. Overfittin occurs when the model is able to correctly determine all the **training data**. Although it may seem like the model is performing well, its accuracy will decrease after being introduced to new data (not part of the training data). Overfitting often occurs when the model has merely learned all the training points, but will struggle to identify variables outside of the training data.  After understanding the decision tree, we can begin to understand the a Random Forest, which is the decision tree but at a higher scale.

The image below is a simple representation of a decision tree:

<img width="659" alt="Screen Shot 2020-10-16 at 8 42 29 AM" src="https://user-images.githubusercontent.com/60228365/96259664-ed3cfd00-0f8b-11eb-80d4-abac20767a36.png">


#### Random Forest

One great way to decrease the overfitting of a decision tree, is to use the Random Forest method. A random forest is a collection of decision trees. Each tree in the Random Forest model is tranined on a random collection of points. The model also incorporates 'bootstrapping', in which the same data points will be used multiple times. In the Random Forest model, the different features are spread out evenly among the different nodes. After all trees are in place, the outcomes from each tree are averaged together in order to obtain a final outcome prediction. 


#### Random Forest Application

The Influenza virus is a common virus that infects almost 60.8 million individuals every year. The Influenza Virus is known for its ability to rapidly change year to year, making it difficult for scientists to predict how bad the virus will be every year. Scientists have come together to develop a Random Forest model, along with other data science methods, to develop a comprehensive framework that is able to predict the spread of the virus. For years, scientists have tracked the spread of the virus using a number of different surveillance methods, which will be very helpful in creating the Random Forest model. There were 6 different target variables included in the model, with some of them being, the perecnt of individuals with influenza symptoms out of indiviuals that went to doctor and the peak week and peek intensity of flu season. Each model consisted of 500 trees which each included 73 different predictors that all worked together to predict the 6 target variables. The Random Forest was much more accurate than the individual decision trees, with an accuracy of 87%, compared to the individual tree of 67%. Although the Random Forest model was seen to overfit slightly, it was not nearly as much as seen in the individual decision trees.  

## Random Forest

#### Decision Trees

Before we begin talking about the number of applications of the Random Forest, it is important to understand the the decision tree. Decision Trees are the basis of the Random Forest, and together, make up a a forest. A decision tree is a common tool used to determine the best option from different consequences. Depending on the specificities of the model, a decision tree can incllude a number of different aspects when choosing an option, including the probability of the certain event occuring, cost effectiveness, and more. One problem that is often observed with the applicaiton of decision trees, is overfitting. Overfittin occurs when the model is able to correctly determine all the **training data**. Although it may seem like the model is performing well, its accuracy will decrease after being introduced to new data (not part of the training data). Overfitting often occurs when the model has merely learned all the training points, but will struggle to identify variables outside of the training data.  After understanding the decision tree, we can begin to understand the a Random Forest, which is the decision tree but at a higher scale.

The image below is a simple representation of a decision tree:



#### Random Forest

One great way to decrease the overfitting of a decision tree, is to use the Random Forest method. A random forest is a collection of decision trees. Each tree in the Random Forest model is tranined on a random collection of points. The model also incorporates 'bootstrapping', in which the same data points will be used multiple times. In the Random Forest model, the different features are spread out evenly among the different nodes. After all trees are in place, the outcomes from each tree are averaged together in order to obtain a final outcome prediction. 


#### Random Forest Application



## K-NN Nearest Neighbor Algorithim

The K-Nearest Neighbors algorithim is a supervised machine learning method that is commonly used in a variety of fields. Before we can get into the implimentation of the fascianting algorithim, it is important to first understand what a supervised machine learning method entails. With supvervised machine learning, the individual creating the algorithim will input specific data that already contains the correct labels. The algorithim will learn the data that was inputted (with the correct labels), and when inputted with data that is not paired with labels, the algorithim should be able to successfuly label the data based on what it has learned. This method of machine learning is very common for problems that involve the classifiation of pictures or data. However, this method can also reach beyond classification problems, into regression problems. A classification problem often has discrete outcomes –– The image inputted was a wolf OR a zebra. On the other hand, regression problems output real numbers that can differ greatly –– determing a weight after being given a height. 

Example: 

Similar points are grouped together 
<img width="397" alt="Screen Shot 2020-10-29 at 10 22 04 AM" src="https://user-images.githubusercontent.com/60228365/97586566-c8f01000-19d0-11eb-8fcf-6ecee2302287.png">


Example of Classification Problem - Do you like pineappple pizza? Yes (1) and No (0)
<img width="330" alt="Screen Shot 2020-10-29 at 10 23 14 AM" src="https://user-images.githubusercontent.com/60228365/97586576-cc839700-19d0-11eb-9467-0df87108b93f.png">



Example of Regression Problem - Height and Weight 
<img width="440" alt="Screen Shot 2020-10-29 at 10 23 07 AM" src="https://user-images.githubusercontent.com/60228365/97586581-ce4d5a80-19d0-11eb-855e-4e99534d5151.png">



Now that we have a comprehnsive understanding of supervised machine learning, we can move into K-Nearest Neighbors! This algorithim is easier to understand when compared to the real world. The K-NN algorithim is based on the fact that points of similar nature will most likely stay realitvely close to one another. For example, looking out into nature, we can see that wolves most commonly travel in packs. This is the same as going into the ocean and seeing schools of clownfish swimming together. 

## Implimenting the Algorithim

The first step in putting the algorithim to use is bringing in your data. After your data has been loaded in, you can choose a K value. Choosing a K value that will give the best results in critical, but the best way to find this K is to try many different values. It is important to note that as the chosen K value decreases, the predictions may become less accurate. With this in mind, it is most reasonable to test your model with higher K values (until finding the best one). The next step is determining the distance between the testing points, and each training point (this should be done for each testing points). Organize the distances in increasing order. 

Using this line of code:

    k_nearest_labels = [data[i][1] for distance, i in k_nearest_distances_and_indices]

You will retrieve the labels for the specific K's you are focusing on.  

Lastly, the algotihim wil return the means of the K Labels. 

Research has shown that the K-NN algorithim has been used in a variety of studies, including making predictions for the economy and stock prices. A Jordanian stock exchange company made use of the algorithim in order to predict stock prices for 6 different companies. 

The K-NN Algorithim, although very useful and accurate for small sets of data, can see problems when being applied to very large sets (slower and less accurate).  


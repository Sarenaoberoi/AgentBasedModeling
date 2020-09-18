## Using Nighttime Light and Satellite Images to Help Predict Human Development in India

### Introduction

Throughout past years, scientists have searched for an accurate, time-efficient, and cost-effective method of determining and tracking human development across the world. Research has shown that census data, although relatively accurate, is extremley difficult to obtain (especially in low and middle income countries). Not only are censuses very expensive to conduct, it can take extended periods of time to conduct an accurate census. Along with this, determining rates of urbanization is critical. In this paper, I will discuss a study that used nightime light data and satellite images along with a convolutional neural network to determine urbanization and human development rates in India. 

### Study

Nightime lights are satellite taken images that detect the presence of lights in certain areas. Nighttime lights can often be a adequate indicator of a country's development, poverty and/or GDP. In term of the study conducted in India, nighttime lights were not sufficient enough for an accurate representation of development, so day time satellite images were taken as well. 

Before creating a convolutional neural network, towns around India were split up into 3 disticnt groups (levels): 1, 2, and 3. The first level was used to represent areas that were underdeveloped, or "Rudementary" (RUD). The second level was an area that was slightly more developed, or "Intermediate" (INT). Lastly, level number 3 was used to represent an advanced or more developed area (ADV). There were 7 different variables used to determine the development of an area: assets, bathroom facilities, Condition of Households, Fuel for Cooking, Main Source of Light, Main Source of Water, Literacy. Depending on how high on the scale these variables were, an area could be labeled with a level of 1, 2, or 3. 

Next, a CNN (convolutional neural network) was trained. A CNN is a commonly used deep learning method that commonly works to differentiate images. The model will begin by having "training" images, along with their corresponding labels, inputted. Once inputted into the model, a CNN will be able to differentiate the images of different labels by looking at specific aspects of each image (and its corresponding label). By looking at the disticnt similarities and differences of images under the same label or different labels, the CNN will be able to develop an adequate understanding of each label, and the images corresonding with that label. 

ResNet:

<img width="516" alt="Screen Shot 2020-09-18 at 11 51 55 AM" src="https://user-images.githubusercontent.com/60228365/93618823-c9df5c00-f9a5-11ea-8307-f0ff166d1988.png">

In this study, two image datasets known as "ImageNet" and "DeepSat" were used to pretrain the CNN model. Both these datasets were images obtained using the Landsat 7 satellite. These two data sets were first modified to get the desired shape and size, and were then trained on a ResNet architecture CNN. The ResNet architecture is a type of convolutional neural network made for very large data sets (includes many convolutions)

The ResNet convolution neural network was successful for the most part. Studies in Africa have shown that the model is successful in predicting areas very similar (in the same country) to the training data, but has a difficult time distinguishing areas outside of the training country. With more data (satellite images, nighttime light data), it is possible to get a more accurate representation of human development.  

### Citation:

- Dagar, A. (2020, September 07). An Approach to Tracking Human Development through Satellite Imagery in India. Retrieved September 18, 2020, from https://towardsdatascience.com/an-approach-to-tracking-human-development-through-satellite-imagery-in-india-7e750b85dc90

- Abdishakur. (2019, November 26). Multi-label Land Cover Classification with Deep Learning. Retrieved September 18, 2020, from https://towardsdatascience.com/multi-label-land-cover-classification-with-deep-learning-d39ce2944a3d

- Jean, N., Burke, M., Xie, M., Davis, W., Lobell, D., &amp; Ermon, S. (2016, August 19). Combining satellite imagery and machine learning to predict poverty. Retrieved September 18, 2020, from https://science.sciencemag.org/content/353/6301/790
 


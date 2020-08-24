## Response 1

#### 1) 

<img width="544" alt="Screen Shot 2020-08-22 at 6 01 54 PM" src="https://user-images.githubusercontent.com/60228365/90979027-173fe900-e520-11ea-93af-711d8c797f2c.png">

plot(x, y) plots points on graph. 


#### 2)

<img width="334" alt="Screen Shot 2020-08-22 at 6 02 28 PM" src="https://user-images.githubusercontent.com/60228365/90979029-19a24300-e520-11ea-8083-1efddd01e2bc.png">

plot(x,y, type = "l") puts a line through points and removes points.  

### 3) 

<img width="306" alt="Screen Shot 2020-08-22 at 6 04 07 PM" src="https://user-images.githubusercontent.com/60228365/90979030-1b6c0680-e520-11ea-87b1-3630c969ec70.png">

plot(x,y, type = "o") keeps points and puts line through them. 

### 4) 
<img width="326" alt="Screen Shot 2020-08-22 at 6 04 50 PM" src="https://user-images.githubusercontent.com/60228365/90979033-1dce6080-e520-11ea-85bd-e42ee8dd4afa.png">

Adding title, x and y axis names, and sub (units of distance = meters)

### 5) 
<img width="322" alt="Screen Shot 2020-08-23 at 8 54 40 AM" src="https://user-images.githubusercontent.com/60228365/90979035-2030ba80-e520-11ea-8d57-0d2134aad89e.png">

lty = linetype

lwd = lineweight

col = pick a color

pch = point symbol

cex = scale of symbol increased or decreased



## Creating More Complicated Plot and Data Frame
### 6) 

<img width="553" alt="Screen Shot 2020-08-23 at 5 01 48 PM" src="https://user-images.githubusercontent.com/60228365/90989709-fef4bc00-e569-11ea-8521-e8921e0af40a.png">

This graph shows 10 squares scattered on the plot. The lines of code 

east <- sample(x, size = 10, replace = TRUE)
north <- sample(y, size = 10, replace = TRUE) 

choose a random number from x and y 10 times. replace = True makes it so that a number can be choosen more than once. rep(0.75, 10) length of each square is 0.75 and there are 10 squares. 

### 7) 

<img width="555" alt="Screen Shot 2020-08-23 at 5 02 28 PM" src="https://user-images.githubusercontent.com/60228365/90989713-00be7f80-e56a-11ea-9a94-2e1851e6bd0a.png">

Randomly choosing 10 circles to be placed on the plot. add = True adds the circles to the already existing plot with the squares. 



### 8)

<img width="555" alt="Screen Shot 2020-08-23 at 5 03 30 PM" src="https://user-images.githubusercontent.com/60228365/90989718-0320d980-e56a-11ea-9fd6-a6da16c5a3fd.png">

Adding larger trees to the plot. fg = symbol border color and bg = color for symbol's fill .


### 10)

<img width="551" alt="Screen Shot 2020-08-23 at 5 44 38 PM" src="https://user-images.githubusercontent.com/60228365/90989721-087e2400-e56a-11ea-82bf-fd3abfff5642.png">

The plot now shows lines added between each dwelling. This is done using lines(). 


## Challenge Question

<img width="442" alt="Screen Shot 2020-08-24 at 11 51 36 AM" src="https://user-images.githubusercontent.com/60228365/91066917-462d8c00-e600-11ea-8b31-72cc07988b8a.png">


<img width="569" alt="Screen Shot 2020-08-23 at 9 32 06 PM" src="https://user-images.githubusercontent.com/60228365/90994856-29557200-e588-11ea-9b86-a0ca5d06c579.png">


This plot shows 50 dwellings, 40 small trees, and 12 large trees. The person visited 7 different homes which can be seen by the spline. The xspline command gave us a curved more continuous line between the 7 homes visited. 


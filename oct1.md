### Project 2


I originally began this project by working with the country Paraguay, but after getting access and analyzing the DHS data, I realized that there was a great deal of important information missing from the households dataset. I switched my country to Uganda, as the data was much more recent, and I had more data to work with.

The plot below shows a planar point pattern of the distribution of households in Altos, Paraguay.

<img width="356" alt="Screen Shot 2020-10-01 at 1 24 16 PM" src="https://user-images.githubusercontent.com/60228365/94925354-112d1880-048d-11eb-841f-fbb742667092.png">

Below, I have placed the specific column name for some of the important variables from the data. 

hv005 : sample weights

hv009 : number of household members 

hv105_01- 27 : Age
  
hv104_01 - 21 : Sex of household members 

I began the project by bringing in some new important libraries, including VIM and haven. After brining in the libraries, I read in the 3 seperate subdivision (adm0, adm1, and adm2). These were also used in project 1. I also read in the raster tif file which included population. After recieving the DHS data for Uganda, I was able to download the files and bring in persons and household data as well. We defined 9 different variables by referncing their speciic columns from the households data frame. These variables were unit, weights, location, size, sex, age, education, wealth, and hhid. Finally, after defining the variables, we created a new data frame using cbind, to bring all the variables into one dataframe. I then filtered my population data into just 1 specific adm1, Lira. I then cropped the masked the population file to Lira (located in Northern Uganda). I had 18506 observations with 4972 variables in my persons object and 19588 observations with 4005 variables in my households object. My hhs data frame which included the 9 variables I specified above had a total of 19588 observations and 87 variables. 

In order to retrieve the spatially located households at adm0, I began by taking the total population of Uganda, and dividing this by the mean household size (object was called uga_hhs_n). The mean household size in my case was around 4.65. Following this step, we created an object called hhs_pts which created a random distribution of points from the object we had just created before. We the finally generated households by sampling from the object uga_hhs_n using the slice_sample command. My weighted error was 9.377076e-03 which is very low!

One important portion of this project was to pivot our gender, age, and education variables. I was able to pivot these variables by looking into the hhs dataframe and finding the specific column numbers that the variable in interest was located in. Following the creation of the pivot objects, I went into the pivot object, and looked at the column numbers where gender and pnmbr were located and specified their column numbers. Following this, I created the pns dataframe which included both gender_pivot, age_pivot, and education_pivot. 

<img width="379" alt="Screen Shot 2020-10-16 at 12 44 11 PM" src="https://user-images.githubusercontent.com/60228365/96366772-e17e4180-1117-11eb-852b-73e39ad01b5f.png">

The plot above represents average household density based on population density.  

<img width="385" alt="Screen Shot 2020-10-16 at 12 36 20 PM" src="https://user-images.githubusercontent.com/60228365/96366779-e511c880-1117-11eb-883a-9ee1cb148c0b.png">

The plot above represents average household density based on population density from the ADM1 data. This plot was created by sampling from the adm1 data. 

<img width="381" alt="Screen Shot 2020-10-16 at 12 40 21 PM" src="https://user-images.githubusercontent.com/60228365/96366784-e80cb900-1117-11eb-97d2-5b9ee241b088.png">

This last plot is an image of a cropped and masked Lira, with the synthetic households distrubuted among the district. The points are slightly large, making the graph look very dense. 

<img width="340" alt="Screen Shot 2020-10-16 at 8 27 47 PM" src="https://user-images.githubusercontent.com/60228365/96366787-ec38d680-1117-11eb-9fda-56bf5931f925.png">

Above, I have inserted a screenshot of the confusion matrix received. 

<img width="329" alt="Screen Shot 2020-10-16 at 8 28 09 PM" src="https://user-images.githubusercontent.com/60228365/96366788-ee029a00-1117-11eb-9c47-c4509f405214.png">

Lastly, I have also inserted a screenshot of my final accuracy (approximatley 17.31).

Heat Map

<img width="543" alt="Screen Shot 2020-10-25 at 6 42 54 PM" src="https://user-images.githubusercontent.com/60228365/97122353-9f4a9680-16fb-11eb-9923-15a552aa23b6.png">

The heat map above is a scaled, normalized, and percentized version of the data. 

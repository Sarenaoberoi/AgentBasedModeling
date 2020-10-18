I was originally working with the country Paraguay, but after beginning project 2, I realized that there was a great deal of important data missing from the DHS data. The plot below shows the distribution of households in Altos, Paraguay. I switched my country to Uganda, as the data was much more recent, and I had more data to work with.


<img width="356" alt="Screen Shot 2020-10-01 at 1 24 16 PM" src="https://user-images.githubusercontent.com/60228365/94925354-112d1880-048d-11eb-841f-fbb742667092.png">

Below, I have placed the specific column name for some of the important variables from the data. 

hv005 : sample weights

hv009 : number of household members 

hv105_01- 27 : Age
  
hv104_01 - 21 : Sex of household members 

I began the project by bringing in some new important libraries, including VIM and haven. After brining in the libraries, I read in the 3 seperate subdivision (adm0, adm1, and adm2). These were also used in proeject 1. I also read in the raster tif file which included population. After recieving data from DHS for Uganda, I was able to download the files and bring in persons and household data as well. We defined 9 different variables by referncing their speciic columns from the households data frame. These variables were unit, weights, location, size, sex, age, education, wealth, and hhid. Finally, after defining the variables, we created a new data frame using cbind, to bring all the variables into one dataframe. I then filtered my population data into just 1 specific adm1, Lira. I then cropped the masked the population file to Lira (located in Northern Uganda). 

One important portion of this project was to pivot our gender, age, and education variables. I was able to pivot these variables by looking into the hhs dataframe and findinng the specific column numbers that the variable in interest was located in. 

<img width="379" alt="Screen Shot 2020-10-16 at 12 44 11 PM" src="https://user-images.githubusercontent.com/60228365/96366772-e17e4180-1117-11eb-852b-73e39ad01b5f.png">


<img width="385" alt="Screen Shot 2020-10-16 at 12 36 20 PM" src="https://user-images.githubusercontent.com/60228365/96366779-e511c880-1117-11eb-883a-9ee1cb148c0b.png">


<img width="381" alt="Screen Shot 2020-10-16 at 12 40 21 PM" src="https://user-images.githubusercontent.com/60228365/96366784-e80cb900-1117-11eb-97d2-5b9ee241b088.png">


<img width="340" alt="Screen Shot 2020-10-16 at 8 27 47 PM" src="https://user-images.githubusercontent.com/60228365/96366787-ec38d680-1117-11eb-9fda-56bf5931f925.png">


<img width="329" alt="Screen Shot 2020-10-16 at 8 28 09 PM" src="https://user-images.githubusercontent.com/60228365/96366788-ee029a00-1117-11eb-9c47-c4509f405214.png">

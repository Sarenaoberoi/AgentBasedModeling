# Welcome to Sarena's Project 1 Deliverable!

## My Geometric Bar Plot with Paraguay!

I began this project by investigating the population distribution of Paraguay. Paraguay is a country located in South America, bordered by Bolivia, Brazil, and Argentina. Paraguay's total population is slightly below 7 million people. I chose to plot the population distribution in the adm1 of Paraguay. Paraguay's adm1 is made up of 17 departments. A few of these departments include San Pedro, Misiones, and Central. As you can see from the plot below, the population is spread out relatively evenly among the 17 different departments. Asunción, the capital of Paraguay, has the highest population out of the country. This is evident by looking at the goemetric bar plot to the right of the map. Central has the higest population, making up approximatley 31.04% of the country's entire population. Following central, we have Alto Paranà and Itapúa with the next highest populations.    

<img width="1280" alt="Screen Shot 2020-09-10 at 12 36 16 PM" src="https://user-images.githubusercontent.com/60228365/92764337-56649b80-f362-11ea-88ce-3fdb1b7f1392.png">

I had picked a number of countries before settling down on Paraguay. Many of the other countries I had chosen were difficult to work with, either because they were too small, didn't have enough data, or didn't have enough subdivisions. I think that Paraguay is a very interesting country with many fascinating cultural traditions. A couple interesting facts about Paraguay:

- Paraguay has higher literacy rates than the United States

- Guarani is the most commonly spoken language

- Iguazu Falls is a large area made up of over 275 waterfalls, making it the largest waterfall in the word

The majority of the population resides in the eastern area of the country.

#### Paraguay - ADM2 - Altos

### Altos!

<img width="468" alt="Screen Shot 2020-09-07 at 8 44 37 PM" src="https://user-images.githubusercontent.com/60228365/92764645-99267380-f362-11ea-9287-fbb47def4f83.png"> <img width="342" alt="Screen Shot 2020-09-07 at 8 45 10 PM" src="https://user-images.githubusercontent.com/60228365/92764660-9b88cd80-f362-11ea-8f03-7236db25f556.png">

<img width="591" alt="Screen Shot 2020-09-07 at 8 46 41 PM" src="https://user-images.githubusercontent.com/60228365/92764672-9deb2780-f362-11ea-8c73-0ce5042b854b.png"> <img width="497" alt="Screen Shot 2020-09-07 at 8 57 06 PM" src="https://user-images.githubusercontent.com/60228365/92764684-a17eae80-f362-11ea-995f-5813aea57bc7.png"> 

<img width="498" alt="Screen Shot 2020-09-08 at 5 39 19 PM" src="https://user-images.githubusercontent.com/60228365/92764700-a3e10880-f362-11ea-9042-ae04c1dc26f4.png">

I decided to choose Altos, a district located in the Cordillera Department of Paraguay. Altos has a population of approximatley 14,000 individuals. By looking at the plots above, it is evident that there are 2 large population density hubs in Altos, located on the east and west side of the city. The majority of the city has an evenly spread population density, with the two towns having drastically larger population densities than the rest of the city. I was able to plot the population points using this command: saolaz_pipo <- rpoint(pop, f = as.im(saolaz_pop19), wind = wind)

The rpoint command works by plotting the points randomly. Each dot on the plot represents an individual living in Altos. 

In order to plot the density, I had to use bandwidth to find my sigma value. After running bandwidth, I got a sigma value of 0.00251. After plotting the density, I moved on to contour lines and polygons. The contour lines worked to surround the highly density areas in Altos. This was done by creating the objects:

Dsg <- as(saolaz_density, "SpatialGridDataFrame")  # convert to spatial grid class
Dim <- as.image.SpatialGridDataFrame(Dsg)  # convert again to an image
Dcl <- contourLines(Dim, levels = 1000000)  # create contour object
SLDF <- ContourLines2SLDF(Dcl, CRS("+proj=longlat +datum=WGS84 +no_defs"))
SLDFs <- st_as_sf(SLDF, sf)

For the levels argument, I made sure to take a look at my density plot that I created before to see what the average densities surrounding the area was. I finally was able to choose a levels of 1000000. After creating the contour lines, I converted the countour lines to polygons. This was done by using this snippet of code:

inside_polys <- st_polygonize(SLDFs)
outside_lines <- st_difference(SLDFs, inside_polys)
outside_buffers <- st_buffer(outside_lines, 0.001)
outside_intersects <- st_difference(saolaz, outside_buffers)
oi_polys <- st_cast(outside_intersects, "POLYGON")
in_polys <- st_collection_extract(inside_polys, "POLYGON")
in_polys[ ,1] <- NULL
oi_polys[ ,1:15] <- NULL


all_polys <- st_union(in_polys, oi_polys)
all_polys <- st_collection_extract(all_polys, "POLYGON")
all_polys <- st_cast(all_polys, "POLYGON")
all_polys_saolaz <- all_polys %>%
  unique()
  
When creating the final plot, it was very important to filter out some of the extraneous values. For example, there were many values that had extremley high densities because the area itself was extremley small. For example, even if there were only 2 or 3 people within an area, if the area itself was small, the densities would show up very high. I was able to filter some of these areas out and focus on more realistic density values and areas.  


## Accessiblity 2- Roads and Pharmacies!

In this plot, I specified roadways (unpaved, unhewn_cobblestone, and asphalt) in Altos, Paraguay. Following this, I specified the healthcare facilities in Altos, Paraguay. Since Altos is a small district in Paraguay, it did not have many healthcare facilities (4 pharmacies).


### Roadways in Altos, Paraguay:


<img width="824" alt="Screen Shot 2020-09-14 at 1 33 39 PM" src="https://user-images.githubusercontent.com/60228365/93118907-f9812200-f68e-11ea-8bbf-110776393580.png">

The skyblue colored lined represent unpaved roads, the black lines represent unhewn-cobblestone roads, and the chartreuse colored lines represent asphalt roads. 


### Pharmacies in Altos, Paraguay:

<img width="821" alt="Screen Shot 2020-09-14 at 1 32 33 PM" src="https://user-images.githubusercontent.com/60228365/93118916-fdad3f80-f68e-11ea-84a0-9c34f0c44e21.png">

The pharmacies are represented by the red dots scattered across the plot. 


### Densities of Urban Areas with Roadways and Pharmacies!

<img width="860" alt="Screen Shot 2020-09-14 at 1 31 14 PM" src="https://user-images.githubusercontent.com/60228365/93118928-00a83000-f68f-11ea-85ce-eb2a89b22891.png">


In the plot above, we see a the roads and pharmacies (represented by the same colors mentioned before), along with population densities. The yellow color represents low population densities, while the orchid (purple) color represents high population densities. This plot is a very good representation of how individuals are able to get to health care facilities using road networks. Looking at the plot, we can also see that the pharmacies are more commonly located in areas with high population densities. 

### Stretch Goal!

<img width="280" alt="Screen Shot 2020-09-14 at 11 41 39 AM" src="https://user-images.githubusercontent.com/60228365/93117316-a8702e80-f68c-11ea-83ad-f056159909f9.png">

<img width="473" alt="Screen Shot 2020-09-15 at 3 28 04 PM" src="https://user-images.githubusercontent.com/60228365/93255794-66b4b600-f768-11ea-9d76-4dab9b927726.png">


This stretch goal was a very fun exercise. It was interesting to see my area in a 3-dimensional plot. Looking at the graph below, we also see that 



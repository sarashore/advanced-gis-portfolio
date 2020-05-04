# advanced-gis-portfolio
This my portfolio for 90753 - Advanced GIS!

# About Me
I'm a second-year MSPPM interested in education and housing policy. Before Heinz, I worked as an 11th Grade English Teacher and then at an education non-profit focused on improving access to higher education and guidance on the application and financial counseling. Since being at CMU, I've worked at Allegheny County DHS, Mullin & Lonergan, and now the URA. When I grow up, I'd like to work for a state department of education to create policies surrounding the intersection of food, housing, and education for students in K-12. In another life, I would have liked to have been a geologist studying volcanic eruptions. Outside of school, I enjoy gardening, rock climbing, relearning Spanish, and snuggling with my newish puppy. 

# What I Hope to Learn
GIS has been my favorite skill that I've learned at Heinz so far. In the last few months, I've used GIS to map housing needs for counties accross the country to submit to HUD; industrial hemp processing site locations in Fayette County, PA; and to create a cluster analysis for risk assessment of all 6-12 schools in the Pittsburgh School District. One thing I still hope to learn in this class is how to make client dashboards. Additionally, I'd like to become more comfortable with GitHub. I only learned about the resource on the first day of this class and now I'm seeing and hearing about it EVERYWHERE!

# Portfolio

## Custom Google Map Style 
My inspiration for this assignment comes from a photo I took in my apartment last spring. It was the first sunny day in Pittsburgh for a while and I really liked the way the light was coming through the big windows. I'm hoping for some more sunny days (literally and metaphorically) soon!

<img width="1129" alt="Image 1" src="https://user-images.githubusercontent.com/62624539/80929316-e1ac9f80-8d78-11ea-9757-96f8aa9706e8.png">

Using this color scheme, I created a map style in Google Maps. The land uses the Dim Gray, the labels are Beige, roads are Sienna, and parks and water are Dark Sea Green. I didn't use the Dark Olive Green; however, I likely could have used it for some type of major feature or as a label for major urban areas. I probably shouldn't have used the green for both parks and water, as neither stands out and it's challenging to differentiate between the two of them. In the future, I would likely include some duller blue to serve as the water feature color.  I played with the hue just a bit in this version to create a slight differentiation between water and parks.  Additionally, with more colors to choose from, I would have differentiated roads from one another.

<img width="1048" alt="Image 2" src="https://user-images.githubusercontent.com/62624539/80929373-744d3e80-8d79-11ea-859e-01579f74d0ec.png">

I like this more neutral color scheme but I think it could use a few more tweaks so as to highlight any relevant points of interest. 

## Create a Custom ArcGIS style

### Identify your source for inspiration and styles used 

Recently, I took an Indian cooking class at Chatam’s Eden Hall campus (I would definitely recommend)! I remember thinking how beautiful all the spices looked – particularly, the turmeric. Though my hands were too busy to take any photos, I found this on Adobe Stock that reminded me of that feeling. I tried to make all landmasses this strong turmeric color and the ocean red like chili powder as the main features in my style.


In the cooking class, the teacher mentioned that she usually carries a map with her to highlight the areas of India that the recipes come from and she'd like for this to be a feature on her new website. Unbeknownst to me, many of the recipes that American’s consider to be “Indian” are specific to the Northern regions. One (potential) use for a map like this may be to illustrate which regions, or specific households, that these recipes come from. 


To check whether the implementation of my style was acceptable, I looked at two map scales: 1:192,176,068 (A Global Scale) and 1:40,302,243 (India). I used the color pencil style on ArcGIS as my base style, and I think in a large-scale view of this map, the colored pencil style could become distracting. Since one theory of applicability would be for Jalsa to use this on her website, I wanted to be sure that she could toggle across the country or world readily and with few changes to the map style or key features. Depending on her views on Indian culinary politics, one aspect to further consider in QA may be intracountry boundaries (note: I have none at this time). Additionally, certain areas of the ocean have a blue background and I can't get them to change without changing the style of the ocean scribbles. 

![Image 4](https://user-images.githubusercontent.com/62624539/80929517-9eebc700-8d7a-11ea-9791-0bb4511e7bf3.jpg)

![Image 4](https://user-images.githubusercontent.com/62624539/80929532-c17de000-8d7a-11ea-9f40-421c940fecdc.jpg)

## Build an on-line map in MapBox

[Here](https://api.mapbox.com/styles/v1/sarashore/ck8osttha3xh91jo0t24uzh28.html?fresh=true&title=view&access_token=pk.eyJ1Ijoic2FyYXNob3JlIiwiYSI6ImNrODdybmFocjAwNWszbW8wN3Rkd3Z0ZmEifQ.rZZabkC6DJxP9Al3uddAcQ#3.04/37.67/-96.29.) is my published map showing the number of opioid overdoses by state. [Note: I did not consider the rate of overdoses.]

Overall, I had a fine experience working with Mapbox. To echo Ian's point from class, I wish that we might have done the entirety of the work outside of ArcGIS; however, I still think this was a valuable experience. I have limited experience in webscraping, so I was appreciative that you provided an excel sheet with the relevant CDC data. I had no trouble joining the data in GIS. I was able to use my minimal knowledge of Python to create a new column in the County feature class to mimic the FIPS code of the Prescription Overdose table and make for easy joining. I was unable to convert the "Null" values to "1000" - I'd love some tips on this as my internet sleuthing was unproductive.

I transported the data to Mapbox via compressed shapefiles and had no trouble doing so. Once in Mapbox, I struggled a bit; however, I'm certain most of this is simply due to my lack of familiarity with the program. In Mapbox, I struggle to make small edits, like turning on and off labels, even after completing their tutorials; however, again, I may grow more comfortable with increased use. Due to the fact that this fine tuning of the presentation of the map took me so long, I wasn't able to get to the second, county-level data.

I think, at this time, I much prefer ArcGIS Pro; however, I absolutely see the merit in building our familiarity with free tools. After class today, I'm interested to learn more about QGIS, as this is what my future employer uses for most of their products.

## Mapping Geographic Footprints

### 412 Food Rescue Data
I really like using Keplar/Mapbox when the data is provided in a JSON or CSV already. This tool is incredibly simple and I appreciate the variety of spatial analysis options you're with which you're offered to display your data. In my illustration of the 412 food rescue data, I chose to connect the sources and destinations with arcs and to tilt the map slightly in 3D space so as to show the arcs clearer. Additionally, I colored the arcs in a way that might make it simpler to tell where food was coming and going.

Important to note, I did not symbolize all of 412's 3 years of data and only looked at data from 2019.

<img width="955" alt="Image 5" src="https://user-images.githubusercontent.com/62624539/80930487-eb86d080-8d81-11ea-987a-a8e5d8800aee.PNG">


### Investigate Sample Dataset
Although my phone has been tracking my location for years, Google has not. This was so disappointing, as I was really hoping to check out my quarantine activity (or lack thereof). I have since turned on my Google location tracking and will be interested to follow up with myself in a week or so. This meant that I had to utilize the provided sample data. I wasn't able to get it to work in Python; however, I've never used that tool before, so it's likely I made dumb errors. 

Additionally, the kernal density feature in Pro was only putting out results for a tiny section of the map (see below). I experimented with changing the output cell size; however, it wasn't effective. 

<img width="473" alt="Image 6" src="https://user-images.githubusercontent.com/62624539/80930491-f04b8480-8d81-11ea-9cc1-320ad679f104.PNG">

Ultimately, I ended up using Keplar again to represent this information. It was very easy to pull out personal information from this dataset. I found this heatmap to be useful to understand general patterns (using the time-stamped lat/long). However, I used the cluster analysis tool to determine the exact street corner at which the sample person lived. 

<img width="949" alt="Image 7" src="https://user-images.githubusercontent.com/62624539/80930498-f6416580-8d81-11ea-9410-9f481c73ff53.PNG">

<img width="958" alt="Image 8" src="https://user-images.githubusercontent.com/62624539/80930501-f9d4ec80-8d81-11ea-92df-6f75d1e9b1d1.PNG">

Although I recognize that this data collection is invasive and makes us substantially more vulnerable, I see the merit of collecting this data for policy creation - when given to the appropriate folks and regulated in an appropriate way, of course. Location data has the potential to be used to develop more socially equitable policies (i.e., understanding how far people have to travel for food & work). Personally, I'm alright with my data being collected; however, I know this means that it's inevitably going to be used for advertisement and other manipulation. In terms of regulating this data, I think it's extremely important that people are informed of the accompanying risk. Crafting more straightforward software agreements or providing monthly updates to the user of their data being collected may be a way to visualize this risk and ensure people are aware of the extent of their data being collected and how it may be used. 

## Hazardous Emergency Decisions

##3 Redirected Traffic/Drive Times 

Below is a map of the redirected traffic patterns in lieu of this spill of chlorine gas. Three routes (1,3 and 4) are mapped in full and two routes (2 and 5) have stops plotted but are not routed. In this map, I’ve mapped the drive times for fire stations at 2 and 4 minutes. At first glance, it seems as though few trucks or emergency response teams would make it to the scene of the incident within 4 minutes. It is likely that Fire Station #18 is best-positioned to handle an incident at this location.

![Image 9](https://user-images.githubusercontent.com/62624539/80930659-f9892100-8d82-11ea-843a-d150d4c84b8e.jpg)

### Hospital Drive Times
Below is a map of the redirected traffic patterns in lieu of this spill of chlorine gas. Three routes (1,3 and 4) are mapped in full and two routes (2 and 5) have stops plotted but are not routed. In this map, I’ve mapped the drive times for hospitals at 5, 10, and 15 minutes. Since the hospitals are not close to the incident, I wanted to be sure to use intervals that would provide an appropriate understand of how long it might take an effected person at the site of the incident to get to any hospital. At first glance, it seems as though ambulance or EMT teams would make it from the scene of the incident to a hospital in less than 15 minutes. For this scenario, I’ve chosen only hospitals within 7 miles to examine. 

![Image 10](https://user-images.githubusercontent.com/62624539/80930660-fb52e480-8d82-11ea-82d0-574a10007163.jpg)

## Hurricane Damage Decisions
<img width="555" alt="Image 11" src="https://user-images.githubusercontent.com/62624539/80930806-ddd24a80-8d83-11ea-8590-18424e33e49d.PNG">


<img width="550" alt="Image 12" src="https://user-images.githubusercontent.com/62624539/80930809-df037780-8d83-11ea-8129-91a5abc77c14.PNG">


<img width="554" alt="Image 13" src="https://user-images.githubusercontent.com/62624539/80930812-e296fe80-8d83-11ea-8349-3a2defc1e4b3.PNG">

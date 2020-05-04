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

### Build an on-line map in MapBox

[Here] (https://api.mapbox.com/styles/v1/sarashore/ck8osttha3xh91jo0t24uzh28.html?fresh=true&title=view&access_token=pk.eyJ1Ijoic2FyYXNob3JlIiwiYSI6ImNrODdybmFocjAwNWszbW8wN3Rkd3Z0ZmEifQ.rZZabkC6DJxP9Al3uddAcQ#3.04/37.67/-96.29.) is my published map showing the number of opioid overdoses by state. [Note: I did not consider the rate of overdoses.]

Overall, I had a fine experience working with Mapbox. To echo Ian's point from class, I wish that we might have done the entirety of the work outside of ArcGIS; however, I still think this was a valuable experience. I have limited experience in webscraping, so I was appreciative that you provided an excel sheet with the relevant CDC data. I had no trouble joining the data in GIS. I was able to use my minimal knowledge of Python to create a new column in the County feature class to mimic the FIPS code of the Prescription Overdose table and make for easy joining. I was unable to convert the "Null" values to "1000" - I'd love some tips on this as my internet sleuthing was unproductive.

I transported the data to Mapbox via compressed shapefiles and had no trouble doing so. Once in Mapbox, I struggled a bit; however, I'm certain most of this is simply due to my lack of familiarity with the program. In Mapbox, I struggle to make small edits, like turning on and off labels, even after completing their tutorials; however, again, I may grow more comfortable with increased use. Due to the fact that this fine tuning of the presentation of the map took me so long, I wasn't able to get to the second, county-level data.

I think, at this time, I much prefer ArcGIS Pro; however, I absolutely see the merit in building our familiarity with free tools. After class today, I'm interested to learn more about QGIS, as this is what my future employer uses for most of their products.

# Module6v4

##Module 6 Notes
##Overview
(As captured from Data Bootcamp Module 6) 

In this module, as assigned Data Analyst, I will analysis, visualization, and statistical skills by retrieving and analyzing weather data for a hypothetical travel company, PlanMyTrip. Successfully completing the tasks will draw on your knowledge of Python, decision and repetition statements, data structures, Pandas, and Matplotlib.

By the end of this module, as assigned Data Analyst, I will complete the following::
•	Perform tasks using new Python libraries and modules.

•	Retrieve and use data from an API "get" request to a server.

•	Retrieve and store values from a JSON array.

•	Use try and except blocks to resolve errors.

•	Write Python functions.

•	Create scatter plots using the Matplotlib library, and apply styles and features to a plot.

•	Perform linear regression, and add regression lines to scatter plots.

•	Create maps by using GeoViews and the Geoapify API.


#Purpose

(This module is built around a project that mirrors a real-world scenario that would require data analysis and visualization. In module6 , I will practice your analysis, visualization, and statistical skills by retrieving and analyzing weather data for a hypothetical travel company, PlanMyTrip.)

As a Data Analyst, I am helping Jack, head of analysis for the PLANMYTRIP user interface team. PLANMYTRIP is a top travel technology company that specializes in internet-related services in the hotel and lodging industry. Jack is the head of analysis for the user interface team. He's asked you to help him collect and present data for customers via the search page, which they will then filter based on their preferred travel criteria in order to find their ideal hotel, anywhere in the world.

Jack, the client, has asked I help him collect and present data for customers via the search page, which they will then filter based on their preferred travel criteria in order to find their ideal hotel, anywhere in the world. As part of my analysis, I will need to perform statistical calculations on the data and the weather parameters in the Northern and Southern hemispheres.

Next as assigned  Data Analyst, I will export the data, clean it, and use the weather data to choose the best cities for vacation based on certain weather criteria, and then map these cities using GeoViews and the Geoapify API.

In addition, I will practice my analysis, visualization, and statistical skills by retrieving and analyzing weather data for a hypothetical travel company, PlanMyTrip. Successfully completing the tasks will draw on my knowledge of Python, decision and repetition statements, data structures, Pandas, and Matplotlib.

##Approach 
Basic Project Plan
Here's an outline of your project plan:

•	Task: Collect and analyze weather data across cities worldwide.

•	Purpose: PlanMyTrip will use the data to recommend ideal hotels based on clients' weather preferences.

•	Method: Create a Pandas DataFrame with 500 or more of the world's unique cities and their weather data in real time. This process will entail collecting, analyzing, and visualizing the data.

Analysis of the data will be split into three main parts, or stages.
1.	Collect the Data

2.	Exploratory Analysis with Visualization

3.	Visualize Travel Data

##Results

#Deliverable 1: Retrieve Weather Data
For this deliverable, you'll generate a set of 2,000 random latitudes and longitudes, retrieve the nearest city, and perform an API call with OpenWeatherMap. In addition to the city weather data you gathered in this module, use your API skills to retrieve the current weather description for each city. Then, create a new DataFrame containing the updated weather data.

1.	Create a folder called Weather_Database to save all the files related with this deliverable.
GitHub Location: https://github.com/LouFoster/Weather_Database.git

2.	Save the Weather_Database_starter_code.ipynb starter code to the Weather_Database folder and rename it as Weather_Database.ipynb.

3.	Use the np.random.uniform function to generate a new set of 2,000 random latitudes and 2,000 longitudes.

 ![image](https://user-images.githubusercontent.com/117233641/228460374-d6e4912c-d336-49ea-9572-b0ec64171410.png)


4.	Use the citipy module to get the nearest city for each latitude and longitude combination.

![image](https://user-images.githubusercontent.com/117233641/228460531-3e9a3003-1bd2-45e5-8bd3-ddf1c159a201.png)



5.	Import your OpenWeatherMap's API key and assemble the API call URL as a string variable. Recall to edit the config.py file to add your API key; also, it's critical to avoid publishing your API key on your GitHub repository.
 
![image](https://user-images.githubusercontent.com/117233641/228460614-f0a20f8f-38b6-4fba-ae23-f55662d7020e.png)


6.	Retrieve the following information from the API call:
  o	Latitude and longitude
  o	Maximum temperature
  o	Percent humidity
  o	Percent cloudiness
  o	Wind speed
  o	Weather description (for example, clouds, fog, light rain, clear sky)
 
![image](https://user-images.githubusercontent.com/117233641/228460712-548135df-3436-4a40-babf-28626c594fa4.png)

![image](https://user-images.githubusercontent.com/117233641/228460780-0d7c595f-7c0f-44c4-a466-a9438d22c4f1.png)
 

7.	Add the weather data to a new DataFrame.
  o	Before continue to the next step, take a moment to confirm that the DataFrame looks similar to the image below (note that cities and countries may vary):

![image](https://user-images.githubusercontent.com/117233641/228460852-ecc0a0d1-637d-4dbb-a55b-92494f86262f.png)
 

8.	Export the DataFrame as a CSV file, and save it as WeatherPy_Database.csv in the Weather_Database folder.
 
![image](https://user-images.githubusercontent.com/117233641/228460923-de92b59b-90b3-46f0-9070-dec3594c90fa.png)
 





#Deliverable 2: 
Create a Customer Travel Destinations Map

In this deliverable,I will employ input statements to retrieve customer weather preferences. Next, I will use those preferences to identify potential travel destinations and nearby hotels. Finally, you'll show those destinations on a map.

1.	Create a folder called Vacation_Search to save all the files related with this deliverable.

2.	Download the Vacation_Search_starter_code.ipynb Jupyter notebook,save it into your Vacation_Search folder, and rename it as Vacation_Search.ipynb.

3.	In the Vacation_Search.ipynb file, ensure that the dependencies and the Geoapify API key is imported correctly.

![image](https://user-images.githubusercontent.com/117233641/228462447-ed9aed24-c174-4357-a0fd-f8fcbc44e35a.png)

4.	From the Weather_Database folder you created in the "Deliverable 1," import the WeatherPy_Database.csv file as a Pandas DataFrame named city_data_df.
 
![image](https://user-images.githubusercontent.com/117233641/228462544-cd1e0063-bf99-43fb-adac-9b3f0f95e0f6.png)

5.	Write two input statements that prompt the user to enter their minimum and maximum temperature criteria for their vacation.
 
 ![image](https://user-images.githubusercontent.com/117233641/228462599-1d1915a1-4267-42c7-9167-bdcc75181794.png)

6.	Create a new Pandas DataFrame by using the loc Pandas method to filter the city_data_df DataFrame for temperature criteria collected. Name the DataFrame as preferred_cities_df.

 ![image](https://user-images.githubusercontent.com/117233641/228462656-eae4d06e-2db4-4f4f-a4ec-3a53fcc5e035.png)


7.	Create a new Pandas DataFrame named clean_travel_cities by using the Pandas dropna function on the preferred_cities_df to drop any empty rows.
 
 ![image](https://user-images.githubusercontent.com/117233641/228462714-b7263e53-4259-499c-b048-504833dbd846.png)


8.	Use the copy Pandas function to create a new DataFrame, called hotel_df, by copying the following columns from the clean_travel_cities DataFrame: "City", "Country", "Max Temp", "Current Description", "Lat", "Lng".

 ![image](https://user-images.githubusercontent.com/117233641/228462786-695c1337-e43b-42e2-bede-2a0f6414d98b.png)


9.	Add a new empty column named Hotel Name to the hotel_df DataFrame.

![image](https://user-images.githubusercontent.com/117233641/228462850-5e0e3b3c-c943-49a9-8001-1376032f07c3.png)

10.	Review the hotel search parameters provided. These parameters are the same we used in this module; you'll use them to search for a hotel for each city.

![image](https://user-images.githubusercontent.com/117233641/228462908-8fce14a6-4ebb-4d29-9be6-c30232166933.png)

11.	Use a for loop to iterate through the hotel_df DataFrame. Retrieve the latitude and longitude of each city and use the Geoapify API to find the nearest hotel based on the search parameters provided, then add the hotel name to the hotel_df DataFrame. If a hotel isn't found, set the hotel name as "No hotel found".

![image](https://user-images.githubusercontent.com/117233641/228462975-da9efed4-06a3-4cd8-b902-5442e4f1a245.png)
 

12.	Drop any rows in the hotel_df DataFrame where a hotel name is not found and store the resulting data into a new DataFrame named clean_hotel_df.
   o	Take a moment to confirm that your clean_hotel_df DataFrame looks similar to the image below (note that the data may vary).

![image](https://user-images.githubusercontent.com/117233641/228463028-485fb854-6a0a-4abc-8498-682388e23ac4.png)

 13.	Create an CSV file to store the clean_hotel_df DataFrame as WeatherPy_vacation.csv in the Vacation_Search folder.
 
 ![image](https://user-images.githubusercontent.com/117233641/228463109-6cb10b44-7f0e-4ad3-961d-08c150ac0488.png)


14.	Use GeoViews to create a map that displays a point for every city in the clean_hotel_df DataFrame. In the point for each city add:
  o	The city name
  o	The country code
  o	The weather description
  o	The point's size should be the maximum temperature for the city

![image](https://user-images.githubusercontent.com/117233641/228463232-701fc81a-8656-4d90-811b-264eaf12927f.png)
 
15.	Take a screenshot of your map and save it to the Vacation_Search folder as WeatherPy_vacation_map.png.
  o	The map should look similar to the following image:

 ![image](https://user-images.githubusercontent.com/117233641/228463305-bd9d542c-0d0b-4fc3-a951-acedc4ac8567.png)




##Deliverable 3: Create a Travel Itinerary Map

For this deliverable, you'll use the Geoapify Routing API to create a travel itinerary that shows the route between four cities chosen from the customer’s possible travel destinations. Then, you'll create a map with a pop-up marker for each city on the itinerary.


1.	Create a folder called Vacation_Itinerary to store all the files for this deliverable.

2.	Download the Vacation_Itinerary_starter_code.ipynb file into your Vacation_Itinerary folder and rename it Vacation_Itinerary.ipynb.

3.	Make sure the initial dependencies and the Geoapify API key are imported.

 ![image](https://user-images.githubusercontent.com/117233641/228463393-9e1a8bf5-5cd9-4aa6-9147-561ea58f21e4.png)


4.	From your Vacation_Search folder from Deliverable 2, import the WeatherPy_vacation.csv file as a DataFrame named vacation_df.

 ![image](https://user-images.githubusercontent.com/117233641/228463424-b2b3e507-d824-4498-a27a-a89a1a1c47f3.png)

5.	Use GeoViews to create a map that shows all the cities in the vacation_df DataFrame. Configure the map as follows:
   o	The point's size should be the maximum temperature for the city
   o	The point's color should be the city's name
   o	Use the hover_cols parameter to the the "Hotel Name", "Country", and "Current Description" columns to each point as additional information.

 ![image](https://user-images.githubusercontent.com/117233641/228463594-565223c7-df27-4b4a-bf99-ba903093600b.png)


6.	From the map, choose four cities that a customer might want to visit. They should be close together and in the same country. Use the loc method to create separate DataFrames for each city on the travel route.

 ![image](https://user-images.githubusercontent.com/117233641/228463641-bc751295-93fb-4936-a133-44bd530f145a.png)


HINT
7.	Use the Pandas concat function to merge the DataFrame from each city in the itinerary to create a new DataFrame named itinerary_df to store the itinerary details. Your final DataFrame should look as in the image below.

![image](https://user-images.githubusercontent.com/117233641/228463708-a8bc81f3-a446-40dc-adaf-0398f353ee37.png)
 
![image](https://user-images.githubusercontent.com/117233641/228463776-2c64cbc3-7c1d-4536-b50a-a6e5ef73912e.png)

8.	Use the Pandas copy function to create a new DataFrame named waypoints_df to store the longitude and latitude for each city in itinerary_df.

![image](https://user-images.githubusercontent.com/117233641/228463855-ad3b7cde-e630-4a34-9df5-ed834d225692.png)
 

9.	Use GeoViews to create a map that shows the four cities in the itinerary. You may end with a map similar to the image below.

![image](https://user-images.githubusercontent.com/117233641/228463918-bdcba7b0-fa95-41b5-a5bb-0b93e3efd1bc.png)

10.	Next, you'll use the Geoapify Routing API to find a route between the cities in the itinerary. Review the code that sets the initial parameters and fetches the coordinates from each city to define the waypoints parameter by using a for loop.

![image](https://user-images.githubusercontent.com/117233641/228463981-95eea187-0e46-4dd7-b265-25ed547fd376.png)

11.	Use the Geoapify Routing API to retrieve the route's directions for your itinerary.

![image](https://user-images.githubusercontent.com/117233641/228464091-ca72273c-21e0-4524-b63b-155f04e1227f.png)

12.	From the JSON response, store the route's legs coordinates in a variable called legs.
 
![image](https://user-images.githubusercontent.com/117233641/228464205-bd460488-37a1-4382-a493-9ded1493fd48.png)
 
 
13.	Loop through the route legs coordinates to fetch the latitude and longitude for each step. Store the latitude and longitude values into two Python lists named longitude and latitude.
14.	Use the longitude and latitude Python lists to create a new DataFrame named route_df.

![image](https://user-images.githubusercontent.com/117233641/228464269-879d0f67-f8e0-44fa-aa5c-79ef38c8677a.png)

 
15.	Use the GeoViews Path function to configure a line plot by using route_df. Set a custom color and width for the line that may contrast with the map.
16.	Use the asterisk operator to display a composed plot that shows the itinerary's route over the map containing the cities. Your map may look as in the following image.





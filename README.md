
Hi everyone my name is kapil kukreja I am student of almabetter my topic for EDA project is AIrbnb booking analysis.

Project Summary -

Airbnb is an American San Francisco-based company operating an online marketplace for short-term home stays and experiences. Guests and hosts have used Airbnb to expand on travelling possibilities and present a more unique, personalized way of experiencing the world. Today, Airbnb became one of a kind service that is used and recognized by the whole world. Data analysis on millions of listings provided through Airbnb is a crucial factor for the company. These millions of listings generate a lot of data - data that can be analyzed and used for security, business decisions, understanding of customers' and providers' (hosts) behavior and performance on the platform, guiding marketing initiatives, implementation of innovative additional services and much more.

In this project I do analysis on 2019 website data regarding listing on website, user reviews, compare prices, analysis host data. I analysis data and provide different visualization charts, different business insights using python language. I use numpy library for creating data array that helps to analysis such big data. We also use panda library which offers data structures and operations for manipulating numerical tables and time series.

These are the Points which I will discussion in this project video.

First one is data summery we have data from airbnb in csv file which belongs to newyork city and our data is in tabular form 

Then we will talk about Problem statement where we will discuss about problems we found in data to solve

And then I work on data for making it analysis ready like finding missing or null values and duplicate value correction. Then we will start analyzing data on various criteria like

Top 10 hosts according to their listing count: - where host is person who is listing their building.

 Finding ratio of each Room Type:-  there are three type of rooms and we will find ratio rooms type  

 Active host as per location:- in this we will calculate active host according to location like grouping of host as per room location

Average price of listing according to the location and Room Type:- in this we analyze average price according to two criteria location and room type

Highest and lowest rent according to location:- in this we find highest and lowest room rent of different locations

And then we will find conclusion in this project

Data Summery

We have total 16 variables/columns and 48896 rows or listings in our data. Now let’s talk about columns description. First column is:-

Unique id: This contains unique non repeating numerical id of listing.

Name of listing: This contains name of Home/Apartment.

Unique host id: This contains unique numerical id of host who is listing their home.

Name of host: This contains name of host.

Nabourhood location: This contains location of Room in New York City.

Neighbourhood area: This contains nearby famous location of Room.

Latitude: This contains geographical locations of Room on map.

Longitude: This also contains geographical locations of Room on map. Both latitude and longitude have float data type. When we search both on Google map we get actual location of building.

Type of room: This contains type of room for example Entire home, private room or shared room.

Price of listing: This contains price of room in dollars.

Minimum nights: This contains minimum days for which booking is accepted.

Number of reviews: This contains count of reviews per Home/ Apartment given by consumers. 

Date of last review: This contains date of last review of Home/ Apartment. 

Number of reviews: This contains count of customer’s reviews/checks per month.

Host listing count: This contains maximum listing count by a host.

Availability of rooms in 365 days: This contains maximum availability of room in days among one year. For example some rooms are available occasionally or seasonally 

Problem Statement

Next we have problem statement in this we rectify problems in data and show them using data visualization and solve them.

 Data analysis on thousands of listings provided through Airbnb is a crucial factor for the company where data can have null or missing values.

 In data price of some listing is zero which is not possible by removing or revising rates of those listing data became analysis ready.

 Our main objective is to find out the key metrics that influence the listing of properties on the platform. For this, we will explore and visualize the dataset of Airbnb in New York City using basic exploratory data analysis (EDA) techniques. 

 We will be finding out the distribution of every Airbnb listing based on their location, including their price range, room type, availability, and other related factors.

Our first visualization chart is about finding missing or null values: - on x-axis we have column names and on y axis we have count of missing values. In this we check null values in all 16 columns and found for columns have missing values. To find that we create entire data to panda’s data frame and use count function to count total values which are not null and store that count in new data frame. As we know our data has 48896 rows so we use Len function in data frame and less not null values count from complete rows count and we get updated data frame with null values count. Now I visualize this missing value data frame using bar plot chart. For visualization I import matplotlib library. As we can see in chart there are 16 properties whose names are missing in data. 21 properties don’t have host name.10052 properties does not having any reviews.

I also find unique values for each column using unique function on dataframe for this I also use for loop to store unique values in dataframe.

There I also find one error that there are 11 listings whose price is zero to remove that listings we first create one dataframe and store data whose price is zero then we use drop  method to remove zero pricing listings

To update host name in 21 properties whose host name is missing we check unique host id of that particular host and update host name from listing having same host id. To update name of property we can provide missing name host list to host for updating listing name. For getting reviews we can gave rewards points to customers that can redeem on next booking or online shopping.

Our second visualization is about finding top 10 host having maximum listings: - on x-axis we have host id and on y-axis we have count of listing from 0 to 350. In this we can see data of top 10 highest listing hosts. The host is on top having 327 listing of buildings and other hosts have 232,121,103 and so on.

For creating this visualization we first create one dataframe named Max_host_id then we use value count method and head method on host id column of our main dataframe airbnb_df. Now we provide indexing and column name to our new dataframe so that we can create chart with this dataframe. We import seaborn library for creating this barplot chart where every host represents with different color.

This chart can be use for various purpose like finding host that gave maximum profit to company. 

Giving rewards or other benefits to maximum listing hosts.

Categorizing host for solving problems they are facing while listing, pricing, creating listing page. 

Next we have room type count chart: - Airbnb offers a variety of room types for travelers to choose from. Here are some of the most common room types:

Entire home/apartment: This is a private accommodation that includes the entire space with all amenities. Entire room is having maximum listing on website that is 51.97%.

Private room: This has a private bedroom within a shared home or apartment. Guests will typically have access to shared spaces like the living room, kitchen, and bathroom. Private rooms have 45.66% listings on website.

Shared room: This is a bedroom that is shared with other guests. Guests will typically have a shared bathroom and access to shared spaces like the living room and kitchen. Shared rooms have very small ratio 2.37% of listing on website.

 Luxury, privacy and good services are first priority of customers visit online website for vacation. People also come from other countries to visit New York City for honeymoon and they prefer private rooms and people come with family prefer entire home or apartment. 

To create this chart we first create a python dictionary and use value counts method on room type column to store data in dictionary. Now create two python list and we separate both room type and count from dictionary and store in that python list.

Now we create pie chart using these list data and matplotlib library functions.

Now next we have active host count per location chart: - In this chart x axis shows neighborhoods group and y axis shows number of host. New York City is divided into five neighborhoods group locations Bronx, Brooklyn, Manhattan, Queens and Staten island.	From this visualization chart we can say that Manhattan have maximum host or we can say maximum 21660 listings and Brooklyn is on second number with 20095 listing. Queens is on third number and then Bronx and Staten Island came.

For creating this chart we take one dataframe and store count of host id using groupby function on neighborhoods group column from main dataframe. With help of this chart we know that Bronx and Staten island have less listings so company have to work in this area to grow business.

Next we talk about Average price chart of property according to Location: -  on x-axis we have neighborhood group and room type and on y-axis we have average price from 0 to 250 . In this chart we saw average price of all three types of rooms on particular neighborhood group. We find that average price for private room and shared room is almost same or has minimal difference for all five locations. But entire home price have huge difference about double or more in every location. Manhattan have highest average price for all three room types and Bronx have lowest average price.

For creating this chart we create a new dataframe and use groupby function on neighborhood group and room type and also find mean of price column for data received from groupby function and store it in newly created dataframe. Now from help of this dataframe chart is created.

This chart is very useful for average price comparison.

Now we talk about highest and lowest rent for location: - In this chart we visualize maximum and minimum price of different neighborhood groups. Brooklyn, Manhattan and Queens have same maximum price of 10000 dollars and same minimum price of 10 dollars. While Staten island and Bronx have very low maximum price 5000 and 2500 dollars but minimum price for Staten island is 13 dollars which is higher than others minimum price.

This chart shows that minimum price is almost same for all 5 locations except one Staten island.

For creating this chart we create two dataframes one for storing minimum price and second for storing maximum price. We use groupby function on neighborhood group and also use min() and max() methods and sort_values method on main dataframe and store minimum and maximum price in that dataframe.

Now we create third dataframe for merging those two dataframe we use merge function of panda library. With help of this third dataframe chart is being created.

How analysis helpful for stakeholders in airbnb 

 Analysis can be incredibly helpful for stakeholders in Airbnb because it can provide valuable insights into the performance of the business, the behaviour of guests and hosts, and the preferences and trends in the market. Here are a few examples:

Market Trends: Analysis can help stakeholders to stay up-to-date on market trends, such as which locations are most popular, which amenities are most in demand, and what types of properties are performing well. This information can be used to make strategic decisions about where to invest in new properties and how to market existing listing.

Host Performance: Analysis can help hosts to evaluate their own performance by providing insights into how their listings compare to others in the area, how many bookings they receive, and how much they earn. This can help hosts identify areas for improvement and optimize their listings to increase revenue. 

Guest Behaviour: Analysis can help stakeholders understand the behaviour of guests, such as their booking patterns, length of stay, and average spending. This information can help hosts optimize their listings to attract more guests and maximize revenue. 

Conclusion

1.  Host_id reveals that some host have a huge number of property ownership above 300.

2. The Majority of the listings are located in Manhattan and Brooklyn whereas Bronx and Staten Island have a minimum number of shares.

3.  Manhattan is the most expensive neighbourhood_group followed by Brooklyn Staten Island Queens and Bronx.

  4.'Entire home/apt' room type has the highest number of listing of 51.97% and ‘Shared Room’ is the least listed room type at only 2.37% in total.

5. Brooklyn offers nearly the same number of private rooms and entire home whereas Manhattan offers highest number of entire homes followed by private rooms.

6. Listing of shared room is very little and staten islands and Bronx offer very few shared rooms.

7. Brooklyn and Manhattan has the majority share of listings.

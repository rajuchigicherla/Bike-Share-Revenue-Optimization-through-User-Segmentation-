
# Bike-Share Revenue Optimization through User Segmentation

## Project Description

The bike-sharing rental company `UrbanBike` (Imaginary Company) wants to analyze its user data to find the main differences in behavior between their two types of users; the `casual` who pays for each ride and the annual `member` who pays a yearly subscription to the service.

## About Dataset
Since `UrbanBike` is a fictional company, we will be using Motivate's ride-share company data 'Divvy' open source data which is accessed under this open license. The data itself is broken up into many files which contains over `5 Million` records.
We can access the Dataset [Here](https://www.kaggle.com/datasets/muliadea/cylistic-bike-share-202110-to-202209)

 ## Business Task
 For UrbanBike you are working as a data analyst(Imaginary). So,The company desires to improve its revenue by understanding the relationship between 'casual' and 'member' users. The aim is to get a deep understanding of how causal and annual members differ in their users and then use this to target the causal users digitally to migrate over to becoming full-fledged members of the service. I will use historical data to identify these trends.

`What would motivate a casual user to become a member?`

 ## Key Stakeholders:
 
- `Lily Moreno is the director of marketing`. Responsible for the development of campaigns and initiatives to promote the bike-share program.

- `UrbanBike marketing analytics team` A team of data analytics responsible for collecting, analyzing and reporting on data that helps guide UrbanBike's business strategy.

- `UrbanBike Executive Team` A team that will review recommendations from the analytics team and action any good recommendations.

## Data Preparation & Cleaning

Initially used `Excel` to quickly get to understand the data . After that data was loaded into `SQL` to transform and clean the data.I went through each column systematically and wrote notes on what jobs needed to be done in the preparation stage. 

##### The following actions were performed in SQL before analysis:

- Identify bikes that have no beginning or ending to their journey and station names that are `NULL`.
- Allowed e-bikes with no end stations to be counted and titled as docked_bike and class_bike for distinction
- Remove entries of trips that we identified in the preparation stage such as trips that were not completed on an e-bike, or temporary stations.
- Create a `day of the week` and `month` column for data analysis patterns.
- Trim whitespace around column names
- Changed column name `member_casual` to `member_type` for clarity.

## Analysis
To investigate some of the patterns within the data processed data was uploaded into `Tableau`
###### Here are some of my key takeaways from the data
#### Monthly, daily and hourly usage
- The pattern of users for both a member and a casual user is roughly the same for monthly and hourly patterns of use. That tells us both users are roughly affected by the time of day and the seasons the same. Where the difference is in the volume of usage. Members use the bikes much more often than casual members and we can also see two spikes in usage around 7 am and 5 pm. This would indicate that members use it for a commute to work or study. The similarities and differences in the patterns are shown below:

![month](https://user-images.githubusercontent.com/118670053/223502720-d5639588-0d9b-42c8-ba33-f1d8b72755f7.png)
![day](https://user-images.githubusercontent.com/118670053/223503214-8985334b-200b-4f37-bc97-b93240c24080.png)

- Next, I explored the daily usage of the bikes and found a very interesting inversion of usage between the members and the casual riders. The casual riders are using it mainly on the weekend and especially Saturday, whereas the members are using it more on the weekdays and less on the weekend. This is an important distinction as it shows the purpose of the bike usage varies dramatically for both categories of users.

![hour](https://user-images.githubusercontent.com/118670053/223503524-f2db6ee8-4ace-4244-b5ef-28dc2defda6d.png)

## Average trip duration

- After looking at the patterns across hours, months and days I turned my attention toward the duration of the bike rides. This again led to some clear patterns which could be useful. Casual riders use the bikes for a longer sum duration per trip.

![avg-journey](https://user-images.githubusercontent.com/118670053/223504332-56c2dfb4-b4d9-472c-957b-c6f71932ae0c.png)

- However, when we look at the number of rides that are categorized as member or casual, we see that 59% of trips are taken by members. These two observations combine to the conclusion that members use them more often for shorter trips whilst casual users them for longer and less frequent use.

## Where users start and end their journeys
 - Finally, we will turn our attention to where the rides take place and investigate of there is a relationship between where casual users and members get on and off their bikes.
 
 ![map](https://user-images.githubusercontent.com/118670053/223505439-f7f16f83-89d5-4384-963f-cad481c934df.png)

 - As we can see from above, all users are concentrated around the city centre areas of the city (both uptown and downtown) and there is a strong relationship between both types of users in that they use UrbanBike bikes in the same areas. Assumptions can be made here that the bikes are used for commuting around a busy city for members but there must be a good proportion of their casual members that are tourists. This is also evident in the fact that nearly all casual users are getting on or off their bikes at key tourist sites. In addition, as seen above, casual members use their bikes for longer rides which could indicate casual tourist use of the bikes. Further data would need to be collected to test this properly.
 
## Key Findings
- Both users enjoy using the bikes in the summer months
- Members like to use them as a commute to and from work/college
- Weekends are popular for both user types but especially for casual users.
- Weekdays are not popular for casual users
- Casual riders go on longer journeys
- Members use the bikes more often.
- Both users prefer to use the bikes that are stationed around the city hubs and tourist spots.

## Recommendations

My objective was to convert casual riders into members through data analysis. This can be achieved and I will explain how shortly, however one major understanding must be made now to make a more impactful action plan. This clear understanding is that many casual users are tourists.

The data indicates that a large proportion of users are tourists because a. they do not use the bikes in commute times b. casual users predominately use the bikes in the dryer and warmer months c.casual users use them predominately for weekend usage and the weekday usage drastically falls off d. they use the bikes less often but go on longer trips which indicates they are exploring e. their usage is focused around tourist areas.

#### 1. Tourist passes
If this recommendation is accepted based on my evidence above, then it is my recommendation that the marketing team tackles these users in an attempt to capture more revenue. I would recommend a tourist pass for the bikes. Either a daily, weekly, or monthly pass would offer to be cheaper for the user to use than a per-hour rate.

#### 2. Social media campaign
A social media campaign should help non-tourist and tourist casual users alike convert to membership (or pass) by targeting the summer months and focusing the campaign on the bikes' ability to get around the city hubs easily as these are the two zones where all users are predominately used.

#### 3. Discounts available for users in certain stores
If the marketing team could collaborate with local businesses around the areas that most casual users use, we could set up a scheme whereby customers who show their bike membership card, could get discounts on certain goods and services available in those stores. This would promote users and create a more widespread and embedded advertising campaign. Other citizens will see that Cyclistic users are getting favorable rates on certain products and will become curious about how to avail of these savings.

#### 4. Further data analysis
I would love to explore how many of the casual users are tourists and more data would need to be collected to support some of the claims made here. I also feel that the company should lean stronger on the idea that a bike is a more environmentally friendly way of transport and further analysis should be made into how other companies have leveraged this fact into their advertising campaign. Perhaps a collaboration with the local government or environmental NGOs would offer another viable path for the company to develop.

 With the above analysis, I believe that I have provided UrbanBike with an accurate picture of current users and also offered several strong recommendations to grow their business. I also have provided the next steps in our ambition to take this company to the very next level.
 ## Presentation
 
 Finally prepared a ` PowerPoint` Presentation to present our work to the key stakeholders of UrbanBike.

# CitiBike as an Alternative Means of Transportation in Des Moines
***Analysis of bikesharing in New York as a model for Des Moines***
#### by Justin R. Papreck
---

## Overview

A proposal to open a CitiBike branch in Des Moines, Iowa has been suggested based on the success of the company in New York City, New York. The data were analyzed to determine whether this would be a viable venture using Tableau. The Tableau Story can be accessed here: [CitiBike as an Alternative Means of Transportation in Des Moines](https://public.tableau.com/app/profile/justin.papreck/viz/CitibikeChallenge_16612815995440/CitibikeDemoines)


New York and Des Moines have very few things in common. One of them is the largest city in the united states, while the other is the largest city in a state that has less than 50% of the population of New York City alone. While the population of Des Moines is about 33 times smaller than that of New York, there is one commonality that the cities share: they are very, very flat. When considering implementing a bikeshare company, it is important to consider the clientele that will be utilizing the service. If the primary source of users in NYC are tourists, then while New York may be an excellent location, Des Moines may not be the ideal state to pitch this service as it isn't even in the top 20 cities to visit in the United States. However, if the primary users of the bikesharing service are locals who are employed relatively near their workplaces, the service may be an excellent addition to the city of Des Moines. 

  In 2021, Des Moines was the #2 safest place to live in the U.S. (US News and World Report), the #7 beest places to live in the U.S. (US News and World Report), the #11 most affordable city to buy a home (Forbes Advisor), and the #1 best place to live in the midwest for high salaries and low cost of living. This makes for a great opportunity to add a bikesharing service to a growing city, not constrained by terrain or water boundaries, and with the safety factor may even be more encouraging to younger people and female workers who might otherwise see such a means of transportation as a risk.   

---
## Analysis 

Initially, the data were evaluated using pandas in python to look at the data types, where the duration (timeduration) was found to be an integer value, which limits the amount of analysis that could be done with it. A new column was created on the table to add the datetime format of this while maintaining the integer measure. Following the data processing, the remainder of the analysis was performed in Tableau.

### Overall Use and Age Demographics 

The analysis comes from data acquired in August of 2018 from CitiBike. The total number of rides, and total ride time were found to be 2,344,224 rides and 41,030,675 hours respectively. The distribution of the rides by rider type is as shown: 

![Customter_Dist_Pie](https://user-images.githubusercontent.com/33167541/186763918-82bce46a-7217-4621-a1b7-53773ac15c93.png)


As can be seen, 83% of the rides are by subscribers, whereas only 17% are by non-subscribing customers. It is unlikely that tourists would be subscribers, so this is an indicator that the majority of rides is from local users and not tourists. Another measure was the age of the users, which showed that younger users were more likely to have longer ride durations, but the average ride duration for users over the age 25 remains close to 15 minutes. Considering the ages, it is likely that the younger users have to ride farther if they are living in a more affordable area and have to cover a longer distance to get to work, whereas older workforce people can afford to live closer to where they work. 


![Avg_Trip_Duration](https://user-images.githubusercontent.com/33167541/186766343-53c3e818-b8ff-435c-941f-78e2d1663437.png)


Finally, the checkout times for overall users was used to see how long the majority of users are using the bikes. 

![Checkout_Times_Users](https://user-images.githubusercontent.com/33167541/186767628-6977ea3f-f8f2-48ac-8d2d-f7e3ccf64a05.png)



--- 
### Gender Demographics

Most of the users' genders were recorded, giving insight to what customers are using the service. The gender distribution was plotted in a pie chart examining the ride counts and gender data collected. 

![Gender_Dist](https://user-images.githubusercontent.com/33167541/186767237-eeadb496-b0d1-4a49-9c99-37d8f6f3c73f.png)


Further, the duration of checkout times by gender was found per hour after checkout, which provides some interesting insight to the users. While there isn't an analysis on which users are unknown (subscribers vs customers), there seems to be a much flatter distribution of unknown users, suggesting much more variance in the ride times - more indicative of tourists than of daily riders.  

![Checkout_Times_Gender](https://user-images.githubusercontent.com/33167541/186767964-53fd5987-d9bd-4011-80be-690ea1cf2498.png)


Male riders are the majority users of the CitiBike service, which may be reflective of perception of safety. New York has a lower than average crime rate per capital; however, it is still a large city and is not as safe for females to ride alone as males. The perception of safety in Des Moines is much higher, and the distribution in Iowa may become less skewed than the divide in the New York data, especially given the high ranking for safety. 


---
### Peak Times and Days

One of the most important factors to consider is when the service is being used. If the majority of the bikesharing is normally distributed across the day, it would be hard to sell the idea that most people are using the service for work, whereas a higher volume of usage on workdays during times of the morning and evening commutes would reflect that many of the users are using this as a means of transportation and not merely recreationally. 


![Peak_Days](https://user-images.githubusercontent.com/33167541/186769416-743b3cfa-566d-4ee5-b831-c80b5e12685f.png)


![Peak_Hours](https://user-images.githubusercontent.com/33167541/186769441-b3f9fb7f-d7ba-49e7-ab42-37218156cad1.png)


![Trips_by_Weekday](https://user-images.githubusercontent.com/33167541/186769472-4d66f3bd-71c5-4751-9bc6-49aee0c79fc8.png)


In the above three figures, it can be seen that the majority of rides take place on Thursday with the lowest ridership on Sundays and Wednesdays. The distribution of peak times is bimodal, with one peak centered at 8 AM and the second at 5 PM. The most interesting finding is on the last of these: Wednesday mornings are no less busy than the other weekdays, but Wednesday evening has very low ridership. There is only one logical explanation for this - "Happy Hour". Since New Yorkers have a reputation of being responsible citizens, those who used the bikeshare in the morning to get to their workplace who went out for a drink after work likely took a rideshare service such as Uber or Lyft to get home rather than driving while intoxicated (as it is illegal to ride a bicycle while intoxicated on public streets). 

The final two figures show the heat map breakdown of users by gender:

![Trips_by_Gender_All](https://user-images.githubusercontent.com/33167541/186770367-fac9489f-bc56-4fe2-8a3e-ad3a7d2508fc.png)

![User_Trips_Gender_Weekday](https://user-images.githubusercontent.com/33167541/186770376-4c381b27-923f-4dce-8eb0-c32a95595a01.png)


Further supporting the hypothesis that the users with an unknown gender are more likey tourists, the days of highest use are Saturday and Sunday with the heaviest usage between the hours of 10 AM and 7 PM. The Female and Male users alike have the heavireest use in the mornings and afternoons on weekdays during commuting hours. Comparing the customers with the subscribers, it becomes very clear that the lack of clear density spots during the week and the higher densities on Saturday and Sunday suggests that Customers are likely tourists or non-locals, using the service for recreation rather than as a means of transportation, and Subscribers haev the heaviest use during the weekdays for male and female users. The unknown gender subscribers do have data collected on rides, but there isn't enough to show a relationship on daily usage - it seems to be equally distributed. 


---
## Conclusion

Since Des Moines is not considered a tourist attraction, it would be problematic to start a service that is primarily driven by recreational users. However, the CitiBike service in New York appears to be primarily utilized as a means of transportation to and from the workplace. As the city of Des Moines continues to grow, traffic on the streets is inevitable, and the appeal of riding a bicycle to work will be an asset to the city. Even though the population of Des Moines is 33 times smaller than that of New York city, the number of needed bicycles would be a fraction of those in New York, and if there is similar subscriber numbers, this could be a very profitable opportunity. The one caveat that remains and is not represented in this data is the proximity of people to their places of work. Since the majority of New York is vertical, it is possible for people to live within a few miles of their workplace, keeping the ride times down to 15 minutes. If the majority of people in Des Moines live beyond a reasonable distance to ride to work, there may not be enough interest in such a program. Furthremore, there will have to be hubs for the service throughout the city, but how far would someone have to travel from their home in a more suburban residence to get to the bikesharing facility.  



---
Git lfs was used for the large csv files. 

version https://git-lfs.github.com/spec/v1
oid sha256:b72aecb6b22a0369aff52298d813090c035363c0680ac136513c6655bb2bcde7
size 13

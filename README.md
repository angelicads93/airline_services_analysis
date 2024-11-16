# British Airways services according to their customer’s reviews

The work presented here is a job simulation from British Airways (B.A). The goal is to assess the customers perception of the airline and satisfaction with the services. Having a better understanding of the customers and their needs is key to improve their experiences, gain their loyalty and attract more customers. 

## The Data:
The data consisted on customer's reviews left on the website https://www.airlinequality.com/airline-reviews/british-airways. Each review contains a written comment, an itemized summary of the trip, and star ratings of various services. Each component can be conveniently scraped from the HTML site with the Python library Beautiful Soup and transferred to a Pandas data frame. The total size of the data set is 1000 reviews. 


Field | Description | Example
------ | -------| -------
Type Of Traveller | Reason of the trip: Solo Leisure, Couple Leisure, Family Leisure or Business. | Solo Leisure
Seat Type | Type of seat depending on comfort: Economy Class, Premium Economy, Business Class or First Class.| Business Class
Route | A sentence describing the origin, destination and location of layoff if any. | Johannesburg to New York City via Heathrow
Date Flown | Month and year of the flight | October 2024
Aircraft | Maker and model of the aircraft | Boeing 777-336 ER
Seat Comfort, Cabin Staff Service, Food & Beverages, Inflight Entertainment, Ground Service, Wifi & Connectivity, Value For Money | Services rated from 1 star to 5 stars | 4 stars
Comment | Text | 
Recommended | yes or no| yes


## Type of customers:
It is interesting to know more about the customers who provided their feedback. Below is shown their distribution according to the reason of their trip and their type of seat. Most of the customers travel for solo leisure or for business, although overall, the proportion of type of travellers is mostly uniform. As expected, the type of seat does shows more differences, more than 50% of the costumers who provided reviews travelled in economic class, and following, are travellers on business class. 

![piePlots](https://github.com/user-attachments/assets/bd9a9c5f-bf6b-4b2f-a4b6-5ff4d760626d)

## Star-rating reviews:
Let’s continue with the features evaluated through the star rating system. The distributions of the customer’s answers are shown in the figure below. It is possible that customers are more incline to give a review when their experience was not what they expected, in which case, these statistics may not be reflecting the true collective perception of the airline but instead, they may be emphasising the down sides of the service. Still, if this is the case, the results presented in this figure are precisely the type of information that can be valuable to improve customer's experience and satisfaction. 

Overall, the service provided by the cabin staff shows the best result. It is indeed the only category where the most frequent star-rating is not one-star, but in fact five-stars. The rest of the services could use some improvement, especially ground services. Moreover, a significant amount of customer did not provide a feedback of the in-flight entertainment, WiFi and connectivity, perhaps because they did not use the service. However, a large proportion of customer who did rate the service express dissatisfaction, especially for the WiFi and connectivity. 

<img src="https://github.com/user-attachments/assets/1d8ad953-971d-47d6-954f-8bc7f22d8e6e" width=80% height=80%>

## Sentiment analysis on customer's comments:
To dissect more the information behind the data, let's also consider the customer's written comments. For this we can perform a sentiment analysis using as tool the Python library TextBlob, leading to a quantitative measure of the review's "polarity" and "subjectivity". They are evaluated between 0 and 1, where maximum polarity implies a positive experience. The last two figures shows the polarity of the customers, according to both their type seat and reason for traveling. It can be noticed that in average, the customers perception of the airline and its services is neutral. Some interesting features on these plots are the outliers points, particularly the ones with lowest polarity. They indicate that customers travelling for business or couple leisure were more likely to have an unsatisfactory experience, as well as customers on business and premium business seats. 

<img src="https://github.com/user-attachments/assets/588ad34d-284d-4679-9ad7-b3876947cf32" width=80% height=80%>

<img src="https://github.com/user-attachments/assets/98b6ed9d-1bdc-43cd-b60d-0722eb0dd4de" width=80% height=80%>

## Conclusion:


So, given the proportions of type of traveller and seat type from the figures above, improving the experience of couples traveling for leisure and customers traveling in business class, will have the largest positive impact on the satisfaction of British Airways customers.

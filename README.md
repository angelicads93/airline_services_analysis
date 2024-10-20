# British Airways services according to their customer’s reviews

This is a job simulation from British Airways, the goal is to use customer's feedback found in https://www.airlinequality.com/airline-reviews/british-airways, to assess their perception of the airline and satisfaction with the services. Each customer review consists of a written comment, an itemized summary of the trip (e.g., aircraft, route, date flown), and star ratings of various services (e.g., Seat Comfort, Food \& Beverages, Ground Service). Each component can be conveniently scraped from the HTML site with the Python library Beautiful Soup and transferred to a Pandas data frame. There total size of the data set is 1000 reviews. 

Let’s start with the features evaluated through the star rating system. The distributions of the customer’s answers are shown in figure below. A significant amount of customer did not provide a feedback of the in-flight entertainment, WiFi and connectivity, perhaps because they did not use the service. However, a large proportion of customer who did rated the service express dissatisfaction, especially for the WiFi and connectivity. It is possible that customers are more incline to give a review when their experience was not what they expected, in which case, these statistics may not be reflecting the true collective perception of the airline but instead it may be emphasising its negative aspects. Still, if this is the case, the results presented in Figure 1 are precisely the type of information that can be valuable to improve the experience and satisfaction of customers. Overall, the service provided by the cabin staff shows the best result. It is indeed the only category where the largest numbered rating is not one, but in fact five. The rest of the services could use some improvement, especially ground services.

<img src="https://github.com/user-attachments/assets/1d8ad953-971d-47d6-954f-8bc7f22d8e6e" width=80% height=80%>

It is interesting to know more about the customers who provided their feedback. Below is shown their distribution according to the reason of their trip and their type of seat. Most of the customers travel for solo leisure or for business, although overall, the proportion of type of travellers is mostly uniform. As expected, the type of seat does shows more differences, more than 50% of the costumers who provided reviews travelled in economic seats, and following are traveller on business seats. 

![piePlots](https://github.com/user-attachments/assets/bd9a9c5f-bf6b-4b2f-a4b6-5ff4d760626d)

To dissect more the information behind the data, let's also consider the customer written comments. For this we can perform a sentiment analysis using as tool the Python library TextBlob, leading to a quantitative measure of the review's "polarity" and "subjectivity". They are measured between 0 and 1, where maximum polarity implies a positive experience. The last two figures shows the polarity of the customers, according to both their type seat and reason for traveling. In average, the customers perception of the airline and its services is neutral. Some interesting features on the above mentioned plots are the outliers points, particularly the ones with lowest polarity. Customers travelling for business or couple leisure were more likely to have a unsatisfactory experience, as well as customers on business and premium business seats. 

<img src="https://github.com/user-attachments/assets/588ad34d-284d-4679-9ad7-b3876947cf32" width=80% height=80%>

<img src="https://github.com/user-attachments/assets/98b6ed9d-1bdc-43cd-b60d-0722eb0dd4de" width=80% height=80%>


So, given the proportions of type of traveller and seat type from the figures above, improving the experience of couples traveling for leisure and customers traveling in business class, will have the largest positive impact on the satisfaction of British Airways customers.

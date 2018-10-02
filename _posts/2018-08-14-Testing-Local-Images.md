---
layout: post
title: Maximizing the New York Minute
---

Weaving through the NYC subway commute, an untrained eye would see only chaos amongst the 6 million daily passengers. A data scientist, however, would see an intricate data set for answering a key marketing question - how to maximize market exposure while minimizing costs. And thinking like a data scientist is the first step of my data science bootcamp journey. 

Given a client’s question on where and when to strategically place street teams, MTA turnstile recordings provides a myriad of open source data for completing this request. It also provides an opportunity for me to learn more about the data science approach as well as providing a minimum viable product for a client.
***
My team’s approach was to combine data science techniques with key intuitions in order to maximize both quantity and quality. 

This concept stated as an equation would be: 
Reach = Impressions x Conversion Rate
         Where:
Impressions : Data Science
Conversion Rate : Intuition

First  we aimed to maximize the street team’s conversion rate by placing them in key areas where the average commuter would be most interested in the organization’s mission. The next step would be to maximize the volume of foot traffic the street teams could meet by finding the stations within the selected regions with the highest average hourly passenger hour.
***
The client provided the following goals:
  1. Build Awareness
  2. Fill event space
  3. Increase Donor Pool

Additional to the goals, we were also provided that the event space would be held in the Lower East Side on the cusp of Summer. From here we built our investigation on three core foundations to reach NYer most likely to be in our market segment:
  1. Direct access to the Gala location
  2. High tech industry density
  3. Affluent Areas

With some reconnisounce on industry in the Big Apple we able to focus our search in Manhattan’s “Silicon Alley” and the Brooklyn Tech Triangular. We specifically focused on stations along the Brown, Green, and Orange lines, since these allow the easier access to the Gala space. From these constraints we chose about 20 stations to focus on in our analysis.
___
After determining our approach we started gathering and preparing our data. In this blog I will be discussing our thought process, for the commented code on this project I encourage you to visit my Github repository.

Using Scrappy we pulled all the turnstile datasets, then limited the data to just May, June, and July of the past two years. The turnstile machines were anything but infallible, so much of our time was spent processing errors.  

After much manipulation we found an average passenger per hour rate at each station. 
We then focused our attention on the highest average rates within our selected stations.
We also checked to see where our priority stations fell among the top 40 stations.


Finally, we examined average weekly and daily rates among our top 3 priority stations to find the best time to send out the street teams. Our boxplot below allows the client to easily see the medium rate for each station, as well as better understand if the rate is fairly consistent or is influence by a high concentration of outliers. The weekly data shows all work days are suitable for the street teams.


Hourly rates are calculated based off of 4 hour reporting segments. This means the high rates at 9pm ecomposses a time period starting at 5pm. From this graph we see the optimal time would be during the rush hour block.


At the end of the week we were able to report back to our client with the answer to their inquiry (and our minimum viable product) that they should send street teams to 14th St, 14St-Union Sq, and 23St during rush hour (5-9pm) during any given weekday.

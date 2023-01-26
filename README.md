# BTT AI Fall 2022 Studio Project 
## Orbital Insight: The Effect of Typhoons on Shanghai Shipments

The problem that I was working to solve in my AI Studio project is to build and test a model that would accurately predict the dwell times of ships heading to Shanghai during and outside of typhoon season. My approach to solving this problem was to gather AIS data on the Shanghai Port. Calculate each ship's dwell time (how long a ship remains anchored at a port) by finding the difference between the first and last ping using Unix time. We had to create a dictionary to store trip numbers and trip duration and use ships’ features of nav status codes (anchored). 

We used dwell time predictions to make a general hypothesis of how storms will affect a port’s average dwell time. The dataset was obtained from the company through their website called GO. We picked out the area of interest and timeframe in which we wanted our data to come. It contained ship pings and other ais information such as destination, nav status code, length, width, etc. Our problem was a supervised learning regression in which the label was dwell time and the rest of the features were used for our chosen models: linear regression, random forest, and gradient boosting. Our best results were with the Gradient Boosting Regressor, it had the lowest mean absolute error (only by a negligible amount) of 26.34 which is not so great since it is very high. 

![Screenshot 2023-01-25 233732](https://user-images.githubusercontent.com/34352705/214759601-22208a0e-671c-4436-9708-c7e2fb0cf3e6.jpg)

Some reasons in why we had no so great results would be we overfitted the model, or features may not lead to accurate predictions. And some potential solutions we can do is spend more tinkering, try using different/more datasets, and potentially look at approaching it as a classification problem. 

The impact of this data will help describe and predict how long delays will be for Shanghai Ports when a particular typhoon occurs. Merchants and businesses need to know when shipments arrive Shanghai is one of the busiest ports in the world. Delays here impact the global supply chain, making this important to understand. And we would see the effect that worsening typhoons (caused by climate change) could have on shipping

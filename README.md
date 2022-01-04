# INFO2950
Fall 2021 INFO 2950 Project: jzy7, fkd6, swz8

#🌃 Exploring Airbnbs in New York City

One of the top tourist destinations in the United States is New York, New York. From the bustling energy of Times Square to the Statue of Liberty’s iconic silhouette to Central Park’s lush greenery, New York City promises entertainment to guests of all ages and interests. As such, the tourism industry in New York City is immense. Prior to the coronavirus pandemic, NYC saw a record-breaking ten year period of growth in tourism, culminating in a total of 66.6 million visitors in 2019 ([Office of the New York State Controller](https://www.osc.state.ny.us/reports/osdc/tourism-industry-new-york-city)).  A crucial part of the tourism industry is the hotel industry - with such a large influx of visitors, there must be adequate lodging to support them. This can be a particular challenge for New York City, which is already densely populated and has limited physical space for expansion. As tourism continues to increase, alternative forms of housing are growing in popularity, including pod hotels, hostels, and renting individually hosted properties.
    
The most widespread platform for listing and renting private property is Airbnb. Airbnb was formed in 2008 by three designers who started off using their own San Francisco home as a bed-and-breakfast to bring in additional income to pay for rent. Recognizing the market potential of their idea, the founders launched the startup Air Bed & Breakfast, which subsequently became Airbnb in 2009. Airbnb does not own any of the properties listed on its website; it simply serves as an interface for connecting people who have extra space they want to rent out with people who are traveling and need a place to stay. Airbnb is free to use and involves a straightforward online account sign-up. Potential guests enter their desired location and their period of stay to populate a list of available Airbnb properties that they can then browse and filter through. Upon finding a property they’re interested in, guests send a request to the host, who can then approve or deny the booking. On the whole, an Airbnb stay tends to be cheaper than rooming at a standard hotel, and Airbnbs also offer the appeal of additional amenities and unique personalization or character.
    
Hosting an Airbnb can be a profitable side business for those with extra room to spare or who are interested in converting an additional property into a rental. [A 2019 study conducted by Earnest.com](https://www.earnest.com/blog/sharing-economy-income-data/) found that on average Airbnb hosts make \\$924 a month, which is nearly three times as much as the average earnings of other positions in the sharing economy (sharing economy refers to the market space of temporary workers who offer some service using their existing assets; in layman’s terms, a “side hustle”), such as Doordashers, Lyft and Uber drivers, and Etsy shop owners. However, this \\$924 income is extremely variable depending on where the listing is based, the frequency at which it’s rented out, and the quality of the listing.
    
With the tourist demand of New York City and the potential profit of Airbnb hosting in mind, we were curious as to how potential hosts in New York City could offer an optimal - and profitable - stay to guests. New York City offers an ideal backdrop for us to conduct our study, as there is a consistent year-round need for lodging. Since our dataset of focus does not include directly accessible information about host profit (this is private and protected information that cannot simply be scraped from Airbnb’s website), we approach Airbnb listings first on the basis of rating, considering nine different variables that might influence the overall rating out of 5 stars achieved by a listing. Note that all values in the dataset represent the standings as of September 1 2021, which is when the creator of the dataset most recently scraped Airbnb’s website. Specifically, we examined the following variables: 
    
* Percentage of guest messages hosts responded to
* Percentage of booking requests host accepted
* Whether the host was designated as a superhost by Airbnb (a title that’s designated on the basis of experience and level of activity over the course of one year)
* Neighborhood (borough) of New York City in which the listing is located
* Number of guests accommodated
* Number of bedrooms
* Number of bathrooms
* Amenities offered (within which we identified five popular amenities to screen for, listed below)
    * Pets allowed
    * WiFi
    * Parking available
    * Pool
    * Kitchen
    * Air conditioning
* Price per night.

To analyze each of the above factors, we calculated summary statistics to capture the overall distribution among all New York City Airbnbs, visualized each factor in relation to the overall Airbnb rating, and calculated covariance and correlation statistics. Because our goal is to be able to offer advice to Airbnb hosts on how to improve their listing’s rating, we fitted regression models to each of the listed variables as predictors of overall rating. Given that guests typically rate Airbnbs based on the big picture of their experience and not singular aspects, we performed a multivariable analysis to look at how these qualities work in tandem to influence guest satisfaction. In conducting these analyses, we sought to determine whether there was a significant difference in rating based on any of the attributes individually or in combination.
    
An important follow-up to our exploration of rating is the determination of whether ratings have a meaningful impact on how often a listing is booked, which translates to how much profit the host can make. This was an essential analysis to perform because Airbnb hosts would only want to invest time and resources into improving their rating if it ultimately equates to making more money and getting a return on their investment. We manipulated a dataset from the same source to calculate the percentage of nights out of the next 365 days that each Airbnb listing was booked out for. By examining the relationship between the overall listing rating out of 5 stars and the booking percentage, we aimed to find out whether there was a significant relationship between these two variables.

To follow up on our linear and logistic predictive modeling, we evaluated significance using analysis of variance (ANOVA). These methods of determining statistical difference provide us with another way to consider whether each of our analyzed variables have a bearing on overall Airbnb rating and whether rating then affects booking performance.
    
Through the process and results of this study, we hope to answer the overarching questions: “What factors most influence the ratings of Airbnb listings in New York City? How do these ratings in turn influence the booking rate of listings?”. To provide more specificity and direction, we defined secondary questions that we targeted during our analysis:
* By grouping the factors\* into broad categories of host attributes (host response percentage, host acceptance percentage, and superhost status) and listing attributes (neighborhood, number of guests accommodated, number of bedrooms, number of bathrooms, and amenities), can a more specialized relationship with rating be identified? 
    * \*Price was not grouped and was instead treated individually, since it falls outside of both host behaviors and physical qualities of the rental property.
* Between host attributes, listing attributes, and pricing, which has the greatest impact on overall Airbnb rating?

The study that follows and our subsequent findings may be particularly applicable to people seeking to host Airbnbs in New York City, but our analysis also brings up interesting insights for anyone who is involved in or has interacted with the tourism and hotel industries of America.

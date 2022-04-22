# surfs_up
# Overview 
You are looking to open a surf and ice cream shop in Oahu, where surfboards and ice cream will be served to locals and tourists. To get
the business off the ground, you reach out to a potential investor. The investor has some concerns regarding the weather and requests
a weather analysis on an Oahu weather dataset he has to help him make the decision to invest (he previously had a business go under due to the weather).  

## Purpose
After running general analysis, the investor asks specifically for additional temperature data for the months of June and December in Oahu, in order to determine 
if the surf and ice cream shop business is sustainable year-round.

# Results
After running additional queries to filter the Measurement data table by month, we get additional temperature data specific to the months of June and December in Oahu from the dataset, as seen in the example below:

![june session query](https://user-images.githubusercontent.com/99205688/164776425-ac569cc3-e993-422a-86b9-5045b7f1012a.PNG)

## Takeaways
Three key differences in weather between June and December are:
* In December, the standard deviation in temperatures is larger, which indicates there can be more fluctuation in temperature in December than in June.
* The minimum temperature recorded in December is 56 degrees F while in June the minimum recorded temperature is 69 degrees F. While there is some notable
difference on the minimum end of temperatures when comparing these months, the maximum temperatures are more close together, with a maximum of 83 degrees F
in December and 85 degrees F in June.
* The first quartile of temperatures in December is cooler than June with temperatures below 69 degrees F, while in June the first quartile of temperatures are 
below 73 degrees F.

## Summary Statistics

![June temps](https://user-images.githubusercontent.com/99205688/164776509-07541ae7-0b98-4d9d-9222-c03fc7e36fc5.PNG)
![Dec temps](https://user-images.githubusercontent.com/99205688/164776518-16de9727-2043-42fc-8567-05d15299f81f.PNG)

# Summary
## Overall Summary
Overall, the temperatures in June seem promising, with most temperatures recorded staying in the 70's. This is a good temperature for both surfing and ice cream.
Temperatures in December fluctuate more and can be colder , with more temperature recordings dipping into the 60's and high 50's, which may still be suitable for
surfing or ice cream, but we could reasonably expect that the colder temperatures could have impact on the amount of business. As long as we are prepared to see
a potential dip in business in December, it seems the business should be able to operate year round. 

## Additional Queries

### Query reporting stations in June and December
We can expect that a weather recording station's elevation can impact the fluctuation in temperatures recorded on the island. We can run an additional query to see which stations reported the most weather data in June and December and take into account the elevation of those stations. 

Stations with the highest elevation:
![elevation station](https://user-images.githubusercontent.com/99205688/164776765-a87a5777-54d9-4084-b2a9-bf8a4d1a6cf4.PNG)

Stations reported most weather data in June and December:

![june stations](https://user-images.githubusercontent.com/99205688/164776885-0a972d28-ce5b-437a-a7fb-a8acc24960ef.PNG)

![dec station](https://user-images.githubusercontent.com/99205688/164776896-dd5917f0-70d7-49ac-b1df-54e3fb4ee781.PNG)

After running the query, it can be seen that the stations with the highest elevations (Upper Wahiawa and Manoa Lyon Arbo) represent the lowest and 5th lowest numbers of weather reports in June and December. This is helpful to know that the station with the highest elevation (Upper Wahiawa) is not greatly skewing the data. However, it can be taken into account that the weather data points reported by Manoa Lyon Arbo is almost the same as many stations with much lower elevation and it may be worthwhile to dive deeper into the reported data from Manoa Lyon Arbo to see if those numbers contribute more towards the fluctuations seen in December.
 
### Query perciptation in June and December
An additional query can be regarding percipitation levels in June and December. After querying the data, it appears that perciptation recordings in
December reported an average of .21 inches of rain. In June, an average of .14 inches of rain were reported. Although June had less percipitation reported
on average, the overall rainfall per month was quite similar for the 1st, 2nd and 3rd quartiles of data, and both months had a standard deviation less than 1. 
This bodes well for the surf/ice cream business as it means that December is not a wash out compared to June.  

![june prcp](https://user-images.githubusercontent.com/99205688/164776936-b624e322-4223-45f9-a966-308d6a135197.PNG)
![dec prcp](https://user-images.githubusercontent.com/99205688/164776952-735848cd-d4f4-4999-ad8b-738522f20cfe.PNG)


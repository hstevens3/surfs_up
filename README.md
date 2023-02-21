# Module 9 Challenge 

# Surfs-Up Weather Analysis

## Overview of the Analysis

This challenge is to prepare summary statistics of weather data for Oahu. By completing the challenge, we are learning how to query SQLite databases with SQLAlchemy, Python and Pandas functions.  

## Results

From the analysis, we learned that

- Weather is not that different in June versus December in Oahu. The average temperature year round is in the seventies. I wish that were true where I live!
---
- There is a greater range of temperatures in December (56-83) than in June (64-85).This can be seen in the images below along with other summary statistics.
#### June Summary Statistics
![June Summary Statistics](/Resources/June_Temperature_Statistics.png)

#### December Summary Statistics
![December Summary Statistics](/Resources/December_Temperature_Statistics.png)

---
- The temperature is less variable in June than December, with most days falling between 73-77 degrees. The histograms below show the distribution of temperatures for both months.
#### June Temperatures
![June Temperatures](/Resources/June_Temperatures.png)
#### December Temperatures
![December Temperatures](/Resources/December_Temperatures.png)

---

## Summary

As we can see, this analysis was helpful to show that Oahu is a feasible location for a surf shop and/or ice cream stand. The lowest temperature in either month across several years of data was 56 degrees, so although not many people would want ice cream on that day, it is still good for surfing. Temperatures that low are rare, the weather is typically in the 60s and 70s. 

---
For additional analysis, it would be helpful to query precipitation for June and December. If it is often rainy during certain months, that would be good to know for determining seasonal hours. A query similar to these could be used:
results = session.query(Measurement.prcp).filter(extract('month', Measurement.date)==6).all()
where 6 is the month number for June and could be updated to any other number 1-12.


The data used for this analysis does not include wind information, but if it did, the wind speeds might be of interest to surfers.
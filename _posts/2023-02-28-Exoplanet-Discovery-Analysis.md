---
title: "Exoplanet Discovery Analysis"
layout: post
---

So I found this dataset containing exoplanet discoveries from 1989 to 2014. Here's a list of exploratory questions that I answered to get a better understanding of what's going on in this dataset. 

1. How many exoplanets are missing values for all 3 planet characteristics at once (mass, orbital
period, and distance)?
2. Were there any years between 1989 and 2014 where no exoplanets were discovered? 
3. Out of the 3 most common discovery methods, which appears to be the most capable of finding
faraway exoplanets?
4. How far away is the closest exoplanet whose mass is unknown?
5. How far away is the furthest exoplanet whose mass is known?
6. How far away is the exoplanet with the longest orbital period?
7. What is the shortest orbital period of the exoplanets with no known mass?
8. What is the average distance of exoplanets whose mass is known? What is the average distance
of exoplanets whose mass is unknown? 
9. Which exoplanet discovery method is responsible for the most missing mass values? 

```
import pandas as pd
df = pd.read_csv('exoplanets.csv')
df
```
|     | method          |   number |   orbital_period |     mass |   distance |   year |
|----:|:----------------|---------:|-----------------:|---------:|-----------:|-------:|
| 863 | Transit         |        2 |         25.5169  | nan      |     nan    |   2014 |
| 163 | Transit         |        1 |         10.8635  | nan      |     190    |   2010 |
| 177 | Transit         |        1 |          3.25721 | nan      |     395    |   2011 |
| 760 | Transit         |        2 |          5.72932 | nan      |     nan    |   2012 |
| 820 | Transit         |        7 |         59.7367  | nan      |     780    |   2013 |
| 473 | Radial Velocity |        3 |         11.577   |   0.0166 |      14.56 |   2011 |
| 772 | Transit         |        5 |         18.1641  | nan      |     368    |   2013 |
| 345 | Radial Velocity |        1 |        589.64    |   2.9    |      10.34 |   2006 |
| 867 | Transit         |        2 |         42.882   | nan      |     nan    |   2013 |
| 494 | Radial Velocity |        1 |       2097       |   3      |      85.18 |   2009 |

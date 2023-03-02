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
| 293 | Radial Velocity |        1 |       1049       |   0.79   |      45.01 |   2009 |
| 123 | Radial Velocity |        1 |          2.64385 | nan      |      10.23 |   2004 |
| 369 | Radial Velocity |        1 |          5.7361  | nan      |      41.27 |   2012 |
| 129 | Radial Velocity |        1 |        598.3     |   0.328  |      10.32 |   2009 |
| 980 | Transit         |        1 |          2.34121 | nan      |     nan    |   2010 |
| 609 | Radial Velocity |        1 |          3.8335  |   0.06   |      81.1  |   2007 |
| 103 | Transit         |        1 |          2.82804 | nan      |    1150    |   2010 |
| 829 | Radial Velocity |        2 |       1460       | nan      |     nan    |   2014 |
| 302 | Radial Velocity |        3 |          5.6363  |   0.0117 |      25.59 |   2011 |
| 557 | Radial Velocity |        1 |         14.275   |   0.0316 |      17.72 |   2011 |


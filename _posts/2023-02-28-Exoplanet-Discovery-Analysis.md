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
| Date       |   MSFT |   KLM |   ING |   MOS |
|:-----------|-------:|------:|------:|------:|
| 2000-01-20 |  34.35 |  0.35 | 14.06 | 14.09 |
| 2000-01-21 |  34.33 |  0.35 | 13.92 | 13.79 |
| 2000-01-24 |  33.3  |  0.35 | 13.56 | 13.79 |
| 2000-01-25 |  32.4  |  0.35 | 13.22 | 13.45 |
| 2000-01-26 |  32.86 |  0.35 | 13.33 | 13.59 |
| 2000-01-27 |  32.05 |  0.35 | 13.28 | 13.25 |
| 2000-01-28 |  31.48 |  0.35 | 13.09 | 13    |
| 2000-01-31 |  31.32 |  0.35 | 12.79 | 13.3  |
| 2000-02-01 |  31.6  |  0.35 | 12.78 | 13.59 |
| 2000-02-02 |  32.86 |  0.35 | 12.7  | 13.45 |


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

| method          |   number |   orbital_period |   mass |   distance |   year |
|:----------------|---------:|-----------------:|-------:|-----------:|-------:|
| Radial Velocity |        1 |          269.3   |   7.1  |      77.4  |   2006 |
| Radial Velocity |        1 |          874.774 |   2.21 |      56.95 |   2008 |
| Radial Velocity |        1 |          763     |   2.6  |      19.84 |   2011 |
| Radial Velocity |        1 |          326.03  |  19.4  |     110.62 |   2007 |
| Radial Velocity |        1 |          516.22  |  10.5  |     119.47 |   2009 |
| Radial Velocity |        1 |          185.84  |   4.8  |      76.39 |   2008 |
| Radial Velocity |        1 |         1773.4   |   4.64 |      18.15 |   2002 |
| Radial Velocity |        1 |          798.5   | nan    |      21.41 |   1996 |
| Radial Velocity |        1 |          993.3   |  10.3  |      73.1  |   2008 |
| Radial Velocity |        2 |          452.8   |   1.99 |      74.79 |   2010 |

How many exoplanets are missing values for all 3 planet characteristics at once (mass, orbital
period, and distance)?

Before I fully do the proper slicing to find how many of these entires from the dataframe have missing values for the three main columns, I just want to get an idea of how many missing values I'm dealing with as a whole. 

```
df.info()
```

RangeIndex: 1035 entries, 0 to 1034
Data columns (total 6 columns):

| column                    |       Non-Null Count |                Dtype |
|:-------------------------:|---------------------:|---------------------:|
| method                    |        1035 non-null |               object | 
| number                    |        1035 non-null |                int64 |
| orbital_period            |         992 non-null |              float64 |
| mass                      |         513 non-null |              float64 |
| distance                  |         808 non-null |              float64 |
| year                      |        1035 non-null |                int64 |

 
 ```
 df[(df['orbital_period'].isnull() & df['mass'].isnull() & df['distance'].isnull())]
 ```

| method                    |   number |   orbital_period |   mass |   distance |   year |
|:--------------------------|---------:|-----------------:|-------:|-----------:|-------:|
| Imaging                   |        1 |              nan |    nan |        nan |   2008 |
| Imaging                   |        1 |              nan |    nan |        nan |   2006 |
| Transit Timing Variations |        3 |              nan |    nan |        nan |   2014 |
| Microlensing              |        1 |              nan |    nan |        nan |   2008 |
| Microlensing              |        1 |              nan |    nan |        nan |   2008 |
| Microlensing              |        1 |              nan |    nan |        nan |   2009 |
| Microlensing              |        1 |              nan |    nan |        nan |   2010 |
| Microlensing              |        1 |              nan |    nan |        nan |   2004 |
| Microlensing              |        1 |              nan |    nan |        nan |   2009 |
| Imaging                   |        1 |              nan |    nan |        nan |   2010 |
| Imaging                   |        1 |              nan |    nan |        nan |   2008 |

Here we can see the 11 total discoveries that had orbital period, mass, and distance as unknown values. 

Were there any years between 1989 and 2014 where no exoplanets were discovered? 

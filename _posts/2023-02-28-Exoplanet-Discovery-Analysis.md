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
method  number  orbital_period    mass  distance  year
398  Radial Velocity       2      103.490000  0.0400     26.21  2011
390  Radial Velocity       2       13.186000  0.0263     42.52  2011
629  Radial Velocity       3      147.730000  1.2800     52.88  2006
475  Radial Velocity       3      106.720000  0.0300     14.56  2011
297  Radial Velocity       3     2295.000000  0.6830     33.24  2002
662          Transit       2        0.837495     NaN    173.00  2011
298  Radial Velocity       3      843.600000  0.6240     33.24  2005
740          Transit       4        9.673928     NaN       NaN  2012
471  Radial Velocity       3      459.260000  0.1210     26.91  2011
500  Radial Velocity       2      408.600000  2.2400     68.54  2004

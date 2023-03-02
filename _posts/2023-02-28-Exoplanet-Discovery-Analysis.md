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

mass  distance  year
0     Radial Velocity       1      269.300000   7.10     77.40  2006
1     Radial Velocity       1      874.774000   2.21     56.95  2008
2     Radial Velocity       1      763.000000   2.60     19.84  2011
3     Radial Velocity       1      326.030000  19.40    110.62  2007
4     Radial Velocity       1      516.220000  10.50    119.47  2009
...               ...     ...             ...    ...       ...   ...
1030          Transit       1        3.941507    NaN    172.00  2006
1031          Transit       1        2.615864    NaN    148.00  2007
1032          Transit       1        3.191524    NaN    174.00  2007
1033          Transit       1        4.125083    NaN    293.00  2008
1034          Transit       1        4.187757    NaN    260.00  2008


---
title: "College Scorecard Analysis"
layout: post
---

As a submission for an internship for the Carroll and Milton Petrie Foundation, I did some exploratory analysis for 
this [dataset](https://collegescorecard.ed.gov/data/) containing countless information about colleges in the United States. 
The full documentation listed on College Scorecard can be found [here]('https://collegescorecard.ed.gov/data/documentation/'). 


In the original dataframe that was derived from the dataset, there were too many columns to work with. After a bit of dimensional reduction
and cleaning up missing values, I decided on the main columns that I wanted to work with. 

```
df
```

|      |   region | institution                      | state   | city        |   fed_loan_percentage |   pell_grant_percentage |   median_student_debt |   total_students |   ugds_men |   ugds_women |   ugds_white |   ugds_black |   ugds_hisp |   ugds_asian |   ugds_aian |   ugds_nhpi |   ugds_2more |   ugds_nr |   ugds_unkn |
|-----:|---------:|:---------------------------------|:--------|:------------|----------------------:|------------------------:|----------------------:|-----------------:|-----------:|-------------:|-------------:|-------------:|------------:|-------------:|------------:|------------:|-------------:|----------:|------------:|
| 4824 |        5 | Charleston School of Law         | SC      | Charleston  |              nan      |                nan      |                   nan |              nan |   nan      |     nan      |     nan      |     nan      |    nan      |     nan      |    nan      |    nan      |     nan      |  nan      |    nan      |
| 1379 |        2 | Morgan State University          | MD      | Baltimore   |                0.7861 |                  0.5582 |                 18359 |             6263 |     0.3944 |       0.6056 |       0.0164 |       0.8258 |      0.0442 |       0.0057 |      0.0016 |      0.001  |       0.035  |    0.0398 |      0.0305 |
| 1425 |        1 | Clark University                 | MA      | Worcester   |                0.6256 |                  0.2316 |                 23000 |             2205 |     0.3787 |       0.6213 |       0.6177 |       0.0481 |      0.0971 |       0.0707 |      0.0005 |      0.0005 |       0.0327 |    0.0916 |      0.0413 |
| 2717 |        8 | Portland State University        | OR      | Portland    |                0.3452 |                  0.5362 |                 16166 |            16596 |     0.44   |       0.56   |       0.5101 |       0.0398 |      0.1864 |       0.0987 |      0.0116 |      0.0066 |       0.0674 |    0.0375 |      0.0421 |
| 5070 |        6 | The Art Institute of San Antonio | TX      | San Antonio |                0.5556 |                  0.5694 |                 19000 |              374 |     0.4492 |       0.5508 |       0.254  |       0.1925 |      0.4545 |       0.0134 |      0.0107 |      0.0027 |       0.008  |    0.0241 |      0.0401 |


Region key:

|    | Region                                      |
|---:|:--------------------------------------------|
|  1 | New England Division                        |
|  2 | Middle Atlantic                             |
|  3 | East North Central                          |
|  4 | West North Central                          |
|  5 | South Atlantic                              |
|  6 | West South Central                          |
|  7 | Mountain                                    |
|  8 | Pacific                                     |
|  9 | Virgin Islands, Puerto Rico, American Samoa |




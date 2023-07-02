---
title: "Running Back Regression Analysis in NFL Teams"
layout: post
---

  The data set that I have selected contains 26,600 entries of box scores of every NFL game starting from 2019 to the most recent NFL season. This dataset also contains statistics for offensive linemen such as offensive guards, tackles, and centers. It also has defensive players such as free safeties and cornerbacks. Therefore, the dataset contains countless advanced statistics that are more correlated with other skill positions. Since I was limiting my study to running backs and wide receivers only, most of the dimension reduction was done with selecting the subset of the data that had offensive skill positions, with the columns that had their workload and efficiency stats.
  The purpose of this report is to find reason for changes in running back (RB) performance on a season-to-season basis. After dimension reduction, my first step was to find how much their workload stats contributes to their efficiency. To do this, I made a correlation graph that drew rushing attempts and targets’ relationship with efficiency statistics such as rushing yards, touchdowns, receptions, yards per carry, etc.

![figure](/assets/Running Back Performance Stats Correlation.png)

  From this graph, you can clearly see that rush attempts and targets have a strong correlation with their respective efficiency stats. Rush attempts have strong correlations with rushing yards, rush longs, and rush yards after the catch. While targets almost have a 1:1 relationship with receptions (catches), reception yards, and reception yards after the catch. What I found peculiar about this graph is how relatively weak workload stats contributed to an RB’s touchdown total. Does it not make sense that the more carries and targets an RB gets, the more touchdowns they should have?

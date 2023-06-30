---
title: "Running Back Regression Analysis in NFL Teams"
layout: post
---

  The data set that I have selected contains 26,600 entries of box scores of every NFL game starting from 2019 to the most recent NFL season. This dataset also contains statistics for offensive linemen such as offensive guards, tackles, and centers. It also has defensive players such as free safeties and cornerbacks. Therefore, the dataset contains countless advanced statistics that are more correlated with other skill positions. Since I was limiting my study to running backs and wide receivers only, most of the dimension reduction was done with selecting the subset of the data that had offensive skill positions, with the columns that had their workload and efficiency stats.
  The purpose of this report is to find reason for changes in running back (RB) performance on a season-to-season basis. After dimension reduction, my first step was to find how much their workload stats contributes to their efficiency. To do this, I made a correlation graph that drew rushing attempts and targets’ relationship with efficiency statistics such as rushing yards, touchdowns, receptions, yards per carry, etc.

---
title: "Running Back Regression Analysis in NFL Teams"
layout: post
---

  The data set that I have selected contains 26,600 entries of box scores of every NFL game starting from 2019 to the most recent NFL season. This dataset also contains statistics for offensive linemen such as offensive guards, tackles, and centers. It also has defensive players such as free safeties and cornerbacks. Therefore, the dataset contains countless advanced statistics that are more correlated with other skill positions. Since I was limiting my study to running backs and wide receivers only, most of the dimension reduction was done with selecting the subset of the data that had offensive skill positions, with the columns that had their workload and efficiency stats.
  The purpose of this report is to find reason for changes in running back (RB) performance on a season-to-season basis. After dimension reduction, my first step was to find how much their workload stats contributes to their efficiency. To do this, I made a correlation graph that drew rushing attempts and targets’ relationship with efficiency statistics such as rushing yards, touchdowns, receptions, yards per carry, etc.

![figure](/assets/Running Back Performance Stats Correlation.png)

  From this graph, you can clearly see that rush attempts and targets have a strong correlation with their respective efficiency stats. Rush attempts have strong correlations with rushing yards, rush longs, and rush yards after the catch. While targets almost have a 1:1 relationship with receptions (catches), reception yards, and reception yards after the catch. What I found peculiar about this graph is how relatively weak workload stats contributed to an RB’s touchdown total. Does it not make sense that the more carries and targets an RB gets, the more touchdowns they should have?

![figure](/assets/workload_eff_rb_corr.png)

  Besides some outlier performances, no, it does not look like the more rush attempts you have, the more touchdowns you average. The ethical question does arise when considering most teams do only use 1-2 running backs throughout the season. The teams that consistently use 3 or more either had their RB1 injured or have a running back committee style offense. I could just limit my study to starting RBs, but I believe that would lead to a misrepresentation of efficiency statistics throughout the NFL. In the 2019-2020 season, out of 1690 total appearances, there were only 296 games where any running back scored at least 1 rushing touchdown in a game, which is 17% of running back performances. In those 296 games, running backs averaged at least 14 carries per game. That’s above the 75th quartile (11.75 carries) in rush attempts when considering
  RB performances in 2019-2020. For receiving statistics, the same kind of variation can be seen. Out of 1690 total appearances, there were only a whopping 101 games where any running back scored at least 1 reception touchdown, which is 5% of running back performances. Players who did score at least one receiving touchdown, averaged 4.3 targets per game, which is above the 75th quartile in target average for running backs in 2019-2020. This all speaks to the weak correlation that workload stats have with touchdown efficiency. Moving on to the strong correlations, I can make a conclusion that more rushing attempts and targets contribute to more yards.

![figure](/assets/target_td_corr.png)

  With this group of subplots, it is easier to see the strong relationship that carries have with rush yards, yards after catch, and long runs. Here are statistical tests that I performed in conjunction with the graph above.
• Carries to Rush Yards:
o Slope = 4.54, R-value = 0.89, P-value = 0.0
• Carries to Rushing Yards after the Catch:
o Slope = 2.19, R-value = 0.8, P-value = 0.0
• Carries to Long Runs:
o Slope = 1.02, R-value = 0.61, P-value = 0.0
• Carries to Rushing Touchdowns:
o Slope = 0.03, R-value = 0.48, P-value = 0.0
• Targets to Receptions:
o Slope = 0.78, R-value = 0.94, P-value = 0.0
• Targets to Reception Yards:
o Slope = 5.96, R-value = 0.79, P-value = 0.0
• Targets to Reception Yards after the Catch:
o Slope = 5.92, R-value = 0.80, P-value = 0.0
• Targets to Reception Touchdowns:
o Slope = 0.02, R-value = 0.25, P-value = 4.25
One more comment on touchdowns, I can see that the P-value for carries to rushing touchdowns suggests the rejection of the null hypothesis. On the other hand, the P-value for targets to receiving touchdowns strong suggests that there is no correlation, even when they share similar slopes. It makes sense since only 25% of running backs average over the 75th quartile in average targets from 2019-2023. However, every other statistical test does make the case that an RB’s production mostly boils down to how many yards can they push the ball down the field. From this point on, I felt comfortable to start making production profiles for individual running backs.
5

Based on the correlations that I found, would I be able to contextualize a player’s spikes, dips, and stability in their production? The first player whose profile I decided to make was Christian McCaffrey’s, currently of the San Francisco 49ers.

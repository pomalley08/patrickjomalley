---
title: Developing Sabermetrics
author: Patrick O'Malley
date: '2017-05-11'
slug: developing-sabermetrics
categories:
  - Personal Projects
tags:
  - R
autoThumbnailImage: false
thumbnailImagePosition: "top"
thumbnailImage: /images/baseball-750.jpg
coverImage: /images/baseball.jpg
metaAlignment: center
---

<!--more-->
## Problem Statement

Define new metrics specific to each position in baseball, and then compare each team's metric rankings against their actual 2016 ranking.

## Data

Data is from Stattleship and downloaded via their API. I am specifically looking at 2016 MLB regular season data.

## Methodology

14 unique positions are defined in the data and there are limited statistics available for each position. I will combine relevant stats for each position into a single position metric. The following graphs are an overview of some of the stats considered.  

Errors per game for both infielders and outfielders

![Errors](/img/errs.png)

OPS (On-base plus slugging) for all positions

![ops](/img/ops.png)

Multiple pitching stats are combined into single stat K+

![kplus](/img/kplus.png)

After creating the metrics, they are standardized and the relationships between stats are visualized. There is a positive relationship between the two pitching metrics: K+ and quality start rate.

![pitcher_metric](/img/pitcher_metric.png)

## Results

Finally the metrics are calculated for each player based on the 2016 season data. Teams are then built by selecting the highest scoring players per position that were on their roster in 2016.

Most teams are clustered around the average with the Chicago Cubs at the top at 0.564 and the Milwaukee Brewers at the bottom with 0.435.

![team_metric](/img/team_metric.png)

The final team comparison is shown below. The teams are listed in order of their 2016 win/loss record, while the color represents whether they over-performed (green) or under-performed (red) according to the calculated team metric.

![ranks](/img/ranks.png)

The metric performed reasonably well at the extremes with some surprises, but had more trouble on the teams in the middle of the table. This result makes sense since many teams were close to the average, and a small difference in the metrics could result in a large difference in the expected position.

Code used for this analysis can be found here: [GitHub Repo](https://github.com/pomalley08/Sabermetrics)

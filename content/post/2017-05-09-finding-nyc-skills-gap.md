---
title: Finding NYC Skills Gap
author: Patrick O'Malley
date: '2017-05-09'
slug: finding-nyc-skills-gap
categories:
  - Personal Projects
tags:
  - R
  - MySQL
  - Tableau
autoThumbnailImage: false
thumbnailImagePosition: "top"
thumbnailImage: /images/nyc-750.jpg
coverImage: /images/nyc.jpg
metaAlignment: center
coverMeta: out
---

This project is an Analysis of the Skills Gap in New York City

## Data Import

Data is provided by Burning Glass in a MySQL database, and will be imported into R for analysis and Tableau for additional visualizations

![erd](/img/erd.png)

## Data Exploration

New York metropolitan statistical area will be considered for analysis

![msa234](/img/MSA234.png)

The majority of job openings are in Manhattan

![jobs](/img/OpenJobs.png)

## Define Skills Gap Criteria

Considering job posting duration by itself is not a good metric since occupations with low number of posts can have extremely high average values

![postdur](/img/post_dur.png)

Looking at industries (as defined by occupation codes) with median posting duration > 15 days, and number of openings > 1000. Top industries are:  

1. Management
2. Healthcare
3. Computer and Math
4. Sales
5. Business and Finance
6. Office and Admin

![topind](/img/top_ind.png)

The top occupations within those industries as defined by number of records with high posting duration are shown in the chart below:

![topoccs](/img/top_occs.png)

## Qualities of Top Occupations

A look at the degree requirements for all of the top occupations. Bachelor's degree is required for 68.74% of the openings

![degrees](/img/degrees.png)

The following word cloud is a look at the most common skills required for the top occupations. Professional skills like communication and organization are the most commonly desired attributes

![skills](/img/skills.png)

Salary data is sparse in the data set, so filtering for it reduces the data points significantly. However there is enough to see expected trends like management and computer jobs having higher average salaries than office and administrative positions

![salary](/img/salary.png)

## Recommendations

The most notable insight of this analysis is to address the bachelor's degree requirement that the majority of these top occupations have. Funding should be directed to make college more accessible with programs like Pathways to Prosperity and the Early College Model

Code used for this analysis can be found here: [GitHub Repo](https://github.com/pomalley08/NYC_Skills_Gap)
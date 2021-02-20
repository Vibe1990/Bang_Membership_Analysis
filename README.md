# Membership Analysis of A Downtown Toronto Gym

This repository contains code and data used in the exploration of membership history of a boutique personal training studio in downtown Toronto of from both past and current members between the period of January 2018 to October 2020. 

---

## TABLE OF CONTENTS

* Overview
* Key Results
* Data Description 
* Technical Overview

---

## Overview

Since being hired as a member to the membership service team in 2017, membership churn is a common occurrence within a service-based industry such as the fitness industry.  While there is very little impact that I can do in terms of the actual service provided, our major roles comes from delivering stellar membership experiences.  Time and again, customer experience has been shown to be an important determinant factor in impacting business performance across multiple industries & across various demographics as noted [here](https://www.emerald.com/insight/content/doi/10.1108/IJQSS-01-2015-0008/full/html) and [here](https://www.pwc.com/us/en/advisory-services/publications/consumer-intelligence-series/pwc-consumer-intelligence-series-customer-experience.pdf#page=8).  This is especially true for boutique fitness studio where it is often an area of focus when contending with "big box/global" gyms, which often has been cited with [“less than satisfactory” customer experience](https://www.lbbonline.com/news/research-reveals-gyms-need-to-workout-their-customer-experience).

However, with the surplus of boutique fitness space in downtown Toronto, along with the impact of the COVID-19 pandemic that has significantly hampered [leisure-based industries and many others](https://www.spglobal.com/marketintelligence/en/news-insights/blog/industries-most-and-least-impacted-by-covid-19-from-a-probability-of-default-perspective-march-2020-update), there hasn’t been a more important time to get some introspection to see what needs to be done to come out of this situation as unscathed as possible.  The purpose of this project is to gain further insight into which sorts of factors play a significant role in contributing towards membership churn.  

## Key Results 

* Most common reasons for membership churn pertained to finance or lack of accessbility/availability (particularly noted in members in the tech-space, advertising/media or finance; scheduling-demanding fields)
* Attendance rates of less than 70% appears to be the cut-off point for a significant decreased odds of membership retention
* COVID pandemic significantly reduced clientele by 31% 
* Just having at least one single CX-related email interaction increased odds of membership retention across all 3 milestone points. However, any more than this doesn't appear to have as significant of an effect. 

## Data Description 

The compiled [dataset](CSM_Bang_no_names.csv) had been gathered through various sources that included:

   1) the scheduling/billing software [Wellnessliving](www.wellnessliving.com)
   2) our internal CSM [AirTable](www.airtable.com)
   3) email interactions (dating as far back as January 2012)
   4) one-on-one interactions with members
   5) Google Search 

| Factor Types | Variable | Description |
|------------|----------|-------------|
| Sociodemographic| age | member's age classification |
|                 |employment sector | member's area of employment |
| Membership History | start date | first ever date when they started their training at studio  |
|                    | end date  | last ever date when they were ever a member at studio|
|                    | length    | total cumulative days as a member | 
|                    | membership | predominant membership type as a member | 
|                    | # of membership change | number of times membership type changed in lifecycle |
|                    | retention status | retention status at 3-, 6- and 12- consecutive months |
|                    | current | current membership status as of (10-04-2020) | 
|                    | number of months | number of months as a member based on given membership type |
|                    | reason to leave | reason given for terminating membership (only for former members) | 
|                    | lifetime revenue | total lifetime value of member | 
|                    | membership rate |  weighted average of monthly dues across each membership type |
|                    | renewals        | number of membership renewals (per 66 day period) | 
|                    | pauses          | number of membership pauses | 
|                    | total sessions | theoretical total of possible sessions that can be attended| 
|                    | attended | number of total confirmed attended sessions |
|                    | cancelled | number of total confirmed cancelled sessions |
|                    | lost      | number of total sessions that were lost |
|                    | pending |  number of total sessions that I have no idea if member attended or not | 
| Email Interaction  | billing | number of email interactions based on billing-related issues |
|                    | service | number of email interactions based on service-related requests not related to scheduling |
|                    | scheduling | number of email interactions based on scheduling/rescheduling something |
|                    | CX | number of email interactions relating to improving membership experience / check-ins |

## Technical Overview 

* Data Exploration
* Data Cleaning & Handling Missing Data 
* Regression Analysis - Survival via Cox-Regression 
* Predictive Modelling - Logistic Regression & Random Forest 
* Model Evaluation 

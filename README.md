# An Analysis of US Wildfires

![Wildfire Image](https://github.com/bking3372/US-Wildfire-Analysis/blob/main/images/Wildfires4.jpg)
## Using Machine Learning to Classify Wildfire Causes

A web application for the visualizations and machine learning classification results for this analysis can be viewed here:  

### Background

An analysis was conducted on US wildfires that occured over a 24 year period to uncover trends in the data and build a model for classifying wildfire causes.  This data included 1.88 million geo-referenced wildfires occuring in the US between 1992 and 2015, representing a total of 140 million acres burned during this period.

Key data variables included:
-  Latitude and Longitude of the fire's point location
-  US State in which the fire occurred
-  Year the fire occurred
-  Discovery date: when the fire was discovered or confirmed to exist
-  Containment date:  when the fire was declared contained or controlled
-  Cause of the fire
-  Size of the fire (in acres)
-  Owner:  primary owner or entity responsible for managing the land at the point of origin of the fire (i.e., private vs federal/state land)


### Data Preprocessing

Prior to analysis, the data was preprocessed as follows:
- Extrameous variables were eliminated (i.e., reporting agency, fire name, etc.)
- Additional variables were calculated:
  -  Duration of the fire (containment date - discovery date)
  -  Month and day of week when the fire was discovered
- Null values were removed
- Categorical variables were dummy coded


### Exploratory Analysis

To better understand the data before starting the machine learning, an expoloration of the data was conducted in Tableau.  Key observations include:
- Wildfires in the US have been steadily increasing with the most common causes including debris burning, arson, and lightning.
- California, Georgia, and Texas have the most wildfires while the central part of the US, including the Great Lakes region, tend to have less.
- Wildfires are more likely to occur in Spring (March, April) and Summer (July, August) with Saturdays have slightly more wildfire occurrences than other days of the week.
- Most wildfires are less than 10 acres in size and are contained within one day.


### Machine Learning Classification

Machine learning was employed to determine if wildfires could be classified by how they were caused:
-  Naturally (i.e., lightning)
-  Accidentally (i.e., debris burning, campfires, fireworks, etc.)
-  Intentionally (i.e., arson)

Machine learning was conducted in several steps:
1. Step1: Classification was performed using the three causes described above (natural, accidental, intentional) along with miscellaneoous/unknown causes.  Four machine learning methods were used:  Random Forest, Decision Trees, Gradient Boosting and Naive Bayes.  The Random Forest classifier was the strongest with a

2. Step2:  The miscellaneous/unknown causes were removed to determine if better classification modeling could be achieved with the three core causes:  natural, accidental, and intentional.  Results improved significantly for both the Decision Tree and Gradient Boosting classifiers (Naive Bayes was not used given its poor results in the first step) yet Random Forest still did the best job of classifying among the three wildfire causes with a

3. Step3:  As a last step, machine learning was performed on each cause individually:  natural causes vs all other causes, accidental causes vs all other causes, and intentional causes vs all other causes.  Random Forest was used for each given its strong results in the prior machine learning steps.  Classification results were strongest for natural causes with a 

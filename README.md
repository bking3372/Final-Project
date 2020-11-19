# An Analysis of US Wildfires

![Wildfire Image](https://github.com/bking3372/US-Wildfire-Analysis/blob/main/images/Wildfires4.jpg)
## Using Machine Learning to Classify Wildfire Causes

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


**Data Preprocessing**

Prior to analysis, the data was preprocessed as follows:
- Extrameous variables were eliminated (i.e., reporting agency, fire name, etc.)
- Additional variables were calculated:
  -  Duration of the fire (containment date - discovery date)
  -  Month and day of week when the fire was discovered
- Null values were removed
- Categorical variables were dummy coded


**Exploratory Analysis**

To better understand the data before starting the machine learning, an expoloration of the data was conducted in Tableau.  Key observations include:


**Machien Learning Classification**

Machine learning was employed to determine if wildfires could be classified by how they were caused:
-  Naturally (i.e., lightning)
-  Accidentally (i.e., debris burning, campfires, fireworks, etc.)
-  Intentionally (i.e., arson)



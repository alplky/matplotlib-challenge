# matplotlib-challenge

## Background:

#### Pymaceuticals Inc. is a burgeoning pharmaceutical company based out of San Diego. Pymaceuticals specializes in anti-cancer pharmaceuticals. In its most recent efforts, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

#### In this study, 249 mice identified with SCC tumor growth were treated through a variety of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals' drug of interest, Capomulin, versus the other treatment regimens. 

## Data Cleaning:

#### Before beginning, the data was checked for any mice with duplicate timepoints. It was discovered mouse g989 had duplicate timepoints with tumor volumes that were different for each timepoint
 - The data was discovered by creating a data frame with Mouse ID and Timepoint columns and using duplicated.
 - Once it was discovered that the tumor volumes were not consistent for the duplicate timepoints, a cleaned dataframe was made by using df.drop with the duplicate Mouse ID. 
 
## Summary Statistics:

#### The summary statistics that were requested were the mean, median, variance, standard deviation, and standard error of the mean (SEM)
 - This was achieved by using the newly cleaned data frame, grouping by the Drug Regimen and using DataFrame.agg. 

## Bar and Pie Charts:

#### For both the bar and pie charts, two were made upon request - first using pandas, then using matplotlib. Both were identical in output. 
 - The bar chart shows the total number of mice for each treatment regimen throughout the study. This was created by grouping by the Drug Regimen and using nunique() on the Mouse ID. 

![Bar Plot](Images/total_mice.png)

 - The pie chart show the gender distribution of all mice in the study. This was created by grouping by Sex and using nunique() on the Mouse ID. 
 
![Pie Chart](Images/gender.png)

## Quartiles, Outliers, and Boxplots:
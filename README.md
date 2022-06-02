# EDA-MODEL
## AIM:
Explanation The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.

## ALGORITHM:
## STEP 1:
Import the required packages(pandas,numpy,seaborn).

## STEP 2:
Read the given .csv file.

## STEP 3:
Convert the file into a dataframe and get information of the data.

## STEP 4:
Remove the non numerical data columns using drop() method.

## STEP 5:
Replace the null values using (.fillna).

## STEP 6:
Returns object containing counts of unique values using (value_counts()).

## STEP 7:
Plot the counts in the form of Histogram or Bar Graph.

## STEP 8:
Find the pairwise correlation of all columns in the dataframe(.corr()).

## STEP 9:
Save the final data set into the file.

## CODE:
```
import pandas as pd
import numpy as np
import seaborn as sns
df=pd.read_csv("/content/Placement_Data (1).csv")
df.info()

df.head()

df.tail()

df.isnull().sum()

df["status"].value_counts()

df["gender"].value_counts()

df["specialisation"].value_counts()

sns.countplot(x="status",data=df)

sns.countplot(x="salary",data=df)

sns.countplot(x='hsc_s',data=df)

sns.countplot(x='degree_t',data=df)

sns.countplot(x="specialisation",hue="status",data=df)

pd.crosstab(df["specialisation"],df["salary"])

pd.crosstab(df["gender"],df["status"])

df.corr()

sns.heatmap(df.corr(),annot=True)
````

## outut:
## reading the file:
![ot1](https://user-images.githubusercontent.com/94233064/171548515-95848e70-b428-4bbd-9f3f-7115c4dd1b88.png)
![ot2](https://user-images.githubusercontent.com/94233064/171548602-10c43584-22e7-4993-98aa-7a38959fe1b7.png)
![tail](https://user-images.githubusercontent.com/94233064/171548622-240c0d34-5911-4048-86e5-54e4cd8d6dfc.png)
## checking the null values:
![isnullsum](https://user-images.githubusercontent.com/94233064/171548723-a134a8c4-98db-46da-a34c-4208366780d9.png)

## value count:
![status](https://user-images.githubusercontent.com/94233064/171548787-ce21baad-d1a8-4455-89fd-f398d5cee6aa.png)
![gender](https://user-images.githubusercontent.com/94233064/171548837-37506413-ea57-42dd-adca-b7cba3a2afa3.png)
![specialization](https://user-images.githubusercontent.com/94233064/171548871-0517f66f-1530-4c64-a200-ecfb58364c31.png)

## plotting the graph:
![ststus plot](https://user-images.githubusercontent.com/94233064/171548987-93122685-378c-4b87-9bf1-86b939b96e4f.png)
![salary plot](https://user-images.githubusercontent.com/94233064/171549055-3ac15b36-31ca-434a-9d9c-71985e48dd56.png)
![hscs plot](https://user-images.githubusercontent.com/94233064/171549076-cde5cb97-da7d-4bc9-8864-4d096f9d64fc.png)
![degree plot](https://user-images.githubusercontent.com/94233064/171549089-4f94cfa9-bb2e-44d4-b723-295f0daeda28.png)
 ![specsalary](https://user-images.githubusercontent.com/94233064/171549666-5cf219a2-1d46-4b86-8b23-77eda2ae29cb.png)
![gender status](https://user-images.githubusercontent.com/94233064/171549712-45d3751c-1eab-4a05-aaad-2d9b20a947c5.png)


## correlations:
![corr](https://user-images.githubusercontent.com/94233064/171549760-ed8bee11-4415-4eee-8900-9662bae67fca.png)

## heat map:
![heatmap](https://user-images.githubusercontent.com/94233064/171549818-1fd2ef6c-eaa3-471e-88c5-39e2b753e141.png)


## RESULT:
Thus the Exploratory Data Analysis (EDA) on the given data set is successfully completed.

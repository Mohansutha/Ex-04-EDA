## EX-04-EDA

## AIM:

To perform EDA on the given data set.

## EXPLANATION:

The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.

## ALGORITHM:

## STEP 1:

Import the required packages(pandas,numpy,seaborn).

## STEP 2:

Read the given .csv file.

## STEP 3:

Convert the file into a dataframe and get information of the 

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

~~~
import pandas as pd
import numpy as np
import seaborn as sns
df=pd.read_csv("supermarket.csv")
df.info()
df.head()
df.tail()
df.isnull().sum()
df["City"].value_counts()
df["Gender"].value_counts()
df["Payment"].value_counts()
sns.countplot(x="Invoice ID",data=df)
sns.countplot(x="Total",data=df)
sns.countplot(x='gross income',data=df)
sns.countplot(x='Payment',data=df)
sns.displot(df["cogs"])
sns.countplot(x="Gender",hue="Quantity",data=df)
sns.displot(df[df["Product line"]==0]["Total"])
pd.crosstab(df["Payment"],df["Quantity"])
pd.crosstab(df["Gender"],df["Quantity"])
df.corr()
sns.heatmap(df.corr(),annot=True)
~~~

## OUTPUT:

![1](https://user-images.githubusercontent.com/94828335/167987992-6f0f63ca-f160-472a-82a7-e21c2c7247f5.png)

![2](https://user-images.githubusercontent.com/94828335/167988019-f8cd98c8-9b8d-4fea-8460-75f9706c69f7.jpg)

![3](https://user-images.githubusercontent.com/94828335/167988044-a57814d8-8e30-4579-8b20-b92261ac8a3f.jpg)

![4](https://user-images.githubusercontent.com/94828335/167988076-55c7547d-a5b5-4c68-9cce-07b10b109518.png)

![5](https://user-images.githubusercontent.com/94828335/167988096-394cd14a-fb25-4a1a-877d-3210f381e78e.png)

![6](https://user-images.githubusercontent.com/94828335/167988124-be5fd1e3-e83c-48e0-9bc0-a1cb5fa308aa.jpg)

![7](https://user-images.githubusercontent.com/94828335/167988177-9f31f70b-6877-4f6c-9b9d-37d32ce487f2.jpg)

![8](https://user-images.githubusercontent.com/94828335/167988211-bf9fdec6-760b-4d61-8f09-b28e3e23cc0b.jpg)

![9](https://user-images.githubusercontent.com/94828335/167988230-c4196bff-508d-46d5-9076-e4ee925ba458.jpg)

![10](https://user-images.githubusercontent.com/94828335/167988296-5647385a-547e-4f1d-b549-d8ea4f609ab0.jpg)

![11](https://user-images.githubusercontent.com/94828335/167988309-0478a85a-922f-49ae-a71d-709982739652.jpg)

![12](https://user-images.githubusercontent.com/94828335/167988319-3d009211-4782-488d-8190-4bfcf50fe6e0.jpg)

![13](https://user-images.githubusercontent.com/94828335/167988337-0a0e2207-38e8-43f0-a7c8-e4e6693f88d7.jpg)

![14](https://user-images.githubusercontent.com/94828335/167988366-09e20175-a644-49cb-ba04-7f4a71d06d5c.jpg)

![15](https://user-images.githubusercontent.com/94828335/167988389-5073abff-9751-498c-b107-0a9a2bf4420e.jpg)


## Result:

Thus the Exploratory Data Analysis (EDA) on the given data set is successfully completed.
















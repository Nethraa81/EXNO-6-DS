# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:

```
 import pandas as pd
 import seaborn as sns
 import matplotlib.pyplot as plt
 df=pd.read_csv("titanic_dataset.csv")
 df.head()
```
<img width="764" height="150" alt="image" src="https://github.com/user-attachments/assets/c6395c9f-842a-4adf-ab15-21fb8824ad64" />

## LINE PLOT:
```
 x=[1,2,3,4,5]
 y=[3,6,2,7,1]
 sns.lineplot(x=x,y=y)
 plt.title('Line Plot')
```
<img width="425" height="359" alt="image" src="https://github.com/user-attachments/assets/b813efb5-a0ef-4b00-b9da-083c3e2e83c2" />


## MULTI LINE PLOT:
```
 x=[1,2,3,4,5]
 y1=[3,5,2,6,1]
 y2=[1,6,4,3,8]
 y3=[5,2,7,1,4]
 sns.lineplot(x=x,y=y1)
 sns.lineplot(x=x,y=y2)
 sns.lineplot(x=x,y=y3)
 plt.title('Multi Line Plot')
```
<img width="413" height="351" alt="image" src="https://github.com/user-attachments/assets/7842cda5-d4e4-4d9f-bdf3-2590038fc226" />

## BAR CHART:
```
 plt.figure(figsize=(8,5))
 sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
 plt.title("Fare Of Passenger By Embarked Town")
```

<img width="534" height="370" alt="image" src="https://github.com/user-attachments/assets/e83b487e-d2a6-4243-95d1-421b914407fe" />

## SCATTER PLOT:
```
sns.scatterplot(x="Age", y="Fare", data=df)
 plt.title('Scatterplot of Age vs Fare')
 plt.show()
```
<img width="441" height="341" alt="image" src="https://github.com/user-attachments/assets/e72035c9-abce-449d-896c-430f30ee068b" />


## BUBBLE CHART:
```
 sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
 plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
 plt.show()
```

<img width="456" height="345" alt="image" src="https://github.com/user-attachments/assets/e1090295-1e20-4c06-89b5-6896efa53d5a" />


## HISTOGRAM:
```
 sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="451" height="349" alt="image" src="https://github.com/user-attachments/assets/7f4d618d-8488-4bb8-8f96-bdf3af0b2df5" />

## BOX PLOT:
```
 sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
 plt.title("Age By Passenger Class")
```
<img width="428" height="362" alt="image" src="https://github.com/user-attachments/assets/6f9e8c01-1754-443e-84b4-04d90df66399" />

## VIOLIN PLOT:

```
 sns.violinplot(x="Pclass", y="Fare", data=df)
 plt.title('Violin Plot of Fare by Passenger Class')
 plt.show()
```

<img width="459" height="335" alt="image" src="https://github.com/user-attachments/assets/8f393e12-25d6-4d9f-974b-752e7bdf5f19" />

## DENSITY PLOT:

```
 sns.kdeplot(data=df['Age'], shade=True)
 plt.title('Density Plot of Passenger Ages')
 plt.show()
```

<img width="460" height="342" alt="image" src="https://github.com/user-attachments/assets/670f5aca-99c8-48d4-bac1-c0a3d575f6a1" />

## HEAT MAP:
```
 numeric_df = df.select_dtypes(include=['float64', 'int64'])
 corr_matrix = numeric_df.corr()
 sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
 plt.title('Heatmap of Titanic Dataset')
 plt.show()
```
<img width="475" height="382" alt="image" src="https://github.com/user-attachments/assets/06a9f8b7-b060-4a24-b4e1-26a4d8f63b1a" />


# Result:

 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully.

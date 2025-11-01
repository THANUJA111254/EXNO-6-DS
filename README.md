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

<img width="1573" height="274" alt="image" src="https://github.com/user-attachments/assets/f1bd11c2-620a-43ec-9491-415dcada705f" />

## 1.LINE PLOT:
```
 x=[1,2,3,4,5]
 y=[3,6,2,7,1]
 sns.lineplot(x=x,y=y)
 plt.title('Line Plot')
```

<img width="727" height="586" alt="image" src="https://github.com/user-attachments/assets/d4ccaa0d-aa0c-41f7-a0b4-3d913a125b38" />

## MULTILINE PLOT:
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

<img width="772" height="581" alt="image" src="https://github.com/user-attachments/assets/4b8ca9c3-116c-48a3-a24d-81970383a2f7" />

## BAR CHART:
```
 plt.figure(figsize=(8,5))
 sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
 plt.title("Fare Of Passenger By Embarked Town")
```

<img width="877" height="586" alt="image" src="https://github.com/user-attachments/assets/cdb56ee6-d511-4adb-93e2-49b9b8fab0d0" />

## SCATTER PLOT:
```
 sns.scatterplot(x="Age", y="Fare", data=df)
 plt.title('Scatterplot of Age vs Fare')
 plt.show()
```

<img width="765" height="574" alt="image" src="https://github.com/user-attachments/assets/7dfe319a-25ca-4fad-a0ba-0a723d87f953" />

## BUBBLE CHART:
```
 sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
 plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
 plt.show()
```

<img width="711" height="576" alt="image" src="https://github.com/user-attachments/assets/c41657b7-db83-45b8-985b-4a8a85b5aad9" />

## HISTOGRAM:
```
 sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

<img width="783" height="607" alt="image" src="https://github.com/user-attachments/assets/1e603b2b-f340-42b9-913e-233a3250cf86" />

## BOX PLOT:
```
 sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
 plt.title("Age By Passenger Class")
```

<img width="725" height="570" alt="image" src="https://github.com/user-attachments/assets/b64a43eb-9667-4231-b212-215755277435" />

## VIOLIN PLOT:
```
 sns.violinplot(x="Pclass", y="Fare", data=df)
 plt.title('Violin Plot of Fare by Passenger Class')
 plt.show()
```

<img width="795" height="590" alt="image" src="https://github.com/user-attachments/assets/9284bb6e-5685-4c6f-9547-921578c530e3" />

## DENSITY PLOT:
```
 sns.kdeplot(data=df['Age'], shade=True)
 plt.title('Density Plot of Passenger Ages')
 plt.show()
```

<img width="764" height="580" alt="image" src="https://github.com/user-attachments/assets/f45cf728-7156-46a6-ab9d-e6d1b35bc6e3" />

## HEAT MAP:
```
 numeric_df = df.select_dtypes(include=['float64', 'int64'])
 corr_matrix = numeric_df.corr()
 sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
 plt.title('Heatmap of Titanic Dataset')
 plt.show()
```

<img width="832" height="654" alt="image" src="https://github.com/user-attachments/assets/ec1c5c67-62a5-4d94-8f41-11c0397f08f5" />








# Result:
  Thus, the Data Visualization using seaborn python library for the given data is implemented successfully

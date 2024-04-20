# EX:6 DATA VISUALIZATION USING SEABORN LIBRARY

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
df=pd.read_csv("/content/titanic_dataset.csv")
df.head()
import seaborn as sns
import matplotlib.pyplot as plt
```
![6-0](https://github.com/Divya110205/EXNO-6-DS/assets/119404855/d83ea26b-0be7-42f2-ac05-23f7be976ac5)

### 1.Line Plot
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
![6-1](https://github.com/Divya110205/EXNO-6-DS/assets/119404855/f0d7d503-3f08-41e4-a2a0-4151ab5c2cb8)

### 2.Multi Line Plot
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
![6-2](https://github.com/Divya110205/EXNO-6-DS/assets/119404855/d4c830c1-17e2-4533-a5bf-9125b002c47b)

## TO VISUALIZE RELATIONSHIPS
### 1.Bar Chart
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
![6-3](https://github.com/Divya110205/EXNO-6-DS/assets/119404855/d8824a6e-d89e-4469-9aaf-74ee16c4e961)

### 2.Scatter Plot
```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
![6-4](https://github.com/Divya110205/EXNO-6-DS/assets/119404855/78b9ffbd-cc91-4f6a-b41a-c367b83062f7)

### 3.Bubble Chart
```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
![6-5](https://github.com/Divya110205/EXNO-6-DS/assets/119404855/bd9c1f59-b33b-4869-aa5a-0ee876a7c8ab)

## TO CAPTURE DISTRIBUTIONS
### 1.Histogram
```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![6-6](https://github.com/Divya110205/EXNO-6-DS/assets/119404855/bca9a8b5-ad6d-4488-89bc-8fe7fdcb4967)

### 2.Box Plot
```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
![6-7](https://github.com/Divya110205/EXNO-6-DS/assets/119404855/95bb6d12-2723-432d-a50a-6db241a68633)

### 3.Violin Plot
```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
![6-8](https://github.com/Divya110205/EXNO-6-DS/assets/119404855/a449378c-ebf5-416b-901c-3110875651ef)

### 4.Density Plot
```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
![6-9](https://github.com/Divya110205/EXNO-6-DS/assets/119404855/c2945da4-34fe-4526-8fcb-63df89686fe9)

### 5.Heatmap
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
![6-10](https://github.com/Divya110205/EXNO-6-DS/assets/119404855/e3abb871-9cba-4007-b9fd-03c5e007347d)

# Result:
  Thus, the Data Visualization using seaborn python library for the given data is implemented successfully

# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY
### NAME: ROHAN J
### REGISTER NUMBER: 212223040171
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
import seaborn as sns
import matplotlib.pyplot as plt
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```
![image](https://github.com/user-attachments/assets/be2fcd69-5a52-452b-b91c-5c4da7a61320)
```
df = sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/331f3df6-29f7-4add-ad30-529fddda568c)
```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle="solid",legend="auto")
```
![image](https://github.com/user-attachments/assets/e37c1597-0fb5-4213-bc20-37b682c8fc29)
```
x=[1, 2, 3, 4, 5]
y1=[3, 5, 2, 6, 1]
y2=[1, 6, 4, 3, 8]
y3=[5, 2, 7, 1, 4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")
```
![image](https://github.com/user-attachments/assets/74782241-db83-4261-9423-bd0f1f3123c7)
```
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip = tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![image](https://github.com/user-attachments/assets/7b52c5d5-6437-45c9-ba4a-3e178ab0b359)
```
avg_total_bill = tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
plt.xlabel('Time of Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Time of Day')
plt.legend()
```
![image](https://github.com/user-attachments/assets/aadeff86-569d-48e5-992e-480c6e20ecf1)
```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![image](https://github.com/user-attachments/assets/6c27779c-2167-4ca0-936a-30b4200ab7c5)
```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/user-attachments/assets/059bb70b-421d-4533-9689-8cd535445195)
```
import pandas as pd
tit=pd.read_csv("/content/titanic_dataset.csv")
tit
```
![image](https://github.com/user-attachments/assets/fdfbfe67-15b7-482a-bd9d-ab8af59f2942)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/user-attachments/assets/7ea411a4-0e23-46e6-8538-bb2ef3433496)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![image](https://github.com/user-attachments/assets/73107ab0-87a8-41a9-b439-e88012ed3339)
```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/user-attachments/assets/f7b14c65-d9d3-4578-b4cd-4268405c33e0)
```
import numpy as np
np.random.seed(1)
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/user-attachments/assets/e9758b6d-c9d8-4bad-8ea2-7ef8cecfce0a)
```
sns.histplot(data = num_var, kde = True)
```
![image](https://github.com/user-attachments/assets/1ee6dec9-effe-4fdd-9c90-29292dad10a3)
```
df=pd.read_csv("/content/titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![image](https://github.com/user-attachments/assets/26024556-018a-49ee-a585-265727f22924)
```
np.random.seed(0)
marks=np.random.normal(loc=70, scale=10, size=100)
marks
```
![image](https://github.com/user-attachments/assets/49fe380f-a0bf-4da7-a791-f04469abee97)
```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![image](https://github.com/user-attachments/assets/a4233b0d-90f1-4da1-8faa-097ad09934c9)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![image](https://github.com/user-attachments/assets/ac847a5d-1238-4283-a5fd-ce89524d052a)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/user-attachments/assets/fa15cced-36ad-437d-9a53-f07643b0e114)
```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![image](https://github.com/user-attachments/assets/c3d5caa4-1212-4919-92d7-93062a153c94)

```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![image](https://github.com/user-attachments/assets/0deabec3-5ca7-4d37-b234-5d1ef715a436)
```
sns.kdeplot(data=mart,x='PassengerId')
```
![image](https://github.com/user-attachments/assets/c3c6abc9-6447-4f5c-8736-67da644d0a10)
```
sns.kdeplot(data=mart,x='Age')
```
![image](https://github.com/user-attachments/assets/c79339b0-85da-496f-a7d0-2873ede562bb)
```
sns.kdeplot(data=mart)
```
![image](https://github.com/user-attachments/assets/9e0558c7-8e6a-4a8a-b432-637ac199f70d)
```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![image](https://github.com/user-attachments/assets/814d6e77-ab6c-4ced-90f7-54515bbee960)
```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![image](https://github.com/user-attachments/assets/b375e597-c1c9-40b3-9553-f9e125d8ff68)
```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/user-attachments/assets/f06afea2-e64d-4821-ac52-d7764ac23b8e)
```
hm=sns.heatmap(data=data)
```
![image](https://github.com/user-attachments/assets/e7695f7d-7356-4733-a2de-be42ce5b5526)

# Result:
Thus, all the data visualization techniques of seaborn has been implemented.


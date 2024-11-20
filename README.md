# EXNO6
# AIM:

To Analyze a data set with Various stages of data science.

# ALGORITHM:

Step 1: Choose your own dataset and read it.

Step 2: Include the necessary python Library.

Step 3: Perform Data Preprocessing steps for the necessary columns.

Step 4: Implement Data analysis using the necessary columns.

Step 5: Perform Feature Engineering process for the categorical columns.

Step 6: Implement Advanced data Visualization for the columns necessary.


# CODING AND SCREENSHOTS:
### NAME : MAMTHA I
### REG NO : 212222230076

```c
import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)

```

![327918503-1c8ab253-15f0-4b45-8caa-13ab87b620d0](https://github.com/user-attachments/assets/e7456437-95d8-46ae-9435-cd8e8197cc12)

```c
df=sns.load_dataset("tips")
df

```

![327918507-95a2ed6d-ef61-4344-be6d-175b073b5192](https://github.com/user-attachments/assets/ae50975e-8911-4378-b013-521ac17fa8e5)

```c

sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")

```


![327918510-99b1f75a-f56a-48fe-91c7-4b6d4cca4c62](https://github.com/user-attachments/assets/fcf5fc92-2e4a-4a6c-9571-5335a75426b8)

```c

x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title("Multi-line Plot")
plt.xlabel('X Label')
plt.ylabel('Y Label')

```

```c
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()


```

![327918517-fd7c2a3a-b168-44b2-8892-0ac6d388adf9](https://github.com/user-attachments/assets/f40e1946-e75c-4756-85f4-b25bdf19381a)

```c
avg_total_bill = tips.groupby('time')['total_bill'].mean()
avg_tip = tips.groupby('time')['tip'].mean()
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip', width=0.4)

plt.xlabel('Time of Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Time of Day')
plt.legend()

```

![327918524-5c9a4aca-7887-4bab-9bf7-a441a31ed425](https://github.com/user-attachments/assets/d875b361-25e3-432b-85cc-ba3d2a004589)

```c

years=range (2000, 2012)
apples = [0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)


```

![327918526-6fdee4e0-c832-43c3-9917-afff4e1375f8](https://github.com/user-attachments/assets/d9d245ba-9c58-4c4a-85c0-0ab4f62238c9)

```c
import seaborn as sns
dt= sns.load_dataset('tips')
# Bar plot with hue parameter
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')



```
![327918530-e9a48fc4-a932-4043-87ed-c46d30d52d7c](https://github.com/user-attachments/assets/cbfd1d42-6b55-44e0-9fef-608a0321ac0d)

```c
import seaborn as sns
# Load the tips dataset
tips = sns.load_dataset('tips')
# Scatter plot of total bill vs. tip amount
sns.scatterplot(x= 'total_bill', y='tip', hue='sex',data=tips)
# Set labels and title
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```

![327918533-3694fb1b-176a-4696-aa5d-c3b1fc7b4260](https://github.com/user-attachments/assets/8213a7a7-e894-41ad-bab7-d0c1c576efb0)

```c
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
np.random.seed(0)
marks = np.random.normal(loc=70, scale=10, size=100)
marks

```

![327918537-eee0727e-d897-4540-ae5a-83cb6f59b847](https://github.com/user-attachments/assets/0cd1dd2d-d549-45aa-953b-24aeef3049d5)

```c
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6,
palette="Set3", inner="quartile")
# Add labels and title
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")

```

![327918540-98fb5506-36c4-4824-bfdd-7b260a2a2752](https://github.com/user-attachments/assets/fd8389a0-7d28-4156-a86f-5b0ae59b4424)

```c
import seaborn as sns
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x ='day', y ='tip', data = tip)

```

![327918546-29596560-6a54-4051-9c55-0903af5c0665](https://github.com/user-attachments/assets/cfe97de2-becc-4d84-a87d-390d0c8fdfa2)


```c

import seaborn as sns
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"])

```

![327918551-7323ef13-38b2-472b-9146-e68f7f5049df](https://github.com/user-attachments/assets/043e093a-85cf-4fbb-98cb-1caa4c5ab2a2)

```c
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set2',alpha=0.8)


```

![327918553-322e04f2-b84b-4477-be92-23e22385feac](https://github.com/user-attachments/assets/2ad486c6-a831-4df9-a58c-170ebcbef6fa)

```c
sns.histplot(data=marks, bins=10, kde=True, stat='count', cumulative=False, multiple='stack', element='bars', palette='Set1', shrink=0.7)
plt.xlabel('Marks')
plt.ylabel('Density')
plt.title('Histogram of students Marks')

```

![327918565-b95a290d-8aa5-421b-910f-a8d05f0db533](https://github.com/user-attachments/assets/fd6af9c3-9e92-4364-9a1c-87fcc2abb91a)



![327918569-15ad7faa-d749-4ae6-8540-e56e79949db3](https://github.com/user-attachments/assets/55cdd424-3368-4ddf-a1d1-4c1889d8fd87)








# RESULT:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully

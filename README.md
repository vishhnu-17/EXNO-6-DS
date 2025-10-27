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
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
<img width="1136" height="310" alt="image" src="https://github.com/user-attachments/assets/014243ac-9953-4e29-aeae-81f2ca53aa86" />
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
<img width="1158" height="633" alt="image" src="https://github.com/user-attachments/assets/3e246136-aaa5-4ca0-a3ae-b5e77c1beef9" />
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
<img width="1123" height="670" alt="image" src="https://github.com/user-attachments/assets/4022d876-8aae-4ad9-93f7-40fcf0bf0132" />
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
<img width="1134" height="728" alt="image" src="https://github.com/user-attachments/assets/20d9fd53-9053-49d5-8c0c-144b4852bbd0" />
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
<img width="1157" height="616" alt="image" src="https://github.com/user-attachments/assets/d9263aaf-fe5d-49ee-a931-da7817b483e6" />
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
<img width="1131" height="620" alt="image" src="https://github.com/user-attachments/assets/8e7b32a0-c3bb-4bdd-86c4-5d5e685fcb56" />
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
<img width="1125" height="661" alt="image" src="https://github.com/user-attachments/assets/780f98a9-b86d-4408-86c9-14c4e3d124cb" />
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
<img width="1123" height="621" alt="image" src="https://github.com/user-attachments/assets/de205dd0-7414-4b2c-b5e7-98a897848359" />
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
<img width="1141" height="608" alt="image" src="https://github.com/user-attachments/assets/24862bb2-175e-4a7a-9720-a27dd4230b73" />
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
<img width="1136" height="688" alt="image" src="https://github.com/user-attachments/assets/c48fba99-f1cd-4f7d-b33f-61ccddd0c358" />
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
<img width="1128" height="656" alt="image" src="https://github.com/user-attachments/assets/99f694bd-bb36-4b7f-99de-8d0435af7ad8" />
# Result:
Thus, Feature selection and Feature scaling has been used on thegiven dataset.

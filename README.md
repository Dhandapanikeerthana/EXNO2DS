# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
```
import pandas as pd
df=pd.read_csv("titanic_dataset.csv")
print(df)

```
<img width="740" height="697" alt="Screenshot 2026-11-18 151105" src="https://github.com/user-attachments/assets/7a08280b-d7e9-4c25-afe4-7366ff8854ec" />

```
df.info()
```
<img width="505" height="345" alt="Screenshot 2026-11-18 151132" src="https://github.com/user-attachments/assets/d5134e89-d016-4d24-ba6b-451123d67047" />

```
df.describe()
```

<img width="692" height="300" alt="Screenshot 2026-11-18 151643" src="https://github.com/user-attachments/assets/076d1c54-ca64-489a-b6db-fe51659dd761" />

```
df.shape
```
<img width="497" height="73" alt="Screenshot 2026-11-18 151815" src="https://github.com/user-attachments/assets/7f562b9c-78e1-44e1-a615-2f792c53cf84" />
```
df.dtypes
```

<img width="451" height="498" alt="Screenshot 2026-11-18 151824" src="https://github.com/user-attachments/assets/257d1821-730d-4af7-8497-bfd3723658a8" />

```
df["Survived"].value_counts()
```
<img width="462" height="175" alt="Screenshot 2026-11-18 152059" src="https://github.com/user-attachments/assets/2074c39d-62fc-465f-9fb5-9a95e284731c" />

```
df.nunique()
```
<img width="287" height="447" alt="Screenshot 2026-11-18 152129" src="https://github.com/user-attachments/assets/4b723efd-6285-4d6d-9ac7-b0203955e0d0" />

```
import seaborn as sns
sns.countplot(data=df,x="Survived")
```
<img width="786" height="536" alt="Screenshot 2026-11-18 152218" src="https://github.com/user-attachments/assets/a263d450-d66f-425b-8ff0-4e2501598512" />

```
sns.boxplot(data=df, x="Age")
```
<img width="670" height="522" alt="image" src="https://github.com/user-attachments/assets/9608c48a-a0e4-4c69-baad-31c6f013114a" />

```
sns.histplot(data=df,x="Age")
```
<img width="682" height="522" alt="image" src="https://github.com/user-attachments/assets/88b9f864-c790-47e0-8020-2a8a637ddfae" />

```
df.rename(columns={'Sex':'Gender'},inplace=True)
print(df)
```
<img width="757" height="791" alt="image" src="https://github.com/user-attachments/assets/25fe1628-4f48-4cbd-93bd-172d5e38a986" />

```
sns.catplot(x='Survived',hue="Gender",data=df,kind='count')
```
<img width="677" height="577" alt="image" src="https://github.com/user-attachments/assets/b57d6b4e-6853-4f5c-a8ca-551024ea0b57" />

```
df.boxplot(column="Age",by="Survived")
```
<img width="643" height="541" alt="image" src="https://github.com/user-attachments/assets/5339a280-ec87-45a1-9122-9afa4a790d06" />

```
sns.scatterplot(x=df["Age"],y=df["Fare"])
```
<img width="650" height="511" alt="image" src="https://github.com/user-attachments/assets/6aec169d-8bbd-49b1-9590-1291197c06b1" />

```
sns.boxplot(x=df["Survived"],y=df["Fare"])
```
<img width="657" height="512" alt="image" src="https://github.com/user-attachments/assets/74a54f77-a8a8-46ea-8730-8c34d261997f" />

# RESULT
        <<INCLUDE YOUR RESULT HERE>>

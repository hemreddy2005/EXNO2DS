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

## Exploratory Data Analysis

```
import pandas as pd
import numpy as np
import seaborn as sns
df = pd.read_csv('/content/titanic_dataset.csv')
df
```

<img width="1104" height="368" alt="image" src="https://github.com/user-attachments/assets/4dd458cc-402c-4523-8bf1-6bc325c1c960" />

```
df.info()
```

<img width="535" height="312" alt="image" src="https://github.com/user-attachments/assets/1bdd63b4-93e5-4252-9c90-965e7d3db84a" />

```
df.describe()
```

<img width="711" height="269" alt="image" src="https://github.com/user-attachments/assets/bd8c6db6-8217-486f-97f2-57d49508cc18" />

```
df.dtypes
```

<img width="323" height="414" alt="image" src="https://github.com/user-attachments/assets/168c4f9d-3cfc-4f77-a141-010ac40bdfe4" />

```
df.shape
```

<img width="196" height="31" alt="image" src="https://github.com/user-attachments/assets/90869629-d00d-40b6-becc-740c742b768f" />

```
df.value_counts()
```

<img width="1216" height="445" alt="image" src="https://github.com/user-attachments/assets/1c20fb60-3fc9-49d2-a1f3-21cbd1c38b88" />

```
df.set_index('PassengerId', inplace=True)
df
```

<img width="1166" height="415" alt="image" src="https://github.com/user-attachments/assets/f1a2c439-d5dc-48b1-bdf4-7e7d453e6c6e" />

```
df.nunique()
```

<img width="283" height="386" alt="image" src="https://github.com/user-attachments/assets/c30a77d9-4537-4e43-9393-efd1c0f8df58" />

```
sns.countplot(data=df, x='Survived')
```

<img width="627" height="413" alt="image" src="https://github.com/user-attachments/assets/ff529ad4-f91a-420c-980b-ceb045703f7b" />

```
df.rename(columns={'Sex':'Gender'},inplace=True)
df
```

<img width="1157" height="411" alt="image" src="https://github.com/user-attachments/assets/ffe8c527-c678-4213-81ac-53aad53e7346" />

```
sns.catplot(x="Gender", col="Survived", kind="count",data=df)
```

<img width="978" height="471" alt="image" src="https://github.com/user-attachments/assets/e233d865-f1a9-4884-82ae-5b0e9604c29a" />

```
df.boxplot(column="Age",by="Survived")
```

<img width="639" height="440" alt="image" src="https://github.com/user-attachments/assets/db8b03c9-6d39-4f9a-8bd9-864d1af18372" />

```
sns.scatterplot(x=df["Age"],y=df["Fare"])
```

<img width="622" height="418" alt="image" src="https://github.com/user-attachments/assets/e83e200f-a501-4d4d-820a-3146e42909c9" />

```
plt=sns.boxplot(x='Pclass',y='Age',hue='Gender',data=df)
```

<img width="633" height="400" alt="image" src="https://github.com/user-attachments/assets/994a0616-c5ce-4395-a655-85073f03ab6e" />

```
sns.catplot(data=df,col="Survived",x="Gender",hue="Pclass",kind="count")
```

<img width="1082" height="469" alt="image" src="https://github.com/user-attachments/assets/832f9d3e-23ab-4a95-8299-1ebc8b2ab0c8" />

```
corr=df.corr(numeric_only=True)
sns.heatmap(corr,annot=True)
```

<img width="542" height="411" alt="image" src="https://github.com/user-attachments/assets/999438d9-a1ee-43f8-ac24-360a056669f7" />

# RESULT

Thus , The Programs are executed and Verified Successfully .

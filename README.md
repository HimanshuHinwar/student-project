# student-project
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
df = pd.read_csv(r"C:\Users\RAJNI PAL\Downloads\Diwali Sales 
Data.csv",encoding='latin1')
df.drop(["Status","unnamed1"],axis = 1, inplace = True)
df.dropna(inplace = True)
df["Amount"] = df["Amount"].astype("int")
ax = sns.countplot(x = "Gender",data = df,palette = ["blue","red"])
sales_gen = df.groupby(["Gender"],as_index = False)
["Amount"].sum().sort_values(by = "Amount",ascending = False)
 
sns.barplot(x = "Gender", y = "Amount", data = sales_gen)
<Axes: xlabel='Gender', ylabel='Amount'>
From above graphs we can conclude that 
female order more than men and have high 
purchasing power than men
count_age = sns.countplot(x = "Age Group", data = df,hue = "Gender")
sales_age = df.groupby(["Age Group"],as_index = False)
["Amount"].sum().sort_values(by = "Amount",ascending = False)
sns.barplot(x = "Age Group" ,y = "Amount", data = sales_age)
<Axes: xlabel='Age Group', ylabel='Amount'>
From above graph we can conlude that female 
under age bracket of 26-35 order more than 
other age brackets
count_states = sns.countplot(x = "State", data = df, width = 0.4)
sales_state = df.groupby(["State"],as_index = False)
["Amount"].sum().sort_values(by = "Amount",ascending = False)
sns.barplot(x = "State",y = "Amount", data = sales_state)
<Axes: xlabel='State', ylabel='Amount'>
From above graph we can conclude that 
Maharastra order more than other states but 
Uttar Pradesh spend more money
count_marital = sns.countplot(x = "Marital_Status",data = df,hue=
"Gender")
count_marital.set_xticklabels(["Married", "Non Married"])
#count_marital.set_xticklabels = (["Married","Non Married"])
[Text(0, 0, 'Married'), Text(1, 0, 'Non Married')]
sales_marital = df.groupby(["Marital_Status"],as_index = False)
["Amount"].sum().sort_values(by = "Amount",ascending = False)
sns.barplot(x = "Marital_Status",y = "Amount", data = sales_marital)
<Axes: xlabel='Marital_Status', ylabel='Amount'>
From above graph we can conlude that married 
people order more than unmarried people
count_occ = sns.countplot(x = "Occupation", data = df)
sales_occ = df.groupby(["Occupation"],as_index = False)
["Amount"].sum().sort_values(by = "Amount", ascending = False)
sns.barplot(x = "Occupation",y = "Amount", data = sales_occ)
<Axes: xlabel='Occupation', ylabel='Amount'>
From above graph we can conclude that most of
the customer comes from IT, Health and 
Aviation Industry
count_pro = sns.countplot(x = "Product_Category" , data = df)
sales_pro = df.groupby(["Product_Category"], as_index = False)
["Amount"].sum().sort_values(by = "Amount", ascending = False)
sns.barplot(x = "Product_Category",y = "Amount",data = sales_pro)
<Axes: xlabel='Product_Category', ylabel='Amount'>
From above graph we can conclude that 
customers order more cloths but spend more 
on food items
Conclusion
We can conclude that female married customers from 
Uttar Pradesh and Maharastra who works in IT, Health and 
Aviation Industry is our largest buyers

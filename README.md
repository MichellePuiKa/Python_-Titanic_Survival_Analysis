# Python_-Titanic_Survival_Analysis

## **1. Background and Overview**
The sinking of the Titanic remains one of the most infamous maritime disasters in history. This project aims to analyse the **Titanic dataset** to explore survival patterns based on different passenger attributes, such as class, gender, age and fare.
The goal of this analysis is to uncover key insights into survival rates and contributing factors using **Exploratory Data Analysis (EDA)** techniques.

## **2. Data Source & Structure**
### **2.1 Data Source**
This dataset was obtained from **[Kaggle – Titanic – Machine Learning from Disaster](https://www.kaggle.com/c/titanic/data?select=train.csv)**.
    
- **Dataset Used:** `train.csv `
- The  `test.csv ` and  `gender_submission.csv ` were **not used**, as this project focuses on **EDA rather than predictive modelling**


### **2.2 Data Structure **
The  `train.csv ` dataset contains of **891 passengers** with the following features:

| **Feature**          | **Description** |
|----------------------|----------------------------------------------------------------|
| **PassengerId** | Passenger Identity Number |
| **Survived** | Survival Status (1 = Survived, 0 = Died) |
| **Pclass**   | Passenger Class (1st, 2nd, 3rd) |
| **Name** | Passenger Name |
| **Sex**  | Passenger Gender |
| **Age** | Passenger Age |
| **SibSp** | Number of Siblings/Spouses Aboard |
| **Parch** | Number of Parents/Children Aboard |
| **Ticket** | Ticket Number |
| **Fare** | Ticket Price |
| **Cabin** | Cabin Number |
| **Embarked** | The Port Where the Passenger boarded the Titanic (C= Cherbourg, Q = Queenstown, S = Southampton) |


## **3. Data Processing & Cleaning**
**Handled Missing Values:**
-	 ‘Age ‘ and  ‘Fare ‘ columns had missing values, which were filled using the **median** to avoid skewing the data
-	‘Cabin ‘ had a high percentage of missing values.  Since it is **not critical** to this analysis, it was **retained as is** without imputation.

**Feature Engineering:**
-	**Grouped ‘Age’ into categories** (e.g. Baby, Child, Teenager, Adult, Senior) to analyse survival trends across different age groups
-	**Extracted Title** from the ‘Name’ column (e.g., Mr, Mrs, Miss, etc.) to analyse survival patterns based on social titles
-	**Created a Family Size feature** by combining ‘SibSp’ (siblings/spouses aboard) and ‘Parch’ (parents/children aboard)
-	**Converted ‘Sex’ into numerical format** (Male = 0, Female = 1) for correlation analysis 

## **4. Executive Summary & Key Findings**
This analysis focuses on four key questions:

**1. What is the overall survival rate?**
-	**38.4%** of passengers survived, while **61.6%** did not (visualized using a **pie chart**)
  
**2. How does survival vary by passenger class and fare?**
-	**1st class** passengers had a higher survival rate, while **3rd class** passengers had the lowest
-	Higher fares were generally associated with better survival odds (visualized using a **KDE**)
  
**3. How does survival vary by age and gender?**
-	**Females had a much higher survival rate** than males
-	**Children (aged ≤10)** had a better survival rate than adults
-	Visualized using a **stacked bar chart**, supplemented with a **data table** showing survival rates by gender and age group

**4. What are the correlations between Titanic dataset features?**
-	Survival is highly correlated with **Sex** and **Title**
-	**Fare has a moderate positive correlation** with survival
-	Family Size has little impact on survival
-	Visualized using a **correlation heatmap**



## **5. Insights Deep Dive**
**1. What is the overall survival rate?**

![Pie Chart]( https://github.com/MichellePuiKa/Python_-Titanic_Survival_Analysis/blob/main/Pie%20Chart.png)

**Overall Survival Rate:** A pie chart was used to show the overall survival rate of passengers, indicating the proportion of those who survived and those who did not. The chart clearly illustrates the disparity in survival, with fewer passengers surviving.



**2. How does survival vary by passenger class and fare?**

![KDE]( https://github.com/MichellePuiKa/Python_-Titanic_Survival_Analysis/blob/main/KDE.png)

A Kernel Density Estimate (KDE) plot was created to explore how survival rates vary by passenger class and fare. The analysis revealed that **survival rates were higher for 1st class passengers, with a positive correlation between higher fare prices and a greater likelihood of survival**.




**3. How does survival vary by age and gender?**

![Bar Chart_Table]( https://github.com/MichellePuiKa/Python_-Titanic_Survival_Analysis/blob/main/Stacked%20Bar%20Chart_Table.png)

A bar chart was generated to show the distribution of survival and death rates by age group and gender. This analysis highlighted that women had a significantly higher survival rate compared to men, with children also showing higher survival rates. Additionally, a table displaying the counts and percentages of survived and died passengers for both males and females was included to offer a clearer comparison between the two groups.




 **4. What are the correlations between Titanic dataset features?**
 
 ![Correlation_Heatmap]( https://github.com/MichellePuiKa/Python_-Titanic_Survival_Analysis/blob/main/Coorelation_Heatmap.png)
 
A correlation heatmap was generated to analyse the relationships between key features in the dataset. The heatmap revealed strong negative correlations between Pclass and Survived, suggesting that lower-class passengers were less likely to survive. A positive correlation between Fare and Survived was also observed, indicating that passengers who paid higher fares had a higher chance of survival.




## **5. Conclusion**
-	Prioritizing women and children during evacuations is critical, as seen from Titanic survival rates
-	Economic status (reflected in class & fare) significantly affects survival chances—future disaster protocols should ensure equitable rescue procedures across all passengers
-	More in-depth analysis could be done on ticket groups (e.g., were passengers with shared ticket numbers more likely to survive together?)


## **6. Recommendations**
-	Improved Evacuation Strategies: Future maritime safety policies should ensure fairer access to lifeboats for all classes
-	Better Safety Regulations: The clear survival gap between men and women suggests the need for more equitable safety measures
-	More Lifeboats & Preparedness: More lifeboats should have been available for all passengers, not just first-class ticket holders


## **7. Limitations**
-	**Limited Dataset:** The dataset includes only 891 passengers, not the entire Titanic manifest
-	**Missing Data:** Age and Cabin had many missing values, requiring imputation or removal
-	**Limited Features:** Additional factors like passenger health, physical strength, and group behaviour were not included
-	**Historical Bias:** The dataset reflects the early 1900s societal norms, which may not apply to modern disasters


## **💡 Connect & Feedback**
Have suggestions or feedback? Feel free to **open an issue**!  

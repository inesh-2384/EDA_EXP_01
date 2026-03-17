## Experiment 1: EDA in IPL Dataset

**Aim:**
To perform Exploratory Data Analysis (EDA) on the IPL matches dataset and derive insights about matches per season, winning teams, toss decisions, and top venues.

**Algorithm / Procedure:**

**1.Import Libraries**
  Import pandas for data handling.
  Import matplotlib and seaborn for visualization.
**2.Load Dataset**
  Use pd.read_csv() to load the IPL matches dataset.
  Check dataset shape using .shape.
  View first 5 rows using .head().
**3.Matches per Season (Univariate Analysis)**
  Group data by season and count matches.
  Plot a bar chart to visualize growth/decline in matches.
**4.Top Winning Teams (Univariate Analysis)**
  Use value_counts() on the winner column.
  Plot top 5 winning teams in a bar chart.
**5.Toss Decisions (Univariate Analysis)**
  Count toss decision preferences (bat vs field).
  Plot results using a bar chart.
**6.Top Venues (Univariate Analysis)**
  Count matches per venue.
  Display top 5 venues with a horizontal bar chart.
**7.Draw Insights**
  Observe patterns in toss decisions.
  Identify teams with consistent winning trends.
  
  **Program**
 ```py
 import pandas as pd
 import matplotlib.pyplot as plt
 import seaborn as sns
 matches = pd.read_csv("Dataset/matches.csv")
 print("Dataset Shape:", matches.shape)    
 print(matches.head())
 print("Dataset Shape:", matches.shape)    
 print(matches.head())
 plt.figure(figsize=(8,4))
 sns.barplot(x=season_counts.index, y=season_counts.values, palette="viridis")
 plt.title("Number of Matches per Season")
 plt.xlabel("Season")
 plt.ylabel("Matches")
 plt.show()
 team_wins = matches['winner'].value_counts()
 print("\nTop Winning Teams:\n", team_wins.head(5))
 plt.figure(figsize=(8,4))
 sns.barplot(x=team_wins.head(5).index, y=team_wins.head(5).values, palette="magma")
 plt.title("Top 5 Winning Teams")
 plt.xlabel("Team")
 plt.ylabel("Wins")
 plt.show()
 toss_decision = matches['toss_decision'].value_counts()
 print("\nToss Decisions:\n", toss_decision)
 plt.figure(figsize=(6,4))
 sns.barplot(x=toss_decision.index, y=toss_decision.values, palette="Set2")
 plt.title("Toss Decisions (Bat or Field)")
 plt.show()
 venue_counts = matches['venue'].value_counts().head(5)
 print("\nTop Venues:\n", venue_counts)
 plt.figure(figsize=(8,4))
 sns.barplot(y=venue_counts.index, x=venue_counts.values, palette="coolwarm")
 plt.title("Top 5 Venues by Matches Hosted")
 plt.xlabel("Matches Hosted")
 plt.ylabel("Venue")
 plt.show()
```
  **Output**

<img width="1920" height="1200" alt="Screenshot 2025-09-02 083346" src="https://github.com/user-attachments/assets/c6095ca1-e621-4961-af99-e9869e1e695d" />
<img width="1920" height="1200" alt="Screenshot 2025-09-02 083408" src="https://github.com/user-attachments/assets/1a9ec5e5-9f25-4a39-96f8-c644e4b9072c" />
<img width="1920" height="1200" alt="Screenshot 2025-09-02 083424" src="https://github.com/user-attachments/assets/6e6b69d6-d2c1-435e-9774-7f16a607644d" />
<img width="1920" height="1200" alt="Screenshot 2025-09-02 083435" src="https://github.com/user-attachments/assets/1cb5e6db-809e-4664-beb2-88fe2c0393e8" />
<img width="1920" height="1200" alt="Screenshot 2025-09-02 083447" src="https://github.com/user-attachments/assets/69c30750-7816-4d1f-aa74-e0c192ad7696" />
<img width="1920" height="1200" alt="Screenshot 2025-09-02 083459" src="https://github.com/user-attachments/assets/5fc9abdd-c443-4f08-b7bf-717b58172df6" />


 **Result**
  This experiment is executed successfully.



Highlight the stadiums hosting maximum matches.

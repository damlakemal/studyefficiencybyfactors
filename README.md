# Studying Efficiency / Productivity by Factors

## Abstract 

This project investigates how several factors in my life relate to and potentially affect my studying efficiency. I will collect daily data on my sleep schedule (sleeping and waking time), screen time (including most used apps and categories), caffeine intake (by mg), study location, total study duration, and a self-rated productivity score. Using this dataset, I will apply basic data analysis and statistical methods to explore the relationships between the variables and identify a pattern that may help my studying habits.

## Project Overview 

In this project i aim to analyze how some factors in my life change or affect my studying efficiency. I will record daily data of several factors like my **sleep schedule**, **screen time**, **caffeine intake** and my **study duration** as well as the **productivity score** of that study session. 

The main goal of this project is to analyze how different factors are associated with my study time and productivity.
By organizing and analyzing these data, I aim to:

- Understand which factors are strongly related with productive study sessions.
- Analyze how changes in these factors are reflected in my productivity.
- Use the results to find an **"optimal routine"** for my own study schedule.


## My Motivation 

As a student, I am constantly trying to improve my productivity and make better use of my time. I have always assumed that my sleep schedule, caffeine intake and my screentime influenced my productivity, but I never had concrete data to prove it.
In this project I aim to find how each factor affects my productivity. 
Ultimately, I hope to find the "optimal routine" to make the best and most productive studying periods. 


## Data Sources 

I will collect daily data using these sources: 

**Sleep Schedule**:

- Sleeping and waking up time recorded manually in a notes app, later transferred to a spreadsheet.
- Sleep quality based on my personal evaluation. I will give a score from 0 to 10 each day (0 being worst, 10 being best).

**Caffeine Intake**:

- I will record each caffeinated drink I drink in a day.
- Later, I will calculate the total amount of caffeine I took that they in mg.

**Screen Time**:

- I will record my screentime on all the devices I use, including my phone, computer, and tablet.
- I will collect data on the three most used apps everyday and how long I used them.
- I will also collect data on the three most used category everyday and how long I have them.

**Study**:

- I will record how long I study each day using my phone stopwatch.
- I will assign a personal productivity score from 0 to 10 (0 being the worst and 10 being the best) to each day, based on how productive and efficient my studying was.
- I will record the place I study at each day, since I figured how it affects my productivity.

## Methodology 

In this project I will follow these steps to prepeare and analyze my data: 

1. **Data Entry and Storage** 

   - I will record all the data daily in a notes app.
   - Later, I will transfer everything into a structured excel table. 
   
2. **Data Cleaning and Processing**

   - I will check missing values (e.g. days I forgot to record something), and fill it with -1 on the table.
   - I will convert all the time-related data into a consistent format.
   - From the raw data I will calculate:
       - Total sleep duration per day
       - Total study time per day
       - Total screen time per day and time spent in different categories / apps
       - Total caffeine intake per day 
  
3. **Tools and Environment**

   - I will use Python for the analysis:
     - "pandas" for reading, cleaning, and organizing the data
     - "matplotlib" for creating plots and visualizations
     - "numpy" for numerical operations

4. **Exploratory Data Analysis (EDA)**

   - I will create a correlation matrix to see which variables are related to each other.
   - I will look at basic statistics (mean, median, min, max, etc.) for each variable.
   - I will plot histograms, and boxplots to see how these values change over time.
  
5. **Hypothesis Testing and Evaluation**

   - Using the dataset, I will test the predefined hypotheses using:
     - Basic correlation analysis to see how variables are related 
     - Bar charts or boxplots to compare groups
     - Scatter plots to visualize relationships between two variables

## Hypotheses and Hypothesis Testing 

In this project, I will test how daily factors are related to my study productivity and efficiency. I will focus on the following hypotheses: 

1. **Sleep and Productivity**

   - **Hypothesis H1:** Sleeping between 7.5 to 9 hours per night is associated with high quality sleep and higher productivity scores.
   - **Testing:** Correlation (Pearson & Spearman) between sleep_hours and sleep quality, Correlation (Pearson & Spearman) between sleep_hours and productivity (Studying Efficiency), Group comparison: 7.5–9h vs outside for sleep quality and productivity (Welch t-test + Mann–Whitney)
  
2. **Studying Location**

   - **Hypothesis H2:** Studying at the Information Center results in higher productivity scores on average compared to any other location.
   - **Testing:** Compare productivity between place == "ic" and place != "ic" using Welch t-test and Mann–Whitney U.
     
3. **Study Duration**

   - **Hypothesis H3:** Studying for more than 4 hours in a day results in a higher productivity score compared to studying 4 hours or less.
   - **Testing:** Two-group comparison (study_hours > 4 vs study_hours ≤ 4) using Welch t-test and Mann–Whitney U at α = 0.05.
     
4. **Caffeine Intake and Productivity**

   - **Hypothesis H4:** Days with caffeine intake greater than 200 mg have higher productivity than days with 200 mg or less.
   - **Testing:** Two-group comparison (caffeine > 200 mg vs ≤ 200 mg) using Welch t-test and Mann–Whitney U (α = 0.05). Since the hypothesis is directional (“higher”), one-sided versions are also reported.
   


## Expected Findings

Based on my intuition and existing common beliefs about productivity, I expect to find: 

- A regular sleep schedule with healthy amount of sleep will **increase** my productivity.
- Studying at the Information Center will **increase** my productivity.
- Studiying longer than 5 hours that day will **increase** my productivity.
- Having little to no caffeine intake will **decrease** my productivity.
- Excessive screen time on non-productive apps will significantly **decrease** my study time and productivity.

  These expectations will be confirmed or denied based on the actual data analysis. 

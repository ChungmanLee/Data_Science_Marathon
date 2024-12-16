# COMP47670 Project 2 - Marathon
### Chungman Lee (23205535)

## Overview
In this project, we analyzed two marathon datasets (from 2008 and 2016), focusing on participants' finish times, pacing strategies, and factors such as age group, gender, and "hitting the wall." The data included split times at every 5 km and half-marathon checkpoints, allowing for detailed examination of performance patterns.

## Data Collection & Cleaning
- **Datasets (2008 & 2016)**: Each dataset contained runners' IDs, ranks, gender, age groups, and detailed split times (`z5`, `z10`, ..., `z40`, `halbmarathon`, `netto`, `brutto`).
- **Preprocessing Steps**:
  - Missing values were dropped, given their scarcity.
  - Time columns were converted to a timedelta format and subsequently into minutes.
  - Inconsistencies in age group and gender columns were filtered out.

## Exploratory Data Analysis (2008 Dataset)
1. **Descriptive Statistics**:
   - The finish times (netto) had a median slightly lower than the mean, indicating a right-skewed distribution.
   - The finish time range was large, and the standard deviation (~41 minutes) suggested a wide performance gap.

2. **Visualizations**:
   - **Histogram** of finish times showed a right-skewed distribution with a concentration of runners finishing between roughly 218 to 272 minutes.
   - **Box Plots**:
     - By Gender: Males generally finished faster than females.
     - By Age Group: Younger groups tended to have faster times; performance declined as age increased.

3. **Pacing and Half Marathon Times**:
   - Strong linear relationship between half-marathon times and overall finish times (R² ~0.90).
   - Negative splits (faster second half) correlated with better performance.

4. **Pacing Strategy Categorization**:
   - **Pacing Types**: Negative split, Even split, Positive split.
   - Negative splits dominated among faster runners, and top 1% (elite) athletes predominantly showed negative splits.
   - Women had a higher tendency toward negative splits compared to men.
   - Older age groups had fewer examples of negative splits, but still, negative/consistent pacing tended to correlate with better outcomes.

5. **Hitting the Wall**:
   - Defined as the second half marathon taking significantly longer (e.g., >1.3 times first half).
   - Slower finishing groups had a higher incidence of "hitting the wall."
   - Women and older runners were less likely to hit the wall, though they might generally run at a steadier but slower pace.

## Analysis for the 2016 Dataset
- Similar patterns emerged:
  - Right-skewed finish time distribution.
  - Males generally faster than females; younger age groups performed better.
  - The linear regression between half-marathon and finish times also showed a strong positive correlation (R² ~0.89, slope similar to 2008 data).

## Key Findings
- **Gender Differences**: Men are generally faster, but women tend to pace more evenly, resulting in fewer instances of hitting the wall.
- **Age Impact**: Younger runners are faster. Older participants run slower but more consistently, hitting the wall less often.
- **Pacing Strategies**:
  - Negative splits correlate strongly with better performance and are a hallmark of elite runners.
  - Positive splits often lead to slower finish times and more instances of hitting the wall.

## Conclusions and Insights
Both in 2008 and 2016:
- Strong linear relationship between half-marathon splits and final finish times.
- The distribution and overall patterns remained consistent, suggesting stable trends in marathon performance over the years.
- Understanding pacing strategies offers valuable insights into endurance running: stable pacing (negative or even) aligns with better outcomes, while a poorly managed second half frequently leads to hitting the wall.

In sum, effective pacing, indicated by negative or even splits, correlates with stronger performance. Age and gender differences also influence pacing choices and outcomes. These findings can guide runners and coaches to focus on balanced pacing strategies for improved results.

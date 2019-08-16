# Visualization of relationship between ​chronic diseases and preventions in 500 US Cities​


## Description
This project created an interactive visualization to show the most prevalent
diseases in the 500 largest cities in the US, the factors that most contribute to those
poor health outcomes and their prevalence within the cities. We base our analysis on
data provided by the Centers for Disease Control and Prevention (CDC).

We developed machine learning models to predict the health outcomes and deduce
the most important contributing factors. These factors are ranked by the strength of
their relationship to each disease. We find that support vector regression (SVR)
performs the best in terms of predicting health outcome prevalence; therefore, we use
SVR to produce the final ranking for visualization.

While current research focuses on a single factor-disease pair, we will study
the relationship between 13 diseases and 14 factors (9 preventions and 5
unhealthy behaviors). 

The full report is available here: [Report](/ProjectReport.pdf)

The project poster is available here: [Poster](/ProjectPoster.pdf)

## Visualizations

Four interactive visualiations were created to enable users to review. The interactive versions can be viewed here: [Tableau Public Link](https://public.tableau.com/profile/myles.lefkovitz#!/vizhome/500_Cities_Visualizations/Story)

#### Health Outcomes and Related Factors

This is the main interface showing our
analysis result. User can select the nation, a state, or a city and see the top
diseases in that area.

For each disease, a bar chart shows the five most strongly related factors
(calculated at the state or national level where available) as identified in the
analysis and identifies the prevalence of each factor (prevention/unhealthy
behavior) and the outcome (disease).

![Health Outcomes Bar Chart](./Images/Health%20Outcomes%20and%20Related%20Factors%20Bar%20Charts.png)

#### Interactive Health Information Map

- A map at the city level displaying 500 circles across the US (one for each city in the data set).
- For each city the circle is colored categorically in line with the most prevalent outcome or the prevention most closely related to the most prevalent outcome.
- When hovering over a circle relevant prevalence details are displayed.
- When clicking on a circle the bar charts from the figure above are displayed for that city.

![Interactive Health Information](./Images/Interactive%20Health%20Information.png)

#### Outcome Prevalence Map

A map of 500 cities comparing the prevalence of the selected outcome.

![Selected Outcome Prevalence](./Images/Outcome%20Prevalence.png)

#### 4.	Top Prevention by Selected Outcome

A map that shows the most relevant prevention for the selected outcome for each city.

![Top Prevention by Selected Outcome](./Images/Top%20Prevention%20by%20Selected%20Outcome.png)


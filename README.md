# Visualization of relationships between ​chronic diseases and preventions in 500 US Cities​


### Description
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

### Experiment

Our analysis identifies the relationships that exist between (1) preventions and unhealthy behaviors and (2) health outcomes. For each of the 13 health outcomes identified in the CDC 500 Cities dataset, we ran an experiment to identify the most relevant factors (preventions / unhealthy behaviors) at national and state levels. 

Data is provided at the census tract levels for 13 health outcomes, 9 preventions and 5 unhealthy behaviors. Data is analyzed both nationally and at state level using census tract data. The data is first split 70% for training and 30% for testing. The selected tool for machine learning / regression is the Python library Scikit-Learn.

A comparison of the four different regression algorithms – Linear, Ridge, Lasso Regression and Support Vector Regression (SVR) - was carried out both for the nation and for each of the states across the 13 health outcomes. The train and test scores suggest that generally SVR produce the highest prediction accuracy among the selected models for different health outcomes. 

With the finding that the best-performing algorithm is SVR, we embarked on using it with our remaining experiments for top-feature analysis reporting. Top Feature Selection Analysis, the user is prompted for the number of top features, after which SVR is automatically run at both national level and for all states. After two hours of processing, it creates two output files containing national and state analyses, with training scores, test scores, and the top features. The figure below shows the output for national level data for the top five features.  Depending on the health outcome, test scores range between 0.8251 and 0.9345 with a mean of 0.8893, confirming that the regression model provides a good fit and that the data has a linear relationship.  The top preventions / unhealthy behaviors are then identified and ranked for each health outcome in order to establish links.  

![Support Vector Regression Results](./Images/Support%20Vector%20Regression%20Results%20with%20Top%20Features%20at%20National%20Level.png)

### Visualizations

Four interactive visualiations were created to enable users to review. The interactive versions can be viewed here: [Tableau Public Link](https://public.tableau.com/profile/myles.lefkovitz#!/vizhome/500_Cities_Visualizations/Story)

**Health Outcomes and Related Factors**

This is the main interface showing our
analysis result. User can select the nation, a state, or a city and see the top
diseases in that area.

For each disease, a bar chart shows the five most strongly related factors
(calculated at the state or national level where available) as identified in the
analysis and identifies the prevalence of each factor (prevention/unhealthy
behavior) and the outcome (disease).

![Health Outcomes Bar Chart](./Images/Health%20Outcomes%20and%20Related%20Factors%20Bar%20Charts.png)

**Interactive Health Information Map**

- A map at the city level displaying 500 circles across the US (one for each city in the data set).
- For each city the circle is colored categorically in line with the most prevalent outcome or the prevention most closely related to the most prevalent outcome.
- When hovering over a circle relevant prevalence details are displayed.
- When clicking on a circle the bar charts from the figure above are displayed for that city.

![Interactive Health Information](./Images/Interactive%20Health%20Information.png)

**Outcome Prevalence Map**

A map of 500 cities comparing the prevalence of the selected outcome.

![Selected Outcome Prevalence](./Images/Outcome%20Prevalence.png)

**Top Prevention by Selected Outcome**

A map that shows the most relevant prevention for the selected outcome for each city.

![Top Prevention by Selected Outcome](./Images/Top%20Prevention%20by%20Selected%20Outcome.png)

### Conclusions

Our analysis shows that for each one of the 13 health outcomes, there is a linear relationship with at least some of the preventions and unhealthy behaviors – we have chosen to rank the top five.  This is true both at the national level and across each of the 50 states.   The visualization allows users to explore the analysis results for their geographic areas of interest. Users can see the most widespread diseases in an area, what unhealthy behaviors and preventions are most related to those diseases. They can also utilize the prevalence map to quickly compare prevalence of those diseases and factors across all cities.
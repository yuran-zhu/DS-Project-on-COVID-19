# DS-Project-on-COVID-19
Exploring and Analyzing COVID-19 Confirmed Cases Growth and Hospital Capacity

This project explores pressing questions related to COVID-19. Currently, the United States is under intense pressure from the disease, with swiftly growing cases and high demand for medical resources. We use data on case statistics and hospitalization capacity, aiming to predict the case growth trend and hopitalization, including whether hospital capacity will be reached in certain locations.

## Data Summary
### Data source
- COVID-19 case data: from Johns Hopkins CSSE at https://github.com/CSSEGISandData/COVID-19 (up to April, 29, 2020)
- US hospital capacity data: from Harvard Global Health Institute at https://globalepidemics.org/our- data/hospital-capacity/
- High risk data: from the Dartmouth Institute at https://www.dartmouthatlas.org/covid-19/ (high risk is defined as age 65 and older with two or more chronic conditions)
- Hospitalization data: from the COVID Tracking Project, which is a volunteer organization organized by The Atlantic that publishes COVID-19 data. https://covidtracking.com. The data is broken up by state.
- HRR: from the Dartmouth Atlas Project project: https://www.dartmouthatlas.org/covid-19/hrr- mapping/. The Hospital Referral Regions are in a lot of the coronavirus data sets and are bigger regions than just counties, but much smaller than states.

## Graphical Summary
### Overview for nationwide
Using US map data, we first visualize US confirmed and death cases by states. It’s clear that New York, New Jersey, Massachusetts, Illinois, and California are the five states undergoing the most severe pressure. We also generate visuals by counties, and it turns out that counties located in the North West seem to have fewer cases. Here, one county has missing data: Shanno, South Dakota (fips code 46113).

### Focus: California
We selected one representative state, California, as the focus to further visualize and build the model on. From the plot of Califonia’s confirmed cases, large discrepancies can be found. It’s clear that Los Angeles is the most hard hit county in the whole state. After starting slowly in early March, the virus has now been spreading swiftly since late March.

To further explore the infectious conditions for different counties, plots are displayed based on California counties. The top 10 counties with the highest numbers case numbers are labelled. The following table summarizes those regions, with the population of the county also indicated. We can see that the hardest hit counties tend to have higher populations, likely due to the population density facilitating transmission throughout the communities.

We also find the following 4 counties haven’t report any confirmed cases. Of note, those counties have lower populations than most other counties in California. Meanwhile, we calculate the confirmed proportion of county population. It allows us to observe the infectious pattern more comprehensively, in combining case number and case rate. The figure below shows top 10 counties in California with the highest confirmed proportion.


## Methodology
As for the data analytics part, we mainly investigate two questions:
- How does the case growth trend develop, and when will it possibly reach a steady state?
- As the viral infection continues to develop fast, will we reach the hospitalization capacity in certain states or regions in the near future?

### Logistic Growth Model
The logistic growth model has been widely used to model population growth with limited resources and space. It can be used in epidemiology, to analyze pandemic dynamics, with a cumulative number of confirmed cases or deaths. The logistic growth model corresponds to the SI model in epidemic studies (S for Susceptible, I for Infectious). As now the primary method to control the pandemic in US is stay at home orders, we could use the logistic growth model to in the case of COVID-19 outbreak.


## Conclusion and Discussion

The US has been deeply affected by the COVID-19 outbreak in terms of public health, the economy and many other aspects. Therefore, the predictions related to this epidemic disease is topical and aims to help policymakers determine approprate measures in advance. The project uses logistic growth model in predicting the confirmed cases in the near future. The results indicate that number of confirmed cases in US will continue increasing until late June and Early July. However, the model is based on the assumption of limited space and resources. If the current stay at home order is lifted earlier, it may take longer time to reach a steady state or hospital capacity will be exceeded.

In addition to using logistic modeling to predict the end of the COVID-19 outbreaks across the US, we also investigated hospital capacity. By implementing stay at home orders and thereby lowering the capacity in the model (“flattening the curve”), most states are well within their capacity in terms of potential number of hospitalizations. We did see that Louisiana may exceed their ICU capacity if everyone that is hospitalized with COVID-19 needs intensive care and no other people need intensive care. However, most COVID patients will not need intensive care, and because of flattening the curve states are well-equipped to deal with the hospital burdens. Overall, modeling is an effective planning tool for dealing with pandemics and pandemic response. They can help policymakers understand the effects of certain policies and help them prepare for potential shortfalls in various locations.

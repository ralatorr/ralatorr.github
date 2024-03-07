# Ricardo Alatorre | Data Scientist | Chicago Booth MBA

## About Me

My name is Ricardo Alatorre, and I am a native of Monterrey, Nuevo León, México, where I've lived most of my life. I've also spent portions of my life in the United States, first as a college student in New York City, then as a business school student and senior program manager in Chicago. A committed student of mathematics, I've taken steps to develop my skills in quantitative modeling throughout the course of my career and have recently decided to pivot into data science, completing General Assembly's Data Science Immersive program in February 2023. I'm currently searching for data scientist roles in technology, energy, and retail.

Outside of work, I spend most of my leisure time cooking, gardening, and reading. I find that all three activities serve to put me at ease, cooking in particular. Lately I've been focsuing on preparing large quantities of curry over the weekends to give me something warm to eat on winter weekdays. When it comes to reading, I'm currently working my way through Lincoln in the Bardo, by George Saunders.

I do my best to maintain an active lifestyle, and generally make sure I run 6 miles at a time a few times a week. I hope to be going back to the gym to lift more consistently very soon as well.

### Educational Background
- General Assembly
  - Certificate, Data Science Immersive  
- University of Chicago Booth School of Business
  - M.B.A. (Econometrics & Statistics, Operations Management, and Analytic Finance)
- Columbia College, Columbia University
  - B.A. (Mathematics)  

### Professional Background / CV

I am a quantitative analyst with 6 years of experience spanning different roles in management consulting, renewable energy business development, and tech program management.

A PDF copy of my resume can be found here: [Ricardo Alatorre's Resume (PDF)](https://github.com/ralatorr/ralatorr.github.io/blob/main/Resume/Ricardo_Alatorre_Resume_2023.pdf).

## Project Portfolio
### NLP Reddit Classification
#### Overview
Taking advantage of the Pushshift Reddit API, we pulled thousands of posts from the r/NHL and r/NBA subreddits. With this data in hand, we set out to leverage NLP methods in order to create models that would take in a given Reddit post as an input and predict whether the post came from r/NHL or r/NBA.

#### Conclusions

After performing some data cleaning and EDA, we found that roughly half of all submissions did not have bodies of text to process, although there was plenty of text data in submission titles that aided our modeling. Thus, we combined both the titles and bodies of text of each submission before they were vectorized through TfidfVectorizer. This way, each post whose body lived entirely within its title was properly processed.

Once the text data had been processed and vectorized, three models were tested, with the following results:
Model (Train Score, Test Score)

    - Logistic Regression (97.6%, 94.2%)
        - LR, GridSearch (99%, 94.7%)
    - k-Nearest Neighbors (53%, 51%)
        - kNN, GridSearch (100%, 55%)
    - Random Forest (96.1%, 92.4%)
        - RF, Gridsearch (96.2, 91.0%)
    
Our most successful model turned out to be Logistic Regression under GridSearch, sporting the following classification metrics:

     - Accuracy (94.8%): Percentage of obsservations the model correctly predicted.
     - Misclassification Rate (5.2%): Percentage of observations the model incorrectly predicted.
     - Sensitivity (96.5%): Rate of True Positives vs All Positives (r/NHL)
     - Specificity (93.1%): Rate of True Negatives vs All Negatives (r/NBA)
     - Precision (93.4%): Rate of True Positives vs Predicted Positives (r/NHL)


#### Link to Project
[NLP Reddit Classification](https://github.com/ralatorr/ralatorr.github.io/tree/main/Reddit_Classification)

### California Health Outcomes
#### Overview
Pollution has long been known to have a causal effect on negative health outcomes. Our group's goal was to use various statistical hypothesis tests as well as exploratory data analysis and regression analysis to gain a stronger quantitative understanding of the effects of air pollution amongst the 58 counties of California.

#### Conclusions

1. Fine air particulate matter (PM 2.5)  had a statistically significant influence on deaths from heart disease, cancer and respiratory illnesses in the most polluted counties in California from 1999-2021. 
2. Time-series analysis allowed us to predict statewide cancer incidence rates for a handful of cancer types with MAPE rates at roughly 1.5%, with PM2.5, NO2 and Ozone often driving increases in incidence rates, but results should be taken with a grain of salt - aggregated data involved merely 20 year-by-year observations.

#### Link to Project
[California Health Outcomes](https://github.com/ralatorr/ralatorr.github.io/tree/main/Health_Outcomes)

### Energy Demand and Price Forecasting
#### Overview

In 2013, the government of Mexico opened up the energy industry to private and foreign investment. In the time since, a private market for energy has emerged. We set out to see if we could build models that reliably predict energy demand and price in the Mexican Wholesale Energy Market (real-time), focusing on the author's hometown of Monterrey, Nuevo Leon, Mexico.

All energy demand, generation, and price data was pulled from APIs and databases that Mexico's National Center for Energy Control (CENACE) maintains. Weather data corresponding to Monterrey, Mexico was also pulled from the OpenWeatherAPI on the intuition that weather can drive energy demand.

When it came to CENACE's energy price and demand data, we selected weighted price data corresponding to the region on the Mexican National Grid that Monterrey is in, as well as data on aggregate demand for energy within that region. When it came to generation, we got our hands on generation data at the national level, on the understanding that this generation all goes into the same grid. All generation, demand, and price data covers the period from 2019-2022 inclusive. So does the weather data. 

#### Conclusions

We tested a variety of different models, including linear regression, random forest regressors, ARIMAX, among others.
We settled on a Random Forest Regressor model to predict energy prices. Our model predicted energy prices by MWh within 300 MXN or so.
When it came to predicting energy demand, we developed a Long Short Term-Memory model, a kind of Recurrent Neural Network (RNN) that allows us to engage in time-series forecasting. This model's predictions had an average Mean Absolute Percentage Error roughly 2x that of the Mexican federal government's own demand forecasts. Given the LTSM model merely took in univariate time series data (i.e. energy demand across time), the development of a similar multivariate model seems promising.

#### Link to Project
[Energy Demand and Price Forecasting](https://github.com/ralatorr/ralatorr.github.io/tree/main/Energy_Forecasting)

## Contact
If you'd like to reach out, I can be contacted via:
- email: [ralatorr@alumni.chicagobooth.edu](ralatorr@alumni.chicagobooth.edu)
- LinkedIn: [https://www.linkedin.com/in/ricardoalatorre/](https://www.linkedin.com/in/ricardoalatorre/)


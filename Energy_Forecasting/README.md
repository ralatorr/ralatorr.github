### Energy Demand and Price Forecasting
#### Overview

In 2013, the government of Mexico opened up the energy industry to private and foreign investment. In the time since, a private market for energy has emerged. We set out to see if we could build models that reliably predict energy demand and price in the Mexican Wholesale Energy Market (real-time), focusing on the author's hometown of Monterrey, Nuevo Leon, Mexico.

All energy demand, generation, and price data was pulled from APIs and databases that Mexico's National Center for Energy Control (CENACE) maintains. Weather data corresponding to Monterrey, Mexico was also pulled from the OpenWeatherAPI on the intuition that weather can drive energy demand.

When it came to CENACE's energy price and demand data, we selected weighted price data corresponding to the region on the Mexican National Grid that Monterrey is in, as well as data on aggregate demand for energy within that region. When it came to generation, we got our hands on generation data at the national level, on the understanding that this generation all goes into the same grid. All generation, demand, and price data covers the period from 2019-2022 inclusive. So does the weather data. 

#### Conclusions

We tested a variety of different models, including linear regression, random forest regressors, ARIMAX, among others.
We settled on a Random Forest Regressor model to predict energy prices. Our model predicted energy prices by MWh within 300 MXN or so.
When it came to predicting energy demand, we developed a Long Short Term-Memory model, a kind of Recurrent Neural Network (RNN) that allows us to engage in time-series forecasting. This model's predictions had an average Mean Absolute Percentage Error roughly 2x that of the Mexican federal government's own demand forecasts. Given the LTSM model merely took in univariate time series data (i.e. energy demand across time), the development of a similar multivariate model seems promising.

<h1> Energy Consumption - Time Series Forecasting </h1>

Data: A time series containing weekly information for electricity consumption in the East Region of the United States
<a href="https://www.kaggle.com/datasets/robikscube/hourly-energy-consumption"> Source: PJM Interconnection LLC (PJM) is a regional transmission organization (RTO) in the United States </a>

<h2> Steps: </h2>

<h3>1) Data Overview</h3>

![ts1](https://github.com/Pollybs/energy_consumption_time_series/blob/main/plots/energy_use_graph.png)

<h3>2) Statistical analysis of time series data using Python</h3>

Checking for stationarity, unit root, seasonality, trend, and autocorrelation

a) stationarity &  unit root

Results of KPSS Test:
Test Statistic             1.176234
p-value                    0.010000

Results of Dickey-Fuller Test:
Test Statistic                -1.882891e+01
p-value                        2.022125e-30

Conclusion: ADF does not find a unit root; but KPSS claims that it is non-stationary. Then, the series is difference stationary. 

(at least one of the tests claims to have found non-stationarity, differencing must be used.)

b) Seasonality and trend (STL): 

![ts2](https://github.com/Pollybs/energy_consumption_time_series/blob/main/plots/stl.png)

![ts5](https://github.com/Pollybs/energy_consumption_time_series/blob/main/plots/mw_hour.png)

![ts3](https://github.com/Pollybs/energy_consumption_time_series/blob/main/plots/mw_day_week.png)

![ts4](https://github.com/Pollybs/energy_consumption_time_series/blob/main/plots/mw_month.png)

Kendall's tau: -0.04791052695148664
P-value: 2.801793697350987e-165
There is a significant trend in the time series.



# Forecasting COVID-19 cases using SARS-CoV-2 Titers in Urban Wastewater

### Motivation:

Since the start of the SARS-CoV-2 (COVID-19) pandemic, an accurate count of cases in the community is tracked by symptomatically and clinically diagnosed cases. 
This method has inherent drawback as many of the patients do not report the disease and/or maybe asymptomatic.
Studies have shown proof of gastro-intestinal disorders triggered by SARS-CoV-2 infections in patients and the occurrence of viral RNA in community wastewater plants. 
Wastewater-based epidemiological surveillance can be used as an early warning system for disease outbreak and to forecast the rate of transmission in communities.
We intend to explore the relationship between SARS-CoV-2 titers in urban wastewater and the rate of infections in nearby communities and design models to forecast the rate of infections using titer information as proxy data (a.k.a Nowcasting).

### Models Implemented:

Given the strong linear relationship between the titer average values and the confirmed daily case count average values, we suspected that linear regression models would work best for this problem. We have explored the use of the following models for forecasting daily case count:

**Naive Model**
We develop a baseline persistence model for evaluating performance of other models. This model uses the case count values from previous day (t-1) to predict the values for the current day (t). 

**Linear and Polynomial Regression**
We evaluate the use of simple linear and regression models solved using Ordinary Least-Squares. 

**Generalized Linear Models**
We suspect piece-wise linear models like GAMs might tend to work better than simple linear models, we develop such a model using Penalized B-Splines.

**Gradient Boosting Regression**

**Recurrent Neural Networks**
Since our time series data is sequential, we explore the use of recurrent neural networks such as **Gated Recurrent Units, LSTM with and without BiDirectional Layers** to create deep neural networks.


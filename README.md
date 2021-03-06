# Time series Forecasting

This git gathers my work during a 2-month internship with the Centre for Health Data Science of the University of Aberdeen. 
The objective of this project was to propose a simple R code that would allow forecasting on time series data, for example related to COVID-19 numbers.

To illustrate the method that I implemented to achieve this objective, I work on the dataset provided by the COVID Tracker Project, ([covidtracking.com](https://covidtracking.com/data)).
This dataset presents COVID-19 related data, for each state of the US, such as number of deaths, hospitalizations, positive tests along time.
For different methods, I have thus been able to train models on data of every state, and propose a robust evaluation of each of them, computing errors on my predictions.
The details of my code is presented on the `report.Rmd` markdown, while the resulting graphed are stored in the `outputs` directory. This document presents all the methodology that I followed to implement forecasting models and evaluate them.

Beside it, I also created a markdown which aims to make people able to use my code and adapt it to their own datasets. In this `forecasting.Rmd` document, the forecasting method used is the exponential smoothing, because this is the one that produced the best results during my experiments. This method should produce satisfactory results on datasets similar to the one that I used for tests.

The final chosen method may not be the best we could find. I started training MLP models that can be more complex and difficult to tune properly. It sill might be a good idea to go further in this direction and try to improve results.

Finally, another option worth exploring would be models based on external inputs, not only on the evolution of data along time. I could just start thinking of this kind of solution, implementing a multi variable linear regression, taking into account the evolution of positive cases. The fitted model obtained is presented by the following graph:

![Linear regression](Rplot.png)

This shows that such ideas would be worth being explored. We indeed can imagine of various relevant external inputs. In our case, such methods could also allow us to evaluate the efficiency of a lockdown, if we add this information to our model and check the evolution of hospitalizations.

# Applied Data Science Capstone Project

## The Problem and the Goal

Road accidents, unfortunately, happened frequently and they can lead to severe consequences. Reducing the number of road accidents, especially the severe ones, is especially important to make people's lives better. Appreciating the inherent randomness of these events, I am trying to understand the deterministic factors in these tragic incidents. For instance, one might intuitively speculate the conditions of the vehicles should be relevant, and the drivers with poorly conditioned cars might be more likely to get involved in accidents.

In order to concretely understand what factors might be important, I am going to use statistical methods to find the correlations between different attributes of the car accidents, and then I will try to build a probabilistic model (i.e. machine learning model) to predict the severity of the car accidents, basing on the highly correlated factors. The final model is expected to help the law makers to propose more effective regulations to reduce the number of severe road accidents.

## Description of the data

I used the data from website [kaggle](https://www.kaggle.com/tsiaras/uk-road-safety-accidents-and-vehicles?select=Accident_Information.csv), which contains the detailed information about traffic accidents across the country from 2004 to 2016.

The dataset contains two tables (`.csv` files). One of them is related to the accidents alone and another is related to the vehicles. The same entry in the two tables is identified by its unique accident ID.

There are 55 features in total for each accidental event, such as `Number_of_Casualties`, `Carriageway_Hazards`, and `Vehicle_Manoeuvre`. The label to be predicted is the `Accident_Severity`, which is categorised into 3 classes `Fatal`, `Serious` and `Slight`. Since there are orders in these categories (`Fatal` > `Serious` > `Slight`) so it is possible to convert them into numbers, and study the numerical correlations between features and the result. The very relevant features will be used to build the model, and the model is expected to be able to predict the accident severities.

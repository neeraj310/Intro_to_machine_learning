# DLfM Group Project: Brand Management
Authors:<br>
Neeraj Kumar<br>
Saiteja Pottanigari<br>


## Problem statement
Predict class of Economic losses caused by Forest Fires using SVM, Random Forest, MLP and Logistics regression. Economic losses have been categorized into 3 classes: 0, 1, 2 and we want to predict the output class based on the dataset features. As Forest fires effects economics loss of any country in the world, building a model which takes features of forest fires and predicting how much it will effect the economic and let the government be ready for the range of impact either it is high or medium or low.

## Multiclass Problem
As it is a multiclass problem with output label holding 3 classes(0, 1, 2). We can take 2 approaches for solving this problem

## One Vs Rest (One Vs All)
Here we use mulitple binary classifer which is compare each class with rest of the classes available being one label. Decision rule:Predict class label with the highest probability. Requires n classifiers if n number of classes exist.

## One Vs One
In this we have to train binary classifier for each class pair. Decision rule:Score for output a data item towards one class, combines all classifier's probability involving this class in the class pairs. Requires nC2 classfiers if n number of classes exist.

For current problem, we are choosing One Vs Rest approach because of two reasons a) Dataset is limited (500 samples) so we want to use all samples for each classifier. b) Number of classes are limited to 3, so number of classifiers will be same in both cases.

# Brief Description of Dataset

## FOREST FIRES DATASET
Dataset description: The data is compiled from forest fires classified according to the economic losses that they caused. There are thirteen different features associated with each fire. The goal is to predict the economic losses range (feature "class") from the other features.

Number of samples: 500
Number of features: 13 (numeric and strings) + one column of class labels (0,1,2)
Features description:
    fwi: Fire weather index
    humidity: Absolute humidity in g/m3
    region: region
    dc: Drought code
    wind: Average wind speed in km/h
    month: Month of the year at start
    area: Burned area in km2
    rain: Outside rain in mm/m2
    nr_firefighters: Number of firefighters employed per day
    severity_rating: severity_rating
    temperature: Temperature in Celsius degree
    fire_id: Fire ID
    duration: Month till extinguishment
    class: Economic losses (0 = low, 1 = medium, 2 = high) <--- LABEL TO PREDICT



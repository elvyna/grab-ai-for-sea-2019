# grab-ai-for-sea-2019
Submission for Grab AI for SEA 2019, traffic management problem (https://www.aiforsea.com/traffic-management)


In this challenge, participants are to build a model trained on a historical demand dataset, that can forecast demand on a Hold-out test dataset. The model should be able to accurately forecast ahead by T+1 to T+5 time intervals (where each interval is 15-min) given all data up to time T.

The given dataset contains normalised historical demand of a city, aggregated spatiotemporally within geohashes and over 15 minute intervals. The dataset spans over a two month period. A brief description of the dataset fields are found below:

geohash6:
Geohash is a public domain geocoding system which encodes a geographic location into a short string of letters and digits with arbitrary precision. You may use the Python Geohash package https://pypi.org/project/Geohash/ or any Java Geohash library https://github.com/kungfoo/geohash-java or similar to encode and decode geohash into latitude and longitude and vice versa.
day: value indicates the sequential order and not a particular day of the month
timestamp: start time of 15-minute intervals, in the following format: :, where hour ranges from 0 to 23 and minute is either one of (0, 15, 30, 45)
demand: aggregated demand normalised to be in the range [0,1]
Model performance determines how a model represents the data and how well the chosen model will work. In this challenge, we will be performing a Hold-out model evaluation. For this problem, you are given a training dataset, and our evaluators will have a test dataset (not seen by the model). This test dataset will assess the likely future performance of the model.

The test dataset will cover a time period of 14 consecutive days. Submissions will be evaluated by RMSE (root mean squared error) averaged over all geohash6, 15-minute-bucket pairs.

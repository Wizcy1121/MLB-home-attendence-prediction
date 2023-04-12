# MLB-home-attendence-prediction

# Business Problem
<img width="956" alt="image" src="https://user-images.githubusercontent.com/92591719/231561203-4120b213-1cd5-4140-8d75-cb24bd5d05bd.png">

# Solution Map
<img width="812" alt="image" src="https://user-images.githubusercontent.com/92591719/231561421-7c1f9e6c-8370-4ea7-889e-30a48e7faff8.png">

## 1. How to use data to make informed decision for long term strategies
--》**Pre-Season Attendance Prediction Model**
**1. Data features**
Team performance: 
Home Team/Visiting Team:
  · Season end rank,
  · Season end Win/Loss ratio,
  · Total # of runs scored/allowed
Players
Home Team/Visiting Team:
  · # of all star players in team,
  · # of top 10 players in team,
  · Previous season MVP in team
Calendar
  · Year, month,
  · Weekday number, 
  · Holidays

**2. Model strategy**
Temporal Fusion Transformer
<img width="524" alt="image" src="https://user-images.githubusercontent.com/92591719/231563045-3a8cd90b-5b0d-44e4-b017-b7ebcfc77beb.png">
advantages:
· Take into account the impact of all the historical data when forecasting time series
· Capable of processing multiple heterogeneous time series data simultaneously
· Achieve high performance across multi-time period forecasting




# Capstone 3 : Bike-Sharing System Analysis

Bike-sharing systems represent a modern evolution of traditional bike rentals, where the entire process—from membership registration to bike rental and return—is automated. These systems allow users to conveniently rent a bike from one location and return it at another. Currently, there are over 500 bike-sharing programs globally, comprising more than 500,000 bicycles. These systems have garnered significant attention due to their contributions to traffic reduction, environmental sustainability, and public health.

Beyond their practical real-world applications, bike-sharing systems generate rich datasets that are valuable for research. Unlike other forms of public transportation such as buses or subways, bike-sharing systems record precise travel durations, departure points, and arrival locations. This turns each system into a virtual sensor network capable of tracking mobility patterns across urban areas. By analyzing this data, it is possible to detect major urban events and shifts in population movement.

## Goals
Goal
The challenge is not just transportation—it’s uncovering patterns, predicting demand, and turning mobility data into actionable insights that drive smarter urban decisions.

## Dataset Features
- dteday: Date of the observation
- season: Season indicator (1: Winter, 2: Spring, 3: Summer, 4: Fall)
- hr: Hour of the day (0 to 23)
- holiday: Indicates whether the day is a holiday
- temp: Normalized temperature in Celsius, calculated as (t - t_min) / (t_max - t_min), with t_min = -8°C and t_max = 39°C
- atemp: Normalized "feels like" temperature in Celsius, calculated as (t - t_min) / (t_max - t_min), with t_min = -16°C and t_max = 50°C
- hum: Normalized humidity (value between 0 and 1, where 1 = 100%)
- casual: Number of casual (non-registered) users
- registered: Number of registered users
- cnt: Total number of bike rentals (casual + registered)
- weathersit: Categorical weather situation:
  1: Clear, Few Clouds, Partly Cloudy
  2: Mist, Mist + Cloudy, Mist + Broken Clouds
  3: Light Snow, Light Rain + Thunderstorm + Scattered Clouds
  4: Heavy Rain + Ice Pellets + Thunderstorm + Mist, Snow + Fog

## Conclusion
The CatBoostRegressor model demonstrated superior performance with an R² of 0.9368, indicating that it explained 94% of the variance in the target variable. It achieved low error values (MAE: 18.77, RMSE: 30.48, MAPE: 23.52%), confirming its reliability and generalizability. Key features such as hour and week categories significantly influenced predictions. However, the model performs best on values ≤350, and care should be taken when predicting higher ranges.

##Recommendations
1. Focus on Time-Based Features
Features like hour_category, hour_sin, and week_category play a critical role in prediction. It is recommended to integrate time-awareness into decision-making processes for better alignment with demand patterns.

2. Monitor High-Value Predictions Carefully
The model shows reduced accuracy for predicted rental counts over 350. These outputs should be validated before being used in high-stakes decisions.

3. Adopt CatBoost for Production
With its excellent accuracy (R² ≈ 0.93) and robust generalization, the CatBoost model is well-suited for operational deployment to predict bike rental volume.

4. Operational Efficiency: Reduce Cost
With MAE of 18.77, the model helps allocate resources more precisely (fleet, staff, etc.).
- Prevents overstaffing or equipment overuse.
- Helps avoid missed opportunities due to underestimation.
- Enables data-driven scheduling of work shifts and maintenance.

5. Service Optimization: Boost Revenue
- Use dynamic pricing based on time to improve profit margins.
- Target discounts or campaigns to low-demand hours to increase utilization.
- Design services aligned with peak usage patterns.
- Optimize fleet distribution—reduce idle time and enhance customer experience.

# Capstone 3 : Bike-Sharing System Analysis

Bike-sharing systems represent a modern evolution of traditional bike rentals, where the entire process—from membership registration to bike rental and return—is automated. These systems allow users to conveniently rent a bike from one location and return it at another. Currently, there are over 500 bike-sharing programs globally, comprising more than 500,000 bicycles. These systems have garnered significant attention due to their contributions to traffic reduction, environmental sustainability, and public health.

Beyond their practical real-world applications, bike-sharing systems generate rich datasets that are valuable for research. Unlike other forms of public transportation such as buses or subways, bike-sharing systems record precise travel durations, departure points, and arrival locations. This turns each system into a virtual sensor network capable of tracking mobility patterns across urban areas. By analyzing this data, it is possible to detect major urban events and shifts in population movement.

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

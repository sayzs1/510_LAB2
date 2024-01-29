# TECHIN 510 Lab 2

scraping information and Use API for TECHIN 510 Lab 2.

## How to Run
Open the `visitsestille.ipynb` and run each cell

## What's Included
- `events.csv`: The event information scrape from website
- `events_with_coordinates.csv`: The event information and each event's latitude and longitude data
- `events_weather_forecast.csv`: The weather information for each event
## Lessons Learned
- How to find special selector to scrape information from one website
  - May become invalid quickly with website changes
  - Pay attention to how often requests.get(url), and remember to use sleep() to avoid harming the site
- How to deal with real place names to get latitude and longitude information
  - Some place name search location+region will not find information, we need to search one of name  to get the information
- Categorize to handle different date types
  - If the date includes now through, determine whether the following period is within the next seven days. If so, take tomorrow's weather forecast
  - If date 1 passes through date 2, determine whether the two periods are within the next seven days, and if so, take the weather forecast for that date
  - Write unknown for an ongoing adn past event
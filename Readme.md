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
- Categorize to handle different date types
  - If the date includes now through, determine whether the following period is within the next seven days. If so, take tomorrow's weather forecast
  - If date 1 passes through date 2, determine whether the two periods are within the next seven days, and if so, take the weather forecast for that date
  - Write unknown for an ongoing adn past event

## Questiones
- How to Deploy the scraper on GitHub Actions?
  - first create the `scraper.py `file in repository, then click 'Actions', in the detailed action page, click 'set up a workflow yourself' then choose configuration. We can create periodically git actions in the `.github/workflows/actions.yml `file. 
  - for example: 
  ```
  on:
  schedule:
    - cron: '*/15 * * * *' # Run every 15 minutes
  ```

- How to find the special selector to scrape information from the website?
  - We can select the information first and then click inspect and in the terminal, click 'copy' - 'copy selector'
- How to deal with real place names to get latitude and longitude information
  - Some place name search location+region will not find information, we need to search one of name to get the information, for example try only search location name without region to get the information, if it doesn't work then try only search the region name and get the information.
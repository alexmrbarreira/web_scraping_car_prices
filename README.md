# car_website_scraping
Simple set of python scripts that gather data from car websites and plots a few car properties together. Useful to rapidly browse available car offers and visualize market trends.

### Dependencies

- numpy and matplotlib
- pandas
- bs4 - python web scraping library

### Table of contents
- [Running the scripts](#running-the-scripts)
- [Results overview I : different cars, same country](#results-overview-I--different-cars,-same-country)
- [Results overview II : different countries, same car](#results-overview-II--different-countries,-same-car)

### Running the scripts
There are two sets of scripts: (i) one for offers in Germany from autoscout24.de and (ii) another for offers in Portugal from standvirtual.com. Their use is similar.

To get and plot data from autoscout24.de (German offers) simply:
- choose search car options in *parameters_de.py*. Check existing examples; to add more check brand/model names in autoscout24.de.
- run *python scrape_autoscout24_de.py*. This will generate data tables in *data_store_de/*.
- run *python plot_data_de.py*. This will make a plot with key car data; the figure is saved in *fig_store_de/*.

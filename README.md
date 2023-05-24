# car_website_scraping
Simple set of python scripts that gather data from car websites and plot a few car properties together. Useful to rapidly browse available car offers and visualize market trends.

### Table of contents
- [Dependencies](#dependencies)
- [Running the scripts](#running-the-scripts)
- [Results overview for different cars, same country](#results-overview-for-different-cars-same-country)
- [Results overview for different countries, same car](#results-overview-for-different-countries-same-car)

### Dependencies

- numpy and matplotlib
- pandas
- bs4 - python web scraping library
- firefox browser (optional)

### Running the scripts
There are two sets of scripts: (i) one for offers in Germany from autoscout24.de and (ii) another for offers in Portugal from standvirtual.com. Their use is similar.

To get and plot data from autoscout24.de (German offers):
- choose search car options in *parameters_de.py*. Check existing examples; to add more check brand/model names in autoscout24.de.
- run *python scrape_autoscout24_de.py*. This saves a car data table in *data_store_de/*.
- run *python plot_data_de.py*. This makes a plot with key car data; the figure is saved in *fig_store_de/*. It also prints the URLs of selected car properties for closer inspection at the website. If *open_URL=True* (which can be selected inside the file), it will direcly open the selected URLs with firefox.

To get and plot data from standvirtual.com (Portuguese):
- choose search car options in *parameters_pt.py*. Check existing examples; to add more check brand/model names in standvirtual.com
- run *python scrape_standvirtual_pt.py*. This saves a car data table in *data_store_pt/*.
- run *python plot_data_pt.py*. This makes a plot with key car data; the figure is saved in *fig_store_pt/*. It also prints the URLs of selected car properties for closer inspection at the website.  If *open_URL=True* (which can be selected inside the file), it will direcly open the selected URLs with firefox.

### Results overview for different cars same country
This figure plots the data for Volkswagen Golf (Variant submodel, *body_type='kombi'*) from autoscout24.de (Germany).

![](./fig_store_de/fig_2016_kombi_volkswagen_golf.png)

This figure plots the data for Audi A4 (Avant submodel, *body_type='kombi'*) from autoscout24.de (Germany).

![](./fig_store_de/fig_2016_kombi_audi_a4.png)

The black dashed lines draw of box of target maximum price and kilometers. As expected, there are far less Audi A4 than Volkswagen Golf in the selected range.

### Results overview for different countries same car
These two figures plot the data from Volkswagen Golf-Variant from autoscout24.de (Germany) and standvirtual.com (Portugal).

![](./fig_store_de/fig_2016_kombi_volkswagen_golf.png)
![](./fig_store_pt/fig_2016_vw_golf-variant.png)

A few remarks from this figure include:
- there are fewer offers in the target price/km range in Portugal compared to Germany; 
- in Portugal, there are very few offers overall with less than 75.000 km, indicating people hold on to their cars for longer before putting them on the market (this can be seen also by the abundance of bluer points on the right panel, which shows the car year);
- in Portugal the cars are less powerful, suggesting that Golf buyers either don't opt for the stronger engine versions, or if they do they do not put them back in the used car market (though this appears less likely).

Overall, given the option, Germany is a better place to look for Volkswagen Golf. Playing around with these scripts for other car brands/models reveals the same general conclusion (which was well known, but can visualized now with the aid of these scripts/plots).


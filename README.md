# WorldBank-data-wrangling-visualisation

In the Jupyter notebook, data visualisation were performed on six time series data sets of key economic & environmental indicators.
The data were downloaded from the World Bank website as csv files. The following indicators were analysed:

- NY.GDP.MKTP.CD -> GDP (current US$) (GDP.csv)
- AG.LND.AGRI.ZS -> Agricultural land (% of land area) (agriculture_area.csv)
- AG.LND.FRST.ZS -> Forest area (% of land area) (forest_area.csv)
- EN.ATM.CO2E.PC -> CO2 emissions (metric tons per capita) (CO2_emission.csv)
- EG.CFT.ACCS.ZS -> Access to clean fuels and technologies for cooking (% of population) (clean_fuel_access.csv)
- EG.FEC.RNEW.ZS -> Renewable energy consumption (% of total final energy consumption) (renewable_consumption.csv)
  
Note: all relevant csv files have been downloaded & saved without modifications in '../main/datasets' folder.

The code in the notebook was written before I knew anything about the World Bank API (or any APIs in general). So, the code is meant to serve in speeding up data analyses and visualisation only AFTER the csv files have been downloaded.
In addition, I did this when I was in the middle of a 3-month-long data science bootcamp by [HyperionDev](https://www.hyperiondev.com/).
I'm, of course, keen to collaborate & exchange ideas about data science in general. For queries about the bootcamp content & curriculum, please contact HyperionDev directly.
</br>I hope you'll find the code useful. Cheers!

A few pointers about the csv file and the code:
- Data downloaded from the World Bank websites are arranged in a particular way: country names are shown as rows & years are shown as columns. While this format is human-friendly, it may not be ideal for plotting.
- In addition, when opened using a text editor application, such as NotePad or TextEdit, there are 4 rows on the top displaying the data source & the date in which the data were last updated.
- The top 4 rows need to be removed so that pandas can read the data and convert them to pandas dataframe. Afterwards, the entire table will be modified so that the years will be displayed in rows rather columns (i.e the table needs to be pivoted).
- To achieve this, a function (process_n_plot) has been written to allow for automatic data processing (see below). In principle, the function should work with any data sets downloaded from the World Bank website.
- Following data processing, the function also generates line graphs for each indicator.

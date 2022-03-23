# Code & Data for "Aggregate Demand, Idle Time, and Unemployment"

This repository contains the code and data to produce the results in the article ["Aggregate Demand, Idle Time, and Unemployment"](https://www.pascalmichaillat.org/3.html), written by [Pascal Michaillat](https://www.pascalmichaillat.org) and [Emmanuel Saez](https://eml.berkeley.edu/~saez/), and published in the [Quarterly Journal of Economics](https://doi.org/10.1093/qje/qjv006) in May 2015.

## Data

The data are stored in two Excel workbooks:

* `data.xlsx` contains the raw data used in the paper, along with descriptions of the data sources. This workbook contains five worksheets:
	– `unused capacity` contains data on the rates of idleness and unemployment in the United States.
	– `occupations` contains data on the number of workers in recruiting and purchasing
	occupations in the United States.
	– `long-term relationships` contains data on the prevalence of long-term customer and employment relationships in 11 countries, including the United States.
	– `quarterly data` contains quarterly macroeconomic data for the United States (capacity utilization rate in manufacturing from the Survey of Plant Capacity, employment level, real output, operating rate in non-manufacturing sectors from the Institute for Supply Management).
	– `monthly data` contains monthly macroeconomic data for the United States (unemployment level, vacancy index, unemployment rate, employment level in manufacturing).
* `cyclical_components.xlsx` contains the cyclical components of product market tightness, labor market tightness, output, and employment for the United States. The cyclical components are computed by the program `construct_cyclical_components.m` from the raw data in `data.xlsx`. Our exploration of the sources of unemployment fluctuations in the United States relies on these cyclical components. This workbook contains two worksheets:
	– `1973--2013` contains the cyclical components of labor market tightness, output, and employment. It also contains the proxy for the cyclical component of product market tightness constructed using the capacity utilization rate in the manufacturing sector measured by the Census Bureau from the Survey of Plant Capacity. These four cyclical components are available at quarterly frequency from 1973:Q4 to 2013:Q2.
	– `1999--2013` contains the cyclical components of labor market tightness, output, and employment. It also contains the proxy for the cyclical component of product market tightness constructed using the capacity utilization rate in the manufacturing sector measured by the Census Bureau from the Survey of Plant Capacity. Last, it contains the proxy for the cyclical component of product market tightness constructed using the operating rate in non-manufacturing sectors measured by the Institute for Supply Management. These five cyclical components are available at quarterly frequency from 1999:Q4 to 2013:Q2.

## Code

The results are produced with Matlab code.

* The script `construct_cyclical_components.m` uses the raw data in `data.xlsx` to produce the cyclical components of product market tightness, labor market tightness, output, and employment. The resulting cyclical components are stored in `cyclical_components.xlsx`.
* The script `plot_figures.m` uses the data in `data.xlsx` and `cyclical_components.xlsx` to produce several figures from the article and online appendices:
	- Figures II
	- Figure VIII
	- Figure IX
	- Figure X
	- Figure A2
	- Figure A3
* The function `quarter.m` transforms a monthly time series into a quarterly time series.

## Software versions

The results were obtained on a Mac running OS X Yosemite with Matlab R2014b.

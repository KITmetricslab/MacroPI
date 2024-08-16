# 'MacroPI' - Macroeconomic Prediction Intervals 

**A forecasting project - simple distributional forecasts for real GDP growth and inflation**

In this project, we construct simple macroeconomic distributional forecasts for in the form of prediction intervals, using existing point forecasts issued by the International Monetary Fund (IMF) within the scope of the biannual World Economic Outlook (WEO) publication. 

The WEO forecasts are issued biannually (once in April and once in September/October) and we issue corresponding prediction intervals in the same rhythm. 

For more information on the IMF WEO forecasts, visit the [corresponding website](https://www.imf.org/en/Publications/WEO/frequently-asked-questions)

Please note that this project is not affiliated with or endorsed by the International Monetary Fund. The data are used in accordance with current [Copyright and Usage guidelines](https://www.imf.org/external/terms.htm) of the WEO publication. 

## Key links

For a visualization of these forecasts, visit our [Shiny App](https://probability-forecasting.shinyapps.io/macropi/). 

We have preregistered the real-time publication of these forecasts. A draft of the relevant document is available in this repo ('MacroPI_draft_preregistration') containing details on the evaluation of these forecasts, time horizon, etc. We plan to deposit a final version of this preregistration on a suitable platform soon. 

The preprint, which contains details on the methodology and describes application results of the retrospective analysis, is available on [ArXiV](https://arxiv.org/abs/2408.08304). 

## Purpose 

Forecasts by macroeconomic institutions are ubiquitous, but are frequently issued in a point forecast format only. Given that forecasts are statements about a future quantity and are thereby inherently uncertain, their transparent and comprehensive communication requires a quantification of said uncertainty. In this project, we address this issue by attaching prediction intervals to one of the largest - both in terms of dissemination and scope - sources for macroeconomic predictions: the International Monetary Fund World Economic Outlook forecasts.

## Forecast targets

- CPI inflation rate (in %)
- real GDP growth rate (in %)

## Contents of this repository
The folders contain the following:

* `forecasts`: Contains csv files with forecasts in a standardized format. The name of the csv-file identifies the forecast origin. We construct central prediction intervals at the 50% and 80% levels based on the predictive quantiles contained in these files. Concretely, each file contains the following columns:
	* `country`: identifies the country using the ISO Alpha-3 code
	* `target`: identifies the target series. `gdp growth` for real GDP Growth, `inflation` for inflation 
	* `forecast year`: the year the forecast is made. Uniquely identifies the forecast origin in conjunction with column `forecast season`
	* `forecast season`: the season the forecast is made, `F` for Fall and `S` for Spring. Uniquely identifies the forecast origin in conjunction with column `forecast year`
	* `target year`: the year the forecast is issued for.
	* `quantile`: the quantile level, one of 0.1, 0.25, 0.75 or 0.9. The 50% forecast interval is comprised of the 0.25 and 0.75 quantiles, the 80% forecast interval of the 0.1 and 0.9 quantiles.
	* `prediction`: prediction value for the forecast instance identified by all other preceding columns. 
* `imf-data`: historical truth data and point forecasts, both from the corresponding IMF World Economic Outlook publication. The name of the csv-file identifies the forecast origin. The csv-files contain the following columns:
	* `country`: identifies the country using the ISO Alpha-3 code
	* `target`: identifies the target series. `gdp growth` for real GDP Growth, `inflation` for inflation 
	* `target year`: the year the forecast is issued for.
	* `prediction`/`true_value`: prediction (point forecasts) or true value (historic values) for the instance identified by all other preceding columns.

## References
- International Monetary Fund. 2023. *World Economic Outlook Database*: Washington, DC. October.
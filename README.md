# 'MacroPI' - Macroeconomic Prediction Intervals 

**A forecasting project - quantifying uncertainty for existing macroeconomic point forecasts**

In this project, we construct central prediction intervals for existing point forecasts issued by the International Monetary Fund (IMF) within the scope of the biannual World Economic Outlook (WEO) publication. 

The WEO forecasts are issued biannually (once in April and once in October) and we issue corresponding prediction intervals in the same rhythm. 

For more information on the IMF WEO forecasts, visit the [corresponding website](https://www.imf.org/en/Publications/WEO/frequently-asked-questions)

Please note that this project is not affiliated with or endorsed by the International Monetary Fund. The data are used in accordance with current [Copyright and Usage guidelines](https://www.imf.org/external/terms.htm) of the WEO publication. 

## Purpose 

Forecasts by macroeconomic institutions are ubiquitous, but are frequently issued in a point forecast format only. Given that forecasts pertain a future quantity and are thereby inherently uncertain, their transparent and comprehensive communication requires a quantification of said uncertainty. In this project, we address this issue by attaching central prediction intervals to one of the largest - both in terms of dissemination and scope - sources for macroeconomic predictions: the International Monetary Fund World Economic Outlook forecasts.

## Forecast Visualization 

For a visualization of the forecasts, visit the shiny app at https://probability-forecasting.shinyapps.io/macroPI

## Forecast targets

- CPI inflation rate (in %)
- real GDP growth rate (in %)

## Contents of this repository
The folders contain the following:

- `forecasts`: forecasts in a standardized format. Currently, forecasts are issued for quantile levels 0.1, 0.25, 0.75 and 0.9. We construct central prediction intervals at the 50% and 80% levels based on these quantiles. 
- `imf-data`: historical truth data and point forecasts, both from the corresponding IMF World Economic Outlook publication.

## References
- International Monetary Fund. 2023. *World Economic Outlook Database*: Washington, DC. October.
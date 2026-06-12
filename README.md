# Simple Macroeconomic Forecast Distributions for the G7 Economies

We construct simple real-time forecast distributions for inflation and growth in the form of forecsat intervals, using existing point forecasts issued by the International Monetary Fund (IMF) within the scope of the biannual World Economic Outlook (WEO) publication.

This repository contains our time-stamped forecasts as well as historical and current WEO point forecasts. We publish our forecasts in accordance with the WEO publication schedule, that is, once in April and once in September/October.

## Purpose

Forecasts by macroeconomic institutions are ubiquitous, but are frequently issued in a point forecast format only. Given that forecasts are statements about a future quantity and are thereby inherently uncertain, their transparent and comprehensive communication requires a quantification of said uncertainty. In this project, we address this issue by constructing forecast intervals from one of the largest — both in terms of dissemination and scope — preexisting sources for macroeconomic forecasts: the International Monetary Fund World Economic Outlook forecasts.

## Retrospective analysis and replication materials

All the code and replication material for our paper can be found in the following GitHub repository. It also contains code to update and publish the real-time forecasts located here.
> <https://github.com/fredbec/uqimf>

The associated paper, published in *The Annals of Applied Statistics*, provides full methodological details and presents the results of the retrospective analysis. It is available open access at:

> Becker, F., F. Krüger, and M. Schienle (2025). "Simple macroeconomic forecast distributions for the G7 economies." *Annals of Applied Statistics*.
> <https://doi.org/10.1214/25-AOAS2095>

When referencing this work, please use the following citation:

	@article{BeckerKruegerSchienle_2025,
  	title={Simple Macroeconomic Forecast Distributions for the G7 Economies},
  	author={Becker, Friederike and Kr{\"u}ger, Fabian and Schienle, Melanie},
  	journal={The Annals of Applied Statistics},
  	volume={19},
  	number={4},
  	pages={2878--2897},
  	year={2025},
  	doi={10.1214/25-AOAS2095},
  	publisher={Institute of Mathematical Statistics}
	}

## Real-time publication

For more information on the time horizon of the project, the scope, and the evaluation of the real-time forecasts, please refer to our preregistration protocol, deposited on the OSF platform.

> Becker, Krüger, and Schienle. 2024. "Simple Macroeconomic Forecast Distributions for the G7 Economies." Deposited 21 September 2024, Registry of the Open Science Foundation.
> <https://osf.io/3b6hk>

	@unpublished{Beckeretal_2024_prereg,
 	  title={Simple Macroeconomic Forecast Distributions for the G7 Economies},
 	  note={Deposited 21 September 2024, Registry of the Open Science Foundation, osf.io/3b6hk},
 	  publisher={OSF},
 	  author={Becker, Friederike and Krüger, Fabian and Schienle, Melanie},
 	  year={2024},
 	  month={Sep}
    }

For a dashboard visualization of our forecast distributions, visit our Shiny App:
> <https://probability-forecasting.shinyapps.io/macropi/>

![MacroPI_shiny_capture](https://github.com/user-attachments/assets/e8d5f17b-1423-4e95-a761-8569b768bc3a)

## Forecast targets

- CPI inflation rate (in %)
- Real GDP growth rate (in %)


## Contents of this repository

The folders and files contain the following:

* `forecasts`: Contains csv files with forecasts in a standardized format. The name of each csv file identifies the forecast origin (e.g., `forecasts_Fall2024.csv` for the Fall 2024 release). We construct central forecast intervals at the 50% and 80% levels based on the forecast quantiles contained in these files. Concretely, each file contains the following columns:
	* `country`: identifies the country using the ISO Alpha-3 code
	* `target`: identifies the target series. `gdp growth` for real GDP growth, `inflation` for inflation
	* `forecast year`: the year the forecast is made. Uniquely identifies the forecast origin in conjunction with column `forecast season`
	* `forecast season`: the season the forecast is made, `F` for Fall and `S` for Spring. Uniquely identifies the forecast origin in conjunction with column `forecast year`
	* `target year`: the year the forecast is issued for
	* `quantile`: the quantile level, one of 0.1, 0.25, 0.75 or 0.9. The 50% forecast interval is comprised of the 0.25 and 0.75 quantiles; the 80% forecast interval of the 0.1 and 0.9 quantiles
	* `prediction`: prediction value for the forecast instance identified by all other preceding columns

* `imf-data`: Historical truth data and point forecasts, both from the corresponding IMF World Economic Outlook publication. The name of each csv file identifies the forecast origin. The csv files contain the following columns:
	* `country`: identifies the country using the ISO Alpha-3 code
	* `target`: identifies the target series. `gdp growth` for real GDP growth, `inflation` for inflation
	* `target year`: the year the forecast is issued for
	* `prediction`/`true_value`: prediction (point forecasts) or true value (historical realizations) for the instance identified by all other preceding columns

* `CHANGELOG.md`: Documents post-publication corrections and pipeline updates to the real-time forecasts, in accordance with the preregistration protocol. Readers who wish to understand any deviations from originally published forecast values should consult this file first.

## Copyright and usage

For more information on the IMF WEO forecasts, visit the [corresponding website](https://www.imf.org/en/Publications/WEO/frequently-asked-questions).

Please note that this project is not affiliated with or endorsed by the International Monetary Fund. The data are used in accordance with current [Copyright and Usage guidelines](https://www.imf.org/external/terms.htm) of the WEO publication.

## References

- International Monetary Fund. 2026. *World Economic Outlook Database*. Washington, DC. October.

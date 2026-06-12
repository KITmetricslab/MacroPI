# Changelog — KITMetricslab/MacroPI repository
*Last updated: June 12, 2026*

This document records changes to the forecast data, methodology, and underlying code
published in this repository. Each entry lists affected forecast rounds, variables, and
countries where applicable. In particular, in accordance with the preregistration protocol
deposited at https://osf.io/3b6hk, any instances of forecast correction subsequent to
their initial publication are documented here.

---

## Bug fix: corrected values for France and United Kingdom

| | |
|---|---|
| **Affected forecast rounds:** | Fall 2025, Spring 2026 |
| **Affected variables:** | GDP growth, Inflation |
| **Affected countries:** | France (FRA), United Kingdom (GBR) |

**Description.** Following a change in the data retrieval process in Fall 2025, point
forecasts and historical values were incorrectly assigned in the data pipeline. This implied an error in the calculation of the most recent (Fall 2025) and the two most recent
(Spring 2026) forecast errors.

**Correction.** All intervals for the affected countries and rounds have been recomputed
and updated in this commit (June 12, 2026, commit message 'Correction: Spring 2026 forecasts', with analogous commit messages for Fall 2025 and contents in folder `imf-data`). The underlying pipeline bug has been fixed.

---

## Change: Consistent rounding to three decimal places

| | |
|---|---|
| **Affected forecast rounds:** | Fall 2025 onward |
| **Affected variables:** | GDP growth, Inflation |
| **Affected countries:** | All |

**Description.** In accordance with a change in the IMF's published data format, all
previous values (historical) were rounded to three decimal places.

# MHW-impacts-on-Kelp
Data and Code for the research of the relationship between marine heatwave (MHW) and long-term observational kelp in different populations.

## Data 
| Data | Source |
|-----:|---------------|
| Reef monitoring kelp cover | Australia’s National Reef Monitoring Network. https://catalogue-imos.aodn.org.au/geonetwork/srv/eng/catalog.search#/metadata/ec424e4f-0f55-41a5-a3f2-726bc4541947 |
| Sea surface temperature | High Resolution NOAA Optimum Interpolation 1/4 Degree Daily SST (OISST) Analysis, Version 2. https://www.ncei.noaa.gov/metadata/geoportal/rest/metadata/item/gov.noaa.ncdc:C00844/html |
| Thermal performance of Ecklonia radiata | Wernberg et al. (2016) and Britton et al. (2024) |
| Occurrence distribution of Ecklonia radiata | Ocean Biodiversity Information System (OBIS) |

## Code files
| File | Description |
|-----:|---------------|
| clean_kelp_data_survey_id.R | Fixing the recording-only-presence problem of the raw kelp cover data, and averaging the data into survey_id and site level |
| mhw_kelp_detection.ipynb | Calculating summer time temperature and MHW metrics for each site and year of kelp surveys, conducting GLMM analysis |
| mhw_kelp_timeseries.ipynb | Plotting timeseries of summer-time temperature, annual abundance of kelp, and MHW categories |
| model_3pop.ipynb | Plotting the GLMM results |
| obisoccurance.ipynb | Calculating MHW temperature climatologies across the geographical distribution of Ecklonia radiate, using occurrence data of kelp from OBIS |
| tpc_review.R | Constructing thermal performance curve and temperature limits for 4 locations from Wernberg et al. (2016) and Britton et al. (2024) |

# References
Wernberg, T, de Bettignies, T, Joy, BA & Finnegan, PM 2016, 'Physiological responses of habitat‐forming seaweeds to increasing temperatures', Limnology and Oceanography, vol. 61, no. 6, pp. 2180-2190.
Britton, D, Layton, C, Mundy, CN, Brewer, EA, Gaitan-Espitia, JD, Beardall, J, Raven, JA & Hurd, CL 2024, 'Cool-edge populations of the kelp Ecklonia radiata under global ocean change scenarios: strong sensitivity to ocean warming but little effect of ocean acidification', Proc Biol Sci, vol. 291, no. 2015, p. 20232253.

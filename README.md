[![DOI](https://zenodo.org/badge/759275381.svg)](https://doi.org/10.5281/zenodo.15009284)
# MHW-impacts-on-Kelp
Data and Code for the research of the relationship between marine heatwave (MHW) and long-term observational kelp in different populations.

| Data | Source |
|-----:|---------------|
| Reef monitoring kelp cover | Australia’s National Reef Monitoring Network. Instruction: https://catalogue-imos.aodn.org.au/geonetwork/srv/eng/catalog.search#/metadata/ec424e4f-0f55-41a5-a3f2-726bc4541947 |
| Sea surface temperature | High Resolution NOAA Optimum Interpolation 1/4 Degree Daily SST (OISST) Analysis, Version 2. https://www.ncei.noaa.gov/metadata/geoportal/rest/metadata/item/gov.noaa.ncdc:C00844/html |
| Thermal performance of Ecklonia radiata | Wernberg et al. (2016) and Britton et al. (2024) |
| Occurrence distribution of Ecklonia radiata | Ocean Biodiversity Information System (OBIS). Data access from https://github.com/iobis/robis |

## Data files
| File | Description |
|-----:|---------------|
| er_atrc_id.csv | Dataset of Ecklonia radiata under Australian Temperate Reef Collaboration at survey_id level after quality control. The identical survey_id represents a survey conducted on the same transect.  |
| er_3pop_site.csv | Dataset of Ecklonia radiata under averaged at site level in Jurien, Jervis Bay, and Maria Island |
| 4pop_change_rawdata.csv | Dataset of the change in canopy cover of Ecklonia radiata at each site of the four locations, including the corresponding MHW metrics (Hobday et al., 2016)|

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
Reef Life Survey (RLS); Institute for Marine and Antarctic Studies (IMAS); Parks Victoria; Department of Primary Industries (DPI), New South Wales Government; Parks and Wildlife Tasmania; Department for Environment and Water (DEWNR), South Australia; Department of Biodiversity, Conservation and Attractions (DBCA), Western Australia; Integrated Marine Observing System (IMOS), 2024, IMOS - National Reef Monitoring Network Sub-Facility – Benthic cover data (in situ surveys), database provided, 10/10/2024.

Hobday, A. J., Alexander, L. V., Perkins, S. E., Smale, D. A., Straub, S. C., Oliver, E. C. J., Benthuysen, J. A., Burrows, M. T., Donat, M. G., Feng, M., Holbrook, N. J., Moore, P. J., Scannell, H. A., Sen Gupta, A., & Wernberg, T. (2016). A hierarchical approach to defining marine heatwaves. Progress in Oceanography, 141, 227-238. https://doi.org/https://doi.org/10.1016/j.pocean.2015.12.014 

Wernberg, T, de Bettignies, T, Joy, BA & Finnegan, PM 2016, 'Physiological responses of habitat‐forming seaweeds to increasing temperatures', Limnology and Oceanography, vol. 61, no. 6, pp. 2180-2190.

Britton, D, Layton, C, Mundy, CN, Brewer, EA, Gaitan-Espitia, JD, Beardall, J, Raven, JA & Hurd, CL 2024, 'Cool-edge populations of the kelp Ecklonia radiata under global ocean change scenarios: strong sensitivity to ocean warming but little effect of ocean acidification', Proc Biol Sci, vol. 291, no. 2015, p. 20232253.

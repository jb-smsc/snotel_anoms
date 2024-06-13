# SNOTEL and BC-Alberta SWE anomalies
Derive 1 April 2024 SWE anomalies relative to 1991-2020 climatology for SNOTEL and western Canada sites.

### AprilSNOTELanom.py
This script calculates the 1 April SWE climatology for 1991-2020 for SNOTEL sites. It then calculates the 1 April SWE anomaly for 2024 relative to 1991-2020 climatology.

For each sites, instances of SWE == 0 are identified and written to the main dataframe as are the number of years during 1991-2020 with SWE observations.

The SNOTEL data used are directly from NRCS (i.e. not the BCQC dataset). These data will soon be included in v2 of https://zenodo.org/records/10287093 , which should make it easier to reference.

### BCAB 1 April 2024 anomalies

Same as SNOTEL but for BCAB snow pillows and uses CanSWEv6 to derive the 1991-2020 climatologies.

### .csv output [1April2024_SNOTEL_anom.csv & 1April2024_BCAB_anom.csv]

time: 1 April 2024

station_id: for snotel sites, SNOTEL sation ID appended to 'SNOTEL_'

station_name: station name

snw: 1 April 2024 snow water equivalent, units = mm or kg/m-2

lat: station latitude, degrees North

lon: station longitude, degrees West

Elevation_NTK: station elevation (m)

clm: 30yr (1991-2020) climatological SWE. This value is calculated for all available sites regardless of the number of years with data.

nyrs: number of years with valid SWE observations

anom: 1 April 2024 SWE anomaly relative to the 30yr climatology. This value is calculated for all available sites regardless of the number of years with data.

snw0: years when swe = 0 on 1 April for the corresponding site. If NaN then all years with observations (all nyrs) have swe >0.

pct_anom: swe anomaly expressed as a percent of the 30yr climatology. This value is calculated for all available sites regardless of the number of years with data.

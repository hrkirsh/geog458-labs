# Population density of the world's largest cities - Data package

This data package contains the data that powers the chart ["Population density of the world's largest cities"](https://ourworldindata.org/grapher/population-density-by-city?tab=discrete-bar&time=2020&country=Moscow~Istanbul~Karachi~Tokyo~Shanghai~Manila~Sao+Paulo~New+Delhi&v=1&csvType=filtered&useColumnShortNames=false) on the Our World in Data website.

### Active Filters

A filtered subset of the full data was downloaded. The following filters were applied:
- country: Moscow, Istanbul, Karachi, Tokyo, Shanghai, Manila, Sao Paulo, New Delhi
- tab: discrete-bar
- time: 2020

## CSV structure

Each row is an observation for an entity (usually a country or region) at a timepoint.

- "Entity" — the name of the entity, e.g. "United States".
- "Code" — our internal entity code. For most countries this is the [ISO alpha-3](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3) code, e.g. "USA"; historical and other non-standard entities get a custom code.
- "Year" or "Day" — the timepoint. Annual data has a "Year" column holding an integer year; otherwise a "Day" column holds a date string in the form "YYYY-MM-DD".
- Every remaining column is a data column, each one a time series. Downloaded with the "full data" option each corresponds to one time series below; with "only selected data visible in the chart" they are transformed depending on the chart type, so the correspondence may be less direct.


## Metadata.json structure

The .metadata.json file contains metadata about the data package. The "charts" key contains information to recreate the chart, like the title, subtitle etc. The "columns" key contains information about each of the columns in the csv, like the unit, timespan covered, citation for the data etc.

## How we process data at Our World in Data

Our World in Data is almost never the original producer of the data - almost all of the data we use has been compiled by others. If you want to re-use data, it is your responsibility to ensure that you adhere to the sources' license and to credit them correctly. Please note that a single time series may have more than one source - e.g. when we stitch together data from different time periods by different producers or when we calculate per capita metrics using population data from a second source.

Preparing this data involves several processing steps. Depending on the data, this can include standardizing country names and world region definitions, converting units, calculating derived indicators such as per capita measures, as well as adding or adapting metadata such as the name or the description given to an indicator.
[Read about our data pipeline](https://docs.owid.io/projects/etl/).

## Detailed information about each time series


### Population density of the top 100 most populous cities
Number of people per km² of land area for cities ranked among the top 100 most populous in 2020. City boundaries are defined using a consistent global approach based on satellite imagery and population data.
Last updated: December 10, 2025  
Next expected update: December 2026  
Date range: 1975–2020  
Unit: people per km²  
Source: European Commission, Joint Research Centre (JRC) (2025) – with minor processing by Our World in Data  

#### How to cite this data

European Commission, Joint Research Centre (JRC) (2025) – with minor processing by Our World in Data

#### What you should know about this data
- Estimated population density of each of the world's 100 most populous cities (as ranked in 2020), based on satellite imagery and census data.
- Cities are defined as areas with at least 1,500 people per km² and a total population of at least 50,000, identified using the [Degree of Urbanization](https://human-settlement.emergency.copernicus.eu/degurba.php) framework based on satellite imagery and census data.
- City boundaries are fixed at their 2025 extent across all years, so historical values reflect conditions within today's boundaries. This can make fast-growing cities appear less dense in earlier periods.
- Cities are also split at country borders, so a city that straddles two countries will appear as two separate entries.
- City boundaries are model-derived and may not match official administrative limits. Data quality varies by region and tends to be lower where census data is sparse or outdated.
- The underlying population figures have been rescaled to match UN World Population Prospects 2022 national totals, so country-level numbers are consistent with UN estimates.
- For 1950–1975, estimates use UN national statistics. From 1975 onwards, population is mapped to 1 km² grid cells using the [Global Human Settlement Layer (GHSL)](https://human-settlement.emergency.copernicus.eu/).
- The ranking of the top 100 cities is fixed based on their population in 2020. Historical values show the density of those same cities across time.
- Historical figures that the producer rates as low plausibility are not shown, and appear as gaps.

#### Notes on our processing step for this indicator
Population density was calculated by dividing the population of the urban center by its total land area.

The producer rates how plausible each city's population figure is, on a four-point scale from low to very high. We do not show the historical figures it rates as "low", leaving those years blank rather than estimating them. Projected values are kept as published, because for future years a low rating usually reflects ordinary forecast uncertainty.


### Projected population density of the top 100 most populous cities
Projected number of people per km² of land area for cities ranked among the top 100 most populous in 2020. City boundaries are defined using a consistent global approach based on satellite imagery and population data.
Last updated: December 10, 2025  
Next expected update: December 2026  
Date range: 2020–2100  
Unit: people per km²  
Source: European Commission, Joint Research Centre (JRC) (2025) – with minor processing by Our World in Data  

#### How to cite this data

European Commission, Joint Research Centre (JRC) (2025) – with minor processing by Our World in Data

#### What you should know about this data
- Projected population density of each of the world's 100 most populous cities (as ranked in 2020), based on the GHSL modeling framework anchored to UN World Population Prospects 2022.
- Cities are defined as areas with at least 1,500 people per km² and a total population of at least 50,000, identified using the [Degree of Urbanization](https://human-settlement.emergency.copernicus.eu/degurba.php) framework based on satellite imagery and census data.
- City boundaries are fixed at their 2025 extent across all years, so historical values reflect conditions within today's boundaries. This can make fast-growing cities appear less dense in earlier periods.
- Cities are also split at country borders, so a city that straddles two countries will appear as two separate entries.
- City boundaries are model-derived and may not match official administrative limits. Data quality varies by region and tends to be lower where census data is sparse or outdated.
- The underlying population figures have been rescaled to match UN World Population Prospects 2022 national totals, so country-level numbers are consistent with UN estimates.
- Projections use the [CRISP spatial model](https://www.researchgate.net/publication/384062691_Calibration_of_the_CRISP_model_A_global_assessment_of_local_built-up_area_presence) at 1 km² resolution, following the UN World Population Prospects 2024 medium scenario.
- The ranking of the top 100 cities is fixed based on their population in 2020. Projected values show the density of those same cities in future years.

#### Notes on our processing step for this indicator
Population density was calculated by dividing the population of the urban center by its total land area.


## Sources

These are the sources behind the data in this package. Each time series above names the ones it draws on in its citation.

### European Commission, Joint Research Centre (JRC) – Global Human Settlement Layer Dataset

The dataset includes population projections by degree of urbanization and at the city level.

For every country and territory in the world, the authors estimated their population from 1950 to 2100 in cities, towns and semi-dense areas, and rural areas. It relies on the UN-endorsed Degree of Urbanisation methodology. As a result, the definitions used in each country are fully harmonized; while national definitions vary considerably.

The long time series consists of three parts:

- From 1950 to 1970, it is based on backcasting by blending data using national definitions of urban and rural areas with data using the Degree of Urbanisation.
- From 1975 to 2020, it is based on the Global Human Settlement Layer (GHSL), because it has the longest time series and uses a transparent and reproducible method.
- From 2020 to 2100, it relies on a new model, "Cities and Rural Integrated Spatial Projections" (CRISP).

The CRISP model estimates population and built-up area change for a global grid of 1 km2 cells in an evidence-based, three-step process. First, the authors estimate population and built-up area change for roughly 1000 functional areas based on past trends and national population projections. Second, they allocate new built-up area to grid cells considering distance to settlements, roads, water, current share of built-up area and other characteristics. Finally, they add population to newly built-up areas and more suitable locations and reduce it in less suitable locations to capture internal migration and natural population decline.

Beyond population, the dataset also delivers maps showing the evolving spatial extent of cities, towns and rural areas. For every city in the world, it also provides updated boundaries, land area and built-up area at five-year intervals from 1975 to 2100.

Producer: European Commission, Joint Research Centre (JRC)  
Published: 2025  
Retrieved on: 2025-12-10  
Retrieved from: https://human-settlement.emergency.copernicus.eu/ghs_wup2025.php  
Direct download: https://jeodpp.jrc.ec.europa.eu/ftp/jrc-opendata/GHSL/GHS_WUP_MTUC_GLOBE_R2025A/V1-0/GHS_WUP_MTUC_GLOBE_R2025A_V1_0_statistics.zip  
License: European Union, 1995-2025 (https://human-settlement.emergency.copernicus.eu/GHSLhowToCite.php)  

Citation: Schiavina, Marcello; Alessandrini, Alfredo; Melchiorri, Michele; Dijkstra, Lewis (2025): GHS-WUP-MTUC R2025A – GHS-WUP multitemporal urban centres, obtained from the Degree of Urbanisation grids (GHS-WUP-DEGURBA R2025A) and linked across epochs, multitemporal (1950-2100). European Commission, Joint Research Centre (JRC). PID: http://data.europa.eu/89h/1ea967e5-bedc-4cf3-a0b0-3851742ee7e2 , doi: 10.2905/1ea967e5-bedc-4cf3-a0b0-3851742ee7e2

Pesaresi, Martino, Marcello Schiavina, Panagiotis Politis, Sergio Freire, Katarzyna Krasnodębska, Johannes H. Uhl, Alessandra Carioli, et al. (2024). Advances on the Global Human Settlement Layer by Joint Assessment of Earth Observation and Population Survey Data. International Journal of Digital Earth 17 (1). doi:10.1080/17538947.2024.2390454

Jacobs-Crisioni, Chris et al (2025). Population projections by degree of urbanisation for the UN World Urbanization Prospects: introducing the CRISP model, Publications Office of the European Union, Luxembourg, 2025, doi:10.2760/7163875

    
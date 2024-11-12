# Greggs Locations Geocoding and Mapping Project
This project demonstrates how to geocode a list of Greggs store locations in the UK by using the National Statistics Postcode Lookup (NSPL) dataset. It standardises postcodes, joins the NSPL coordinates with each Greggs location, and visualizes the stores on an interactive map centred on Manchester.

## Project Overview
This Jupyter Notebook project is structured to guide you through each step required to:

1. Load and preprocess the Greggs locations dataset (`greggs_uk.csv`).
2. Standardize postcodes to a consistent format.
3. Load and subset the NSPL dataset (`NSPL21_AUG_2024_UK.csv`) to retain only essential columns.
4. Merge datasets to assign coordinates to each Greggs store.
5. Visualize results on an interactive map using Folium.

## Files
* `NSPL_Geocode.ipynb`: The Jupyter Notebook with the code and detailed instructions.
* `greggs_uk.csv`: CSV file with Greggs store details, including columns for `postcode`, `name`, `address`, and `rating`.
* `NSPL21_AUG_2024_UK.csv`: CSV file with the National Statistics Postcode Lookup data, including `pcds`, `lat`, and `long` columns.  This will need to be downloaded from the [ONS Open Geography Portal](https://geoportal.statistics.gov.uk/search?q=PRD_NSPL%20AUG_2024&sort=Date%20Created%7Ccreated%7Cdesc)

## Requirements
* Python 3.x
* Libraries: `pandas`, `geopandas`, `folium`

Install the necessary libraries using:

`pip install pandas geopandas folium`

## Usage
1. Run each cell in the Notebook to load, process, and visualise the data.
2. The output will be an HTML map with markers for each Greggs store, displaying `name`, `address`, and `rating` in the popups.

## Example Instructions
To start using this Notebook:

1. Load the Greggs data from `greggs_uk.csv`.
2. Standardize the postcode format to uppercase with a space before the last three characters.
3. Load the NSPL data and subset it to keep only necessary columns.
4. Merge the data on the postcode column.
5. Visualize the data on a Folium map, centred on Manchester.

## Expected Output
An interactive map of Greggs locations across the UK centred on Manchester. Clicking a marker will show the store’s `name`, `address`, and `rating`.

## License
The Greggs data is sourced from the Food Standards Agency’s [Food Hygiene Rating Scheme](https://data.food.gov.uk/catalog/datasets/38dd8d6a-5ab1-4f50-b753-ab33288e3200) under the [Open Government Licence (v3)](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/). The data was acquired on 12th November 2024 and may have changed since then, so it should not be relied upon for current or official use. This project is for educational purposes only.
# Marine Cadastre AIS (MCAIS) Data Parse
Download AIS data from MarineCadastre's AIS (MCAIS) data files and return all ships of specified types that travel within defined geo-boundaries and timespan(s).

This code was developed as part of the 2023 ASG Data Visualization Challenge in which AIS data was to be used to find shipping route changes in the Arctic due to ice level changes over time.  This repository has code to do the following:
1. Pull AIS data from Marine Cadastre's repository (available here: https://marinecadastre.gov/ais/) based on specified date range, geo-boundaries, and ship type(s)
2. Reduce data size by removing erroneous lat/long values, aggregating port/harbor milling data to a single point, and reducing route data by using a straight-line reduction algorithm.
3. Returns the finished dataframe containing only the relevant data points needed to plot routes and show stop points - as well as a dataframe containing the calculated stop points.

Note: The Marine Cadastre data used is limited to just the data along U.S. coasts.  See https://marinecadastre.gov/ais/ for more information.

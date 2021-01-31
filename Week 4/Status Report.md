# Status Report - Aziz and Andrew
BRT in Los Angeles and Atlanta: https://github.com/amjarnagin/BRT_project/blob/main/Project%20Proposal.md
## Project Roles
* Aziz: Los Angeles mapmaker
  * Will be working on the Los Angeles portion of the project. This includes generate the BRT maps for the Orange and the Silver Line, creating isochrome walksheds around the station, and compiling census data relating to race, poverty level, and car ownership
* Andrew: Atlanta mapmaker
  * Responsible for Atlanta analysis: creating geoJSON files for proposed BRT routes, generating isochrone walksheds for each station, and bringing in relevant census data. Andrew is also working on writing a function to automate the isochrone generation process.
## Status Update
Mood is good, we have a clearer vision of what is feasible and what to focus on in our project.
## Data Update
* Data sources are fine at the moment, have data for race but will be looking for data sources for car ownership (we found “Means of Transportation to Work” in the census, but I’m not sure if there’s a better measure that isn’t focused solely on commute), and see if there is a specific dataset for poverty. Will need to locate which file BRT lines in Los Angeles will be in, as I was told by another group that the BRT data is not in the file that one would expect in the Metro website.
* For Atlanta, Andrew was able to make a geoJSON (https://github.com/amjarnagin/BRT_project/blob/main/Week%204/MARTA_BRT_routes_stops.geojson) for proposed BRT routes working off lines I, J, and K from the More MARTA plan (https://itsmarta.com/uploadedFiles/MoreMARTAAtlantaMap06192019.pdf). Only the Capitol Ave BRT has planned station locations, so for the other two lines I made a best guess for reasonable stops.
* We were having trouble finding density information in Census Reporter, but it turns out that Social Explorer has population density per square mile! So that solves one issue. May also try to find information about employment density if needed.
## Concerns
### Major: N/A
### Minor:
* (Aziz) If we cannot find poverty level census data would it be possible to combine income categories together? Aziz tried in the previous assignment to combine the lowest four income categories in LA County, accounting for the poverty level of the average family size in LA County (3). However, there were some values in the fourth category that were higher than the poverty level. Would subtracting those values be possible?
* (Andrew) Is there a simple way to combine multiple isochrones to a single basemap? I have some ideas, but the goal would be to display isochrones for a complete BRT route (or even better, for all routes in the city). As is, my function can generate a series of individual isochrone maps, but doing too many overloads the notebook memory.
(Andrew) I’m guessing we’ll go over this later in the course, but I’m trying to think through how to analyze/map census data in combination with isochrones. Potentially finding the tracts within the isochrone and then performing the analysis on those tracts?
  

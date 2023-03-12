# baseball_projects
Sample collection of my independent baseball research projects.

## Run Expectancy
My premier project. Takes in Tru Media pitch-by-pitch data, located in the nested folders, and parses the data to calculate the average run expectancy from every base-out-state. Using the data, I was able to create a number of deliverables that included: when to bunt, break even rate for stolen bases, and the effect on batter importance dependent on their spot in the batting order. Also, created a lineup simulator to estimate the average runs per game each lineup order will score. 

## MLB Player Comp Finder
This is a script that analyzes MLB pitching data from Statcast and college data from Rapsodo to predict how pitchers compare to MLB players. The script downloads Statcast data for a specific period, selects important metrics, and converts some values to be consistent with Rapsodo. It then determines which pitchers have thrown at least 100 pitches, cleans and reads in Rapsodo data, and predicts MLB pitcher comparisons using a random forest classifier.

The output is a dataframe showing predicted player comparisons for each pitcher. 

## Statcast War
This is a Python script that calculates xWAR (Expected Wins Above Replacement) for MLB players for two different years and calculates the R^2 scores for WAR and xWAR. The get_xwar() function retrieves batting and fielding statistics for a given year and calculates xwRAA, BSR, and xRuns for each player, as well as the league-wide batting and pitching statistics. It then calculates xWAR for each player. The get_xwar_two_years() function calls get_xwar() for each year and merges the data for the two years, keeping only rows that are present in both dataframes. Finally, the script calculates the R^2 scores for WAR and xWAR using the mean squared error function from the metrics module.

The output of the script is the R^2 scores for WAR and xWAR from 2021 to 2022. The purpose and methodology of the analysis are relatively straightforward, although some knowledge of baseball statistics and terminology may be required to fully understand the calculations being performed. The correlation between run and both xWAR and WAR were also calculated. The findings showed that while xWAR is a little less correlated with runs than WAR, xWAR is much more predictive year over year.

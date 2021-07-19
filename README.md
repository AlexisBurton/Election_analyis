# Election Analyis

## Project Purpose
This code was written to determine the results of a district election. The goal was to determine not only the overall winner, but also give a breakdown of total votes by county. 

## Election Audit Results
- There were a total of votes 369,711 cast. This was calculated by setting the initial vote count to zero, and then running through each data row of the original .csv file and adding 1 to the total vote count for each iteration. [total vote code](Documentation/total\ vote\ code.png)

- Votes by County: 
Similar to calculating the total election results, an initial county vote variable was set to zero. This variable however was created as a dictionary tied to the County names, so as the program iterated through the .csv data, a vote was added to the appropriate dictionary entry based on the county listed in each row. [county vote code](Documentation/county\ vote\ code.png)


	| County | Votes Cast | % of Total Votes |
	| :--- | --- | ---: |
	|  Arapahoe |   24,801 | 6.7 %  |
	|  Denver |  306,055 | 82.8 %  |
	|  Jefferson |   38,855 | 10.5%  |



- Denver County cast the most votes.
- Votes by Candidate

	| Candidate | Total Votes | % of Total Votes |
	| :--- | --- | ---: |
	|  Diana DeGette |  272,892 | 73.8 % |
	|  Raymond Anthony Doane |   11,606 | 3.1 % |
	|  Charles Casper Stockholm |   85,213 | 23.0 % |

- Diana DeGette won the election with 272,892 votes, or 73.8% of the total votes cast.

## Election Audit Summary
This code works well for the district election for which it was created. It does however have the proper framework to calculate other election types, whether they be larger or smaller. Were it to be used for local elections, you could add a dictionary within the counties that would tabulate votes for county-level positions. Conversely, for state-wide elections, you could create a district dictionary that uses the individual counties as dictionary keys. 

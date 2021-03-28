# Election_Analysis
Election Analysis project for UT Austin Data Analysis Bootcamp

## Project Overview
A Colorado Board of Elections employee has given you the following tasks to complete the election audit of a recent local congressional election.

1. Calculate the total number of votes cast.
2. Get a complete list of candidates who received votes.
3. Calculate the total number of votes each candidate received.
4. Calculate the percentage of votes each candidate won.
5. Determine the winner fo the election based on popular vote.

## Resources
- Data Source: election_results.csv
- Software: Python 3.7.6, Visual Studio Code 1.54.3

## Results
The analysis of the election show that:
1. There were 369,711 votes cast in the election.
2. The candidates were:\
  -Charles Casper Stockham\
  -Diana DeGette\
  -Raymon Anthony Doane
3. The candidate results were:\
  -Charles Casper Stockham  23.0%  (85,213 votes)\
  -Diana DeGette  73.8%  (272,892 votes)\
  -Raymon Anthony Doane  3.1% (11,606 votes)
4. The winner of the election was Diana DeGette.

## Challenge Overview
The election commission has given you the following tasks to provide them with additional data in order to complete the audit:

1. Calculate the voter turnout by county.
2. Calculate the percentage of votes from each county out of the total count.
3. Determine the county with the highest turnout.

## Challenge Results
Analysis of the election data showed that:
1. The number of votes cast by county were:\
-Jefferson: 38,855\
  -Denver: 306,055\
  -Arapahoe: 24,801
2. The percentage of total votes cast by each county were:\
  -Jefferson: 10.5%\
  -Denver: 82.8%\
  -Arapahoe: 6.7%
3. The county with the highest turnout was Denver County.

## Summary
In order to accomplish the assigned tasks, we first opened and read the file using Python. We then looped through the rows of votes using a `for` loop. With each vote we incrementally increased the total count of votes using the script `total_votes += 1`. At the same time we used logical statements to check if the candidate had already been added to our list of candidates receiving votes. If they had not, we appended them to our data. We also incrementally increased the vote count for the candidate receiving that vote. We then added the county to our list if it had not already been added, and incrementally increased the vote total for that county. After performing some simple mathematical operations, we used a `with open()` statement to open a text document and write the results there, while also printing the results to the terminal. 

This script could be easily modified to process data for other elections as well. Because the addition of candidates to the list of candidates is an automated process, it can handle any number of candidates. Likewise, it can handle any number of counties. If the election were for a narrower location, such as a municipal election, and the electoral commission wanted to analyze the data based on subdivision rather than county, we could reword the print statement `f"Largest County Turnout: {largest_turnout_county}\n”` to instead read `f”Largest Subdivision Turnout: {largest_turnout_subdivision}\n”`. We would also need to relabel the variables naming county statistics. If we wanted the code to have even broader application, we could read the csv header to determine how the data should be broken down and then have our code write the results in those terms automatically.

If the script were to be applied to a larger election, say a national one, we could further break down the results by state and county by adding another nested `for` loop which would tally the votes by state and county.



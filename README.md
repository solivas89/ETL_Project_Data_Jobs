# September 03, 2020 - ETL_Project_Data_Jobs

# Project Team Members
Max Oteng
Sal Olivas

# Git Hub Repository Link
https://github.com/solivas89/ETL-Project_Data-Anlyst-Postions.git

# **E**xtract: 
We were able to find 2 data soruces, both of which are CSV files, in Kaggle. In discussing our project and doing 
research, we came across the topic of Data Analyst/Scientist postion that were scraped from both Glassdoor and LinkedIn.
The data from Glassdoor dpesn't have as many listings as that of the one from LinkedIn, however it does show additional
data like Salary Estimates and Orginization type (ie. Profit / Non-Profit).

	- Data Scientists Job Market in the U.S. - Report from August of 2018 but used to show just how many data
	scientist positions are available.
	- Data Analyst Jobs - unsure of date of data set, however, the data is more recent as it pertains to job listings 
	amidst the ongoing pandemic. 

Ultimately we chose these 2 data sources to Extract, Transfrom, and Load this data to show just how many Data Analyst/Scientist positions
are out there. Both in general and specific to certain major cities. 

# **T**ransform:
Once the data files were read into our data base, a different types of transfromation and some cleaning took place. 
See below...

* Filtering:
	1. Column names to show only the columns thought pertinent. 
	2. To hone in some job listings in the data set that shows salary estimates, we filtered to only showed job postings 
	in 2 large cities - Los Angeles, CA & New York, NY.
* Cleaning:
	1. Renamed Column to display how we saw fit.
	2. Removed unecessary text / information from our data sets.
		- Some values were showen as "-1". We replaced that with "Unknown" for consistency across our data sets
		- Some values were "NaN". We replaced that with "Unknown" for consistency across our data sets
		- We removed repetitive text that was wrapped in parenthesis. This proved particularly difficult and required
		assistance to do so properly. We thought we were able to remove the text and parenthesis as they were not shown 
		when the data was listed. However, when printed out in a data frame, only the parenthesis remained. We were
		able to remove the parenthesis once we set "regex=False" in our code.
		- Removed zip codes from our data as some of the locations ended with zipcodes.
* Aggregating:
	1. Perfomred grouby counts in order to see just how many jobs are listed.
	in the utilized data sets. Additionally, it allowed to provide SQL statements for ease of use of the tables created.



# **L**oad:
	1. We chose to load our data set into PostgresSQL as it is one of the most commonly used relation database management
	systems. Additionally, it allow for ease of use in performing data queries with the extracted and tranfor on the job use 
	2. In doing so, we created 2 tables with the 2 data sets we utilized for this porject. See below...
	- Data Base Name: Data_Jobs
	- Table Names: la_ny_table & major_cities_table
		***Add in data base name and table names



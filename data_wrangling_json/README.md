# Data Wrangling with JSON

JSON exercise
Using data in file 'data/world_bank_projects.json',
1. Find the 10 countries with most projects
2. Find the top 10 major project themes (using column 'mjtheme_namecode')
3. In 2. above you will notice that some entries have only the code and the name is missing. Create a dataframe with the missing names filled in.

**Solution to Q1:**
1. Read 'world_bank_projects.json' and store to dataframe, then inspect the data structure
2. Since each project is paired with a country name, we count the occurence of each country name to find the top 10 countries with most projects.

**Solution to Q2:**
1. Read 'world_bank_projects.json' and store as string, then inspect the data structure
2. The column 'mjtheme_namecode' is a dict of code and name of projects. Because some row of the name are empty, we need to count the occurence of project code instead of name. 

**Solution to Q3:**
1. Sorting teh dataframe from Q2 by projects' code and name.
2. Fill the empty field with NaN
3. Apply the .fillna() method with 'bfill', Backward fill, to fill all NaN with appropriate project names.

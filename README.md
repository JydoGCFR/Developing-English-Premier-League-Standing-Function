# Developing-English-Premier-League-Standing-Function

**"An Overview of this Project:** 
    
The dataset utilized by the EPL_Standings function comprises pertinent details pertaining to matches 
in the English Premier League (EPL). The match between two teams is delineated in each row, which 
comprises the following information: date, home team, away team, full-time home goals (FTHG), full-time
away goals (FTAG), and full-time result (FTR). The outcome of the match is denoted in the FTR column 
as either a victory ('H'), a defeat ('A'), or a draw ('D') for the host team.

**Critical Variables:**

Date: Date of the match.
HomeTeam: Name of the home team.
AwayTeam: Name of the away team.
FTHG: Full-time home goals.
FTAG: Full-time away goals.
FTR: Full-time result (win, lose, or draw).

**Approach to Methodology:**

**Data Retrieval:** Using URLs specified by the season parameter, the function retrieves the EPL match data
for the specified season from a website (the current season, and the last two seasons).

**Preprocessing of Data:** Only the required columns (Date, HomeTeam, AwayTeam, FTHG, FTAG, FTR) were 
selected by the function.
The function formated dates by transforming the provided date into a date format object and applying the
modified date to the unprocessed data.
The data was filtered until and including the date of input.

**Data Transformation:** The function performs a data transformation from the match-level to the team-level
by renaming columns, generating distinct data frames for home and away matches, and computing 
supplementary variables including match type ('Home' or 'Away'), record (including wins, losses, and 
draws), and points.
It consolidated the home and away match data frames into a solitary data frame named 'epl_clean'.

**Summary Statistics:** These were computed by the function in accordance with the names of the teams involved. 
These statistics include the following: overall record, home record, away record, matches played, 
points, victories (Wins), goals scored (GS), and goals allowed (GA).
The requested metrics such as point percentage (PtPct), goals scored per match (GSM), and goals allowed
per match (GAM) were calculated.

**Sorting the final table:** In descending order, the function sorts the summary table according to the following criteria: points 
earned per match (PPM), wins (W), goals scored per match (GSM) and goals allowed per match (GAM).
The Wins column was dropped to enable the final output align with the requested output.
It concludes by returning the categorized and summarized EPL standings as at the inputed date and season.

**Reflection:**

**Key challenges:** I encountered included the management of date format variations, the maintenance of 
column name consistency across seasons, and the aggregation of match-level data into team-level 
summaries.

**The function performs the following operations:** Downloads the corresponding data file according to 
the specified season, standardizes date formats, and computes summary statistics for each team using
conditional statements.

**Contribution:** The function offers a methodical framework for examining and condensing EPL match data,
thereby providing valuable insights into the performance of teams within a designated timeframe. 
This tool aids stakeholders in comprehending team standings, discerning the most successful teams, 
and scrutinizing patterns in points earned, goals scored, and match outcomes.

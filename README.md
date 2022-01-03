# NFL_Data_Clustering
 Indentifying NFL team archetypes using kNN clustering

## Project Description:
 This is a kNN cluster anlaysis of NFL seasonal team data that attempts to identify distinct team
 archetypes and evaluate how these archetypes may relate to a team's success measured by regular
 season wins. The notebook includes some data exploration, data preparation, kNN clustering, 
 cluster evaluation of results, and conclusions.
 
## Python Libraries:
 Numpy
 Pandas
 matplotlib
 scikit learn
 
## Data:
 
 Source: Pro-football-reference.com
 
 Description: The dataset used in this analysis contains seasonal team offensive and defensive 
 stats for every NFL team from the years 2010-2019. It is a combination of several datasets
 accessible from pro-football-reference.com. The data includes regular season data only, and
 therefore, measures of team success are based on regular season wins and not playoff or superbowl
 outcomes.
 
 320 Observations
 
 53 Features
 
 ### Feature Descriptions:
 
  ****Offensive Stats****
  Rk -- Rank
   This is a count of the rows from top to bottom.
   It is recalculated following the sorting of a column.

  Tm -- Team Name

  G -- Games played

  PF_Off -- Points Scored by team

  *Yds_Off -- Total Yards

  *Ply_Off -- Offensive Plays: Pass Attempts + Rush Attempts + Times Sacked

  *Y/P_Off -- Yards per Offensive Play
   (Rush + Pass Yards)/( Pass Attempts + Rush Attempts + Times Sacked)

  *TO_Off -- Team Turnovers Lost

  FL_Off -- Fumbles Lost by Player (since 1994) or Team

  *1stDTot_Off -- First Downs

  Cmp_Off -- Passes completed

  AttPass_Off -- Passes attempted

  YdsPass_Off -- Yards Gained by Passing
   For teams, sack yardage is deducted from this total

  TDPass_Off -- Passing Touchdowns

  Int_Off -- Interceptions thrown

  *NY/Apass_Off -- Net Yards gained per pass attempt
   (Passing Yards - Sack Yards) / (Passes Attempted + Times Sacked)
   Minimum 14 attempts per schedule game to qualify as leader.
   Minimum 1500 pass attempts to qualify as career leader.

  1stDPass_Off -- First Downs by Passing

  AttRush_Off -- Rushing Attempts (sacks not included in NFL)

  YdsRush_Off -- Rushing Yards Gained (sack yardage is not included by NFL)

  TDrush_Off -- Rushing Touchdowns

  *Y/Arush_Off -- Rushing Yards per Attempt
   Minimum 6.25 rushes per game scheduled to qualify as leader.
   Minimum 750 rushes to qualify as career leader.

  1stDRush_Off -- First Downs by Rushing

  Pen_Off -- Penalties committed by team and accepted

  PenYds_Off -- Penalties in yards committed by team

  1stPy_Off -- First Downs by Penalty

  Sc%_Off -- Percentage of drives ending in an offensive score

  TO%_Off -- Percentage of drives ending in an offensive turnover


  ****Defensive Stats****
  PF_Def -- Points Scored by team

  *Yds_Def -- Total Yards Against

  *Ply_Def -- Offensive Plays: Pass Attempts + Rush Attempts + Times Sacked

  *Y/P_Def -- Yards per Offensive Play
   (Rush + Pass Yards)/( Pass Attempts + Rush Attempts + Times Sacked)

  *TO_Def -- Takeaways

  FL_Def -- Fumbles Lost by Team

  *1stDTot_Def -- First Downs

  Cmp_Def -- Passes completed

  AttPass_Def -- Passes attempted

  YdsPass_Def -- Yards Gained by Passing
   For teams, sack yardage is deducted from this total

  TDPass_Def -- Passing Touchdowns

  Int_Def -- Interceptions thrown

  *NY/Apass_Def -- Net Yards gained per pass attempt
   (Passing Yards - Sack Yards) / (Passes Attempted + Times Sacked)
   Minimum 14 attempts per schedule game to qualify as leader.
   Minimum 1500 pass attempts to qualify as career leader.

  1stDPass_Def -- First Downs by Passing

  AttRush_Def -- Rushing Attempts (sacks not included in NFL)

  YdsRush_Def -- Rushing Yards Gained (sack yardage is not included by NFL)

  TDrush_Def -- Rushing Touchdowns

  *Y/Arush_Def -- Rushing Yards per Attempt
   Minimum 6.25 rushes per game scheduled to qualify as leader.
   Minimum 750 rushes to qualify as career leader.

  1stDrush_Def -- First Downs by Rushing

  Pen_Def -- Penalties committed by team and accepted

  PenYds_Def -- Penalties in yards committed by team

  1stPy_Def -- First Downs by Penalty

  Sc%_Def -- Percentage of drives ending in an offensive score

  TO%_Def -- Percentage of drives ending in an offensive turnover

  W -- Total Team Wins

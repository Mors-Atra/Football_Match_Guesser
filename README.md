# Football_Match_Guesser
This python script uses an algorithm based on probability calculation to predict the outcome of a match with a high probability of being correct. WARNING! THIS SCENARIO CANNOT PREDICT 100% CONSISTENTLY! THE BOT USES THE DATA IN THE PREVIOUS SEASON SO IT MAY NOT BE 100% VALID FOR THIS SEASON! PLEASE DO NOT BET LARGE AMOUNTS OF MONEY ON MATCHES RELYING ON THIS BOT! Please further read if you want more explanation and have a good prediction :) 

# BEFORE YOU START;

Some of the numbers here will be decimal where it seems like it shouldn't be. For example average goal expected to be scored by team X will be something like 1.57. But, just like nobody has 2.4 children, nobody scores 1.57 goals — this is only an expected value. It's the average number of goals expected to be scored by team X if the match were played again and again, heaven forbid. So this not an ACTUAL value, it is an expected one!

# How does this work?

This bot works with calculating 2 aspects of a team. Their attack power and defence weakness. Also, it looks to the average goals scored for an home and an away team in a specific league.

# Calculating the average number of goals scored for a team in a specific league.

Up first, we have to calculate average goals scored for a team in a whole season. To do this, we need to add all of the scored or conceded goals in any league. This could be any league like Süperlig, LaLiga, Premier League etc. Once you added up all of the total goal scored or conceded in any league, you have to divide it by the total number of teams there are in the league. The number that you have right now is the average goal scored in a season for a team. (The number you can have can be something like 43,25 so please round the number you have!)

# Calculating the attack power of a team

Next, you have to find a team's attack power. To do that, you have to divide the average goal scored in a season for a team with all goals scored during the season by the team whose attacking power you want to find. For example if I wanted to calculate the Fenerbahçe's attack power (A team in the Süperlig, Turkish main league), I would have to divide their scored 73 goals in a whole season with average goal scored in a  season for a team (It is 53 goals for Süperlig). This would give me 1.37 which will be the attack power of fenerbahçe. That means that fenerbahçe scored 37% more than the average goals scored in a whole season. Now hopefully, if-didn't manage to confuse you, we can take a look at how to calculate a team's defence weakness.

# Calculating the defence weakness of a team

Up next, we have a teams defence weakness. Now we have 2 data in our hands. Average goals scored in a whole season which is 53 for Süperlig ONLY. This varies depending on your'e league. Now we know that to calculate a team X's attack power, we have to divide the goals scored by the team X in a whole season by average goal scored in a  season for a team. For the defence weakness of team X, you just have to divide the goals conceded by team X by average goal scored in a season for a team. For example if I wanted to calculate the defence weakness of Gaziantep S.K (A team in the Süperlig), I would have to take their conceded goals and divide them by average goal scored in a season for a team which would give me 0.90. This means that Gaziantep S.K conceded 10% more goals than the average. Hopefully this makes a bit more sense and lets move on!


# Calculating the average goal scored for a home team

Now this is pretty similar to calculating average goals scored. All we need to do is add up the goals scored by all teams that played in home, divide this number by the number of teams and divide the final number by half of the matches played in a league. The reason we do this is that only half of the games in a league are home games for one team. The final you have right now is the average goal scored for a home team. Now if you manage to came here, we have a one final data to resolve and that is the average goal scored for away team!


# Calculating the average goal scored for a away team

To calculate this. Just do the same thing as calculating the average goal scored for a home team but instead of adding all of the goals scored by teams that played in home, just add all of the goals scored by teams that played in away and the number you have is the average goal scored for an away team!

# After all of theese steps, you should have;
Desired team's attack power,
Desired team's defence weakness,
Average goals scored by any home team,
Average goals scored by any away team. If the numbers confuse you because they are decimal, do not worry beacuse as said in the above, these are expected values not ACTUAL ones. Now that you gathered all of the data requried to calculate a match's outcome, Its time for the fun part!

# Calculate a match's outcome

To calculate match's outcome, we have to first find number of goals a team is expected to score. For example lets calculate the outcome of Fenerbahçe-Beşiktaş match. Lets also say that fenerbahçe is the home team. The formula for this calculation is;

(Fenerbahçe's attack power) * (average home team score per match) * (Beşiktaş's defence weakness)

The outcome of this calculation would give us something like 1.77. However there is no such thing as 1.77 goals so we have to round the expected value and we can say that probably, fenerbahçe would score 2 goals if they were the home team. For beşiktaş, the calculation follows like this:


(Beşiktaş's attack power) * (average away team score per match) * (Fenerbahçe's defence weakness)


This would leave us with 1.17 and when we round it, beşiktaş will probably score 1 goals in a match with fenerbahçe when they are the away team. So we can say that a Fenerbahçe-Beşiktaş match will en up in a score of 2-1 if Fenerbahçe is the home team. If Beşiktaş was the home team, their chances of scoring a goal would increase slightly. So hopefully, you now understood how this bot uses this algorithm to calculate an outcome of an match. Up next, if you are not interested in Süperlig teams, you can add your'e own teams in the .INI file yourself! This is how;


# Adding your'e own team


First, open the .INI file and look at thye format. It follows like this;

---------------------
[TEAM NAME THAT YOU WANT TO ADD IN ALL CAPS]

your'e_teams_attack_power_variable = your'e team's attack power

your'e_teams_defence_weakness_variable = your'e team's defence weakness

(OPTIONAL) your'e_teams_scored_goals_for_a_whole_season_variable = your'e_teams_scored_goals_for a_whole_season

(OPTIONAL) your'e_teams_conceded_goals_for_a_whole_season_variable = your'e_teams_scored_conceded_for a_whole_season

---------------------
After you done this, you are all good to go. DON'T FORGET TO CALCULATE THE TEAM'S DATA ACCORDING TO THEIR OWN LEAGUE! ALSO, AVERAGE GOAL SCORED FOR AN HOME TEAM OR AVERAGE GOALS SCORED FOR AN AWAY TEAM DATAS ARE ALL CALCULATED ACCORDING TO SUPERLIG, SO THE CALCULATION MAY NOT BE ACCURATE!


Made by @Mors_Atra






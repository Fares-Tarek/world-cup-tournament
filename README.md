# world-cup-tournament
a program to run simulations of the FIFA World Cup.

In soccer, teams are given FIFA Ratings, which are numerical values representing each team’s relative skill level. Higher FIFA ratings indicate better previous game results, and given two teams’ FIFA ratings, it’s possible to estimate the probability that either team wins a game based on their current ratings. The FIFA Ratings from two previous World Cups are available as the May 2018 Men’s FIFA Ratings and March 2019 Women’s FIFA Ratings.

Using this information, we can simulate the entire tournament by repeatedly simulating rounds until we’re left with just one team. And if we want to estimate how likely it is that any given team wins the tournament, we might simulate the tournament many times (e.g. 1000 simulations) and count how many times each team wins a simulated tournament.

The simulate_game function accepts two teams as inputs (recall that each team is a dictionary containing the team name and the team’s rating), and simulates a game between them. If the first team wins, the function returns True; otherwise, the function returns False.

The simulate_round function accepts a list of teams (in a variable called teams) as input, and simulates games between each pair of teams. The function then returns a list of all of the teams that won the round.

In the main function, notice that we first ensure that len(sys.argv) (the number of command-line arguments) is 2. We’ll use command-line arguments to tell Python which team CSV file to use to run the tournament simulation. We’ve then defined a list called teams (which will eventually be a list of teams) and a dictionary called counts (which will associate team names with the number of times that team won a simulated tournament). Right now they’re both empty, so populating them is left up to you!

Finally, at the end of main, we sort the teams in descending order of how many times they won simulations (according to counts) and print the estimated probability that each team wins the World Cup.

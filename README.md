# Predicting NBA Attendance/Capacity with Linear Regression - Metis Project 2
Rudy Wang

## Background:

Yes, I'm another one of the many NBA fans that wanted to pursue a project using basketball analytics. You can imagine my excitement slightly dip when I went on Google and did a quick search of "NBA Data Science Projects" and saw endless pages of the same, rote projects: Predicting MVP, Wins, or even the salaries of players, and many more. I found myself wanting to do something in the space that would be a bit outside of the box and different than the other established NBA topics online.

That's when the idea of predicting NBA attendance popped up. At the end of the day, the NBA organization is a business with a focus on making money for itself and despite viewership via television or cord-cutter apps, physical attendance garners the most money for teams as attendance goers snatch up merchandise, buys treats and drinks at the many venues within the stadium, and obviously the tickets to attend the game. 

Because every stadium has a different capacity, it would be difficult to compare the actual raw numbers of attendance among all stadiums. My focus shifted to predicting the % filled at each stadium:

<img src="https://latex.codecogs.com/gif.latex?\%&space;Filled&space;=&space;\frac{Average&space;Home&space;Game&space;Attendance}{Total&space;Arena&space;Capacity}\" title="\% Filled = \frac{Average Home Game Attendance}{Total Arena Capacity}\" />

It would be interesting to see whether I could accurately predict what factors cause an NBA stadium to be filled up or not at all - do team stats, amount of all-stars, or even city population have any influence on the attendance?

## Mission:

The initial thought was to see if there was any relationship on basic/advanced basketball stats with predicting NBA attendance at the varying stadiums. I would use web scraping and linear regression tools to accomplish my set out mission.

## Updates: 

## Trust the Process:

1. Web scraped Basketball-Reference (2000-2019 Individual Team Stats) for each team (adjusted for changes in team names, when applicable i.e. New Jersey Nets -> Brooklyn Nets). Converted into CSV file.
2. Web scraped Basketball-Reference (2000-2019 NBA All Stars) for each team to extract out the number of all-stars per team. Converted into CSV file.
3. Extracted stadium name and capacity information from Wikipedia into Excel.
4. Extracted number of championships for each NBA team at HISPANOSNBA into Excel. 
5. Read CSV and Excel files into a primary dataframe to construct Linear Regression models for training and validation.
6. Took the best training model and tested to output results.

## Conclusion and Beyond.

My R-Squared values for testing for all of my models yielded negative values. This tells me simply that NBA game statistics aren't enough to predict the actual % filled number of a NBA stadium. There are other factors that I must be missing that may be much more important than the in-game stats such as social factors that I did not include the first time around. 

To further improve my results, I decided to take another stab by gathering social information that I did not take into consideration before:

1. North America's city populations from 2000-2019: Macrotrends.net, Biggestuscities.com, Census.gov.
2. NBA Superstar Legacy (explained below).

What is NBA Superstar Legacy? I created this as an extra feature for my dataset, because NBA fans are heavily influenced by face of the franchise players: Michael Jordan, Shaquille O'Neal, Kobe Bryant, Lebron James, etc. My previous dataset failed to capture how "popular" teams are due to a legacy lingering effect from talented players that exploded within their respective teams. As a result, I wanted to do my best to capture this important factor: I grabbed the top 100 players sorted by their Player Efficiency Rating (PER) - which is one of the most used single statistic to capture the 'best' players that played or are playing in the NBA - and assigned a 1 to teams that had a influential superstar/s between 1995 and 2019 and a 0 to teams that did not possess any of the players. The players selected were based on my own sense of domain knowledge:

1. Michael Jordan - CHI
2. Lebron James - CLE
3. Anthony Davis - NOP
4. Shaq/Kobe - LAL
5. Tim Duncan - SAS
6. Karl Malone - UTA
7. Clyde Drexler - POR
8. Kevin Durant - OKC
9. Tracy McGrady - HOU
10. Stephen Curry - GSW
11. Dwyane Wade - MIA
12. Dirk Nowitzki - DAL
13. Dwight Howard - ORL
14. Patrick Ewing - NYK
15. Allen Iverson - PHI

## Final Conclusion.

My final model used the following features: wins, capacity, number of all stars, population, and superstar legacy to achieve an improved R-Squared value .52! It's quite clear that a highly populated stadium is more than just in-game stats. External social factors matter very much and recommending finding the face of a franchise in combination with a densly populated city would be the best way to achieve higher ticket sales for attendance.





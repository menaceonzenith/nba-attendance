# Predicting NBA Attendance/Capacity with Linear Regression - Metis Project 2
## Rudy Wang

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
5. Read CSV Files into a primary dataframe to construct Linear Regression models for training and validation.
6. Took the best training model and tested to output results.

## Conclusion and Beyond.

My R-Squared values for testing for all of my models yielded negative values. This tells me simply that NBA game statistics aren't enough to predict the actual % filled number of a NBA stadium. There are other factors that I must be missing that may be much more important than the in-game stats such as social factors that I did not include the first time around. 

To further improve my results, I decided to take another stab by web scraping more information.




# NHL reports using Power BI
For this project, I am using Power BI to get and transform data, and build a variety of visualizations for reports.    

## Getting data
The source of my data is coming from the free [NHL API.](https://gitlab.com/dword4/nhlapi) Some API endpoints that I will be using include:

* All teams: https://statsapi.web.nhl.com/api/v1/teams
* A team’s current statistics: https://statsapi.web.nhl.com/api/v1/teams/54?hydrate=stats(splits=statsSingleSeason)
* Statistics for each player of a team: http://statsapi.web.nhl.com/api/v1/teams/54?hydrate=roster(person(stats(splits=statsSingleSeason)))

### Team Data
My first step is to work with the team data from the NHL API. It can be found here: https://statsapi.web.nhl.com/api/v1/teams. Since JSON represents data as a structured hierarchy, I have to go in and expand every list and then expand each record. In addition to this, rename and update data types for each column. After I've finished getting and transforming the data, this is what I've ended up with.

![Team Data](.../assets/images/nhlreports/teamsdata2.gif)
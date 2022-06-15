# List of Dataset Links for Project 4

The following list of links should serve as a great starting point for putting together problems and/or ideas for your Project 4:

https://www.drivendata.org/competitions/  
https://www.kaggle.com/  (One of the best places for data sets)  
https://data.world/  
https://www.challenge.gov  
https://archive.ics.uci.edu/ml/index.php  
http://www.stat.ufl.edu/~winner/datasets.html  
https://www.reddit.com/r/datasets/  
http://exploresara-sara-tx.opendata.arcgis.com/  
http://nowdata.cinow.info/indicators/local-open-data-portals  
https://data.fivethirtyeight.com/  
https://toolbox.google.com/datasetsearch  
https://github.com/brohrer/academic_advisory/blob/master/use_cases.md  
https://explore.openaire.eu/  
https://blog.datasciencedojo.com/30-datasets-to-uplift-your-skills-in-data-science/ (Would recommend going for Intermediate or Advanced Datasets here)  
https://developer.ibm.com/exchanges/data/  
https://github.com/awesomedata/awesome-public-datasets  
https://mran.microsoft.com/web/packages/fivethirtyeight/vignettes/fivethirtyeight.html  
https://data.worldbank.org/  
https://www.imf.org/en/Data  
https://www.transit.dot.gov/ntd/ntd-data  
https://gosa.georgia.gov/downloadable-data  
https://www.usaspending.gov/#/download_center/custom_award_data  

## Sports Related Data
Many of the cooler Sports Play-by-Play date scraping packages are done in R (nflfastR, hoopR, etc.), but thankfully the creators of those projects set up a data repository in Github that you can read directly into your notebook.

### NFL Data from nflfastR/nflverse
The nflfastR package scrapes nfl data from several sources, and the play-by-play data is stored in several different formats at the following link: [nflfastR Data](https://github.com/nflverse/nflfastR-data/tree/master/data).  

From there, you can click on the file you want. So if you wanted the 2021 Play-By-Play data, click on play_by_play_2021.csv.gz.  On the next page that comes up, you can either download the file to your machine by clicking on download, or you can read it in directly by right-clicking the "View raw" link and Copy Link Address.  Then you can run the following line in your Jupyter Notebook pasting in the link you copied from the nflfastR data repository to read in the data:

```python
pbp = pd.read_csv('https://github.com/nflverse/nflfastR-data/blob/master/data/play_by_play_2021.csv.gz?raw=true', compression='gzip', low_memory=False)
pbp.head()
```
You can also find additional data on [nflverse](https://github.com/nflverse/nfldata/tree/master/data).

### NBA and College Basketball Data from hoopR

Similar to nflfastR, the [hoopR Data](https://github.com/sportsdataverse/hoopR-data) is in Github.  At that link, you can click on either the nba or mbb folders for the NBA or Men's College Basketball data respectively.
From that folder tree, you can then click on the pbp folder for play-by-play data, the player_box folder for player specific box scores, schedules for Team schedules, or team_box for Team Box Scores.  Each folder has four different types of files.

As above, if you wanted Team Box Scores for the 2021-2022 Men's Basketball Season using the parquet file format, you can click on the github file folders in order from mbb, team_box, then parquet.  Click on the team_box_2022.parquet file, then right click on View Raw and Copy Link Address.

```python
mbb_pbp = pd.read_parquet('https://github.com/sportsdataverse/hoopR-data/blob/main/mbb/team_box/parquet/team_box_2022.parquet?raw=true')
mbb_pbp.head()
```


### Other Sports

[PySport](https://opensource.pysport.org/) keeps a list of various sports packages to use to scrape/get data as well including Soccer, Hockey, Baseball, and more.  Code and packages are updated frequently so there may be different ways of getting data than what was demonstrated above.

Keep in mind that the data scraped, while cleaned up by the scraping process, still require a great deal of cleaning for analysis.  There are a few python-related tutorials on the NFL data.

# Football_Scraping

This project was meant to scrape general college football data for each major college football team, and then dump that data into a CSV. The data will be used in another project <a href="https://github.com/havelljd/College_Football_Analytics">here</a>. I scraped 15 years of data from 70 college football teams.

I'm a huge college football fan, and so I wanted to run some analysis on data from games. After checking out some Kaggle data and a few other datasets, there wasn't one that grabbed the stats for the teams that I wanted. So, I decided to scrape the data from www.sports-reference.com, as the format and info there looked great. Here's a screen grab of the table of data that I grabbed.

<img width="1003" alt="image" src="https://user-images.githubusercontent.com/8563653/209899071-32c4c565-e25c-44cb-895c-879581fec285.png">

I also included the coach of each team and the conference as columns in my pandas dataframe.

You can see in the image, there's a "share and export" link, but in order to get 15 years of the 70 major college football teams, scraping is the only way to go. Otherwise, I'd be downloading 1,050 different files! Scraping is the obvious choice.

Scraping the site took over 2.5 hours at a time, as the terms of use of sports-reference was to only send 20 requests per minute max (or you get blocked for a while...which happened to me :). As fun as it is waiting that long for the scraper to finish, I can tell you it felt like a lot longer than 2.5 hours each time I ran it (and when the result wasn't what I wanted because of a missing comma in my code...ugh). Here's the output of my scraper printing the team and year it's scraping (it did this for all 70 teams). 

<img width="150" alt="image" src="https://user-images.githubusercontent.com/8563653/209899287-ae258958-4489-4c98-8d54-4bafcec643dd.png">

After I was done scraping, I didn't want to continually scrape the site for the data for use afterward, so I dumped the dataframe to a .csv and uploaded that to the cloud for easy future use. The .csv file is located at https://byu.box.com/shared/static/8arjj9k9sijfz8f93gqle5ig0lmsxxxl.csv.

<img width="1129" alt="image" src="https://user-images.githubusercontent.com/8563653/209899691-9963538b-039c-41ba-8087-667d57e8227b.png">

Even though this data was meant to be used for a separate analytics project, I couldn't help myself and did some quick coaching wins visualizations. I organized the data into 3 columns; coach, wins (that coach had), and losses. This helped track coaches even if they switched schools; for example, Bronco Mendenhall coached at BYU and Virginia in the past 15 years. This visualization included wins and losses at both schools, and I sorted coaches by total wins across all schools. I plotted this out with matplotlib.

<img width="1157" alt="image" src="https://user-images.githubusercontent.com/8563653/209899891-bf0c9ef5-fee4-48d5-8abd-3154c36f8cb7.png">

The visualization was only meant to easily see the most "successful" coaches in college football, regardless of schools. In the future, it would be interesting to see coaches lifetime earnings, along with wins and schools coached at (and success at each school).

More analysis on this data is being done in <a href="https://github.com/havelljd/College_Football_Analytics">this repository</a>.

# FramingIndex
A Juypter Notebook outlining a new statistic for baseball which judges a catcher's ability to frame a pitch

Demo Video: https://youtu.be/VGjEIuqUMzs

## Introduction
One of my favorite positions in baseball has always been catcher. My favorite player since I was very young has been Yadier Molina. It is well documented that there is not a great way to measure the value of catchers. Stats like wins above replacement (WAR) simply do not paint an accurate value for catchers compared to other players on a team.

To measure the value of a catcher we need to prioritize what is most important for the position. In my opinion one factor of a catcher's game that is under represented in sabermetrics is the catcher's ability to frame a pitch. Framing a pitch is when the catcher moves their glove to catch the pitch in a way which makes it look like a strike. This way a good catcher can get strike calls for his pitcher hat less experienced catchers may not. Similarly, a less experienced catcher may cost his pitcher strikes if he does not make a convincing catch of a pitch that is in the strike zone.

In order to quantify a catcher's ability to frame a pitch, I will be going through statcast data to count the number of strikes called that were outside of the zone and the amount of called balls in the strike zone. While we have no absolute proof that framing was the reason for the call, I think it is the best indicator we have in the data without knowing much about an umpire's strike zone.

I am going to use a month's worth of statcast data to test my statistic. I picked the period between the end of July and August 2018 for my analysis because it is in the late to middle part of the season, so players and umpires should have had time to settle into a rythm. I only used a month of data because statcast data tends to crash in my experience if more than a few months of data is used. I also wanted to limit the dataset because I had to use the playerID lookup function, which takes time to run.

## Calculation

The following is an explanation for my statistic, the Framing Index:

[[(number of balls called strikes) - (number of strikes called balls)] / [(total called strikes)]]*100

## Conclusion
After running the statcast data I came up with the framing index for 5 different catchers who had the most balls called strikes for the period between the end of July and August 2018. The catchers were as follows:<p>
•	Yasmani Grandal, Los Angeles Dodgers 0.179<br>
•	Salvador Perez, Kansas City Royals - 0.118<br>
•	J.T. Realmuto, Miami Marlins - 0.179<br>
•	Austin Romine, New York Yankees - 0.302<br>
•	Mike Zunino, Tampa Bay Rays - 0.245<br>

Austin Romine leads the group with a framing index of 0.302, the Yankees catcher had a notably impressive 2018 campaign as he fought to retain his position on the starting roster according to Yankee's blogger pinstripe alley.

Yasmani Grandal and J.T. Realmuto are two names you would expect to find on this list. The two are frequently found on lists of the best catchers in baseball for their ability to "steal strikes". I think if I was able to run a full season of statcast data, these two names would remain on the list.

There are limitations to the Framing Index however. Framing Index on its own is not an all-encompassing metric to judge catchers by. Things like blocked pitches, throw outs and some offensive stats would also be taken into account. This is illustrated by Yasmani Grandal's now infamous meltdown during the Dodger's 2018 postseason campaign, where he allowed a slew of past balls that directly resulted in runs for the other team.

There is also a lot of debate as to how much framing a catcher can actually get away with in today's mlb. Umpires are expected to make the right call and are very aware of catcher's trying to frame the ball. This makes it difficult for catchers to influence the call the umpire makes. Still, the fact we see a couple of the best catchers in baseball show up on this list could mean that pitch framing still plays a part in today's mlb.

One thing that could improve the accuracy of this statistic is if we had some sort of metric about each umpire's strike zone. Each home plate umpire has a slightly different size and shape to their zone, and it would be helpful to normalize this data before running the framing index calculation. This would serve the same purpose as a park factor in other calculations.

Overall, I think framing index is a good metric to use in combination with other statistics to measure the effectiveness of a catcher. This statistic relies on the human factor to umpire's calls and would be rendered useless should they ever implement an electronic strike zone or something like that. However, for the time being, it remains a good indicator of a catcher's ability to frame a pitch.

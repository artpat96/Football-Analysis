# Football_Analysis_Project 

<b> Project description (available in polish language in .pdf file): </b>

The football Analysis project involved taking the data of selected players from the last 3 seasons and structuring it. The data was transferred to Excel (attached file in .xls format) and converted to .csv format to upload it to Python via Jupyter Notebook.
The project focused on processing the data properly, starting with loading it in the wanted form (using the NumPy library) and loading the .csv file as a main table (using the Pandas library).
The data then was converted accordingly, so as to pull out interesting statistics and make comparisons of players' playing styles. The project focuses on skills such as:
- loading and appropriate implementation of data (arrays, dataframe, tables creation)
- data manipulation with the help of the Pandas library (grouping the data, extracting average, maximum and minimum scores from given columns, extracting specific data of interest from the table)
- creation of additional columns to our main table with new calculations
- creation of various forms of charts using Matplotlib and Seaborn libraries
- customization of these charts for analysis purposes
- creating functions to simplify the creation of multiple charts
- drawing conclusions from the created analysis (description below)

# Players' Analysis

The following analysis is divided into 4 parts and it's aim is to get answers to the following questions:
- what is the position of each analyzed footballer (defender, playmaker, winger, striker)?
- what is the best player in each position?
- who had the best individual season?
- who had the most consistent form over the 3 seasons, is it possible to identify the biggest star of the league?

<b> PART 1 </b>

At the very beginning, it is worth looking at players who regularly score less than 10 goals per season.
![def_fwd](https://user-images.githubusercontent.com/111128309/218095610-6a6241b0-4b13-4445-911b-88efe4da244c.jpg)

Cancelo and Alexander-Arnold have not crossed the 10-goal barrier in any season. So they are clearly defenders. Next, we look at the ones who regularly scores above 17 goals per season. On this basis, we can say with certainty that Salah and Kane are strikers. Mane, Son and Vardy also scroll down the list one time each, so they should be examined from that angle. The easiest way is to check the statistics of all shots taken, that way you can see how close to the opponent's goal a particular player plays. 
-	Sadio Mane:
![Mane](https://user-images.githubusercontent.com/111128309/218096741-b4f735fa-3076-4521-9c07-4eac136d98f9.jpg)
![Mane2](https://user-images.githubusercontent.com/111128309/218096757-ac3cb211-4434-472f-a45b-4bebb0eefec5.jpg)

Mane shoots a lot, but we also see that he dribbles a lot. Moreover we can see that over time his dribbling decreases and his shooting increases. This means that his style has probably evolved slightly. From being initially a typical scrummager, he has become a player who plays closer to the middle. He is then something between a winger and a striker. However, it can be seen that he dribbles, next to Zaha, most often in the league. Therefore, for the purpose of analysis, we will assign him the position of a winger, but we will also check how he compares with typical strikers.
-	Jamie Vardy:
![Vardy](https://user-images.githubusercontent.com/111128309/218096773-f5a3a244-f955-4bf5-b0ab-da2c84203682.jpg)

You can see that Vardy can score a lot of goals by taking few shots. This means that he probably shoots from very close range, so his field position is that of a striker. In addition, Vardy creates few situations, which reinforces our belief that he is the type of striker who waits for a pass from his teammates.
-	Son:
![Son](https://user-images.githubusercontent.com/111128309/218096842-f965925d-23ef-40e2-b625-bb51d9f992f4.jpg)
![Son2](https://user-images.githubusercontent.com/111128309/218096857-ef8ee21c-0cf2-451a-ab43-4f59395e11db.jpg)

He is a very interesting player, probably the hardest to characterize. He certainly doesn't take many shots, but he can score quite a few goals. He dribbles less than Mane, but can create a lot of situations for other players and has a lot of key passes. He is likely to be something between a playmaker, a winger and a striker. For the purposes of analysis, we'll assign him to the playmaker position, but we'll also look at how he compares to wingers.
-	Wilfried Zaha - He's a typical winger. Most dribbling in the entire league. Consistent number of situations created and shots per season.
![Zaha](https://user-images.githubusercontent.com/111128309/218096906-da28f041-23e1-4665-bf3b-05a20489a591.jpg)

-	Kevin de Bruyne - He's a typical playmaker. Most assists, created chances, key passes. Unrivaled in this regard, despite fewer minutes than the competition.
![KdB](https://user-images.githubusercontent.com/111128309/218096876-d856e09e-ea0a-4d0d-9e81-26822a443379.jpg)

<b> PART 2 </b>

So we have grouped players. Next, we will try to characterize each player in greater detail and select the best player in a given position.
The defenders in the list are the side defenders. They have more offensive statistics than central backs, and these are the statistics that we focus on in the following analysis. By the number of assists, chances created (centering or long passes) and key passes, it is clear that Trent Alexander-Arnold is unrivaled by Cancelo over 3 seasons. It gets more interesting when comparing other positions (the analysis of offensive stats somewhat forces this), which is why I decided to add TAA to the analysis of playmakers (with stats of creating chances he most resembles such a player profile).

<i><b> de Bruyne vs Son (vs TAA) </i></b>

In this part of the analysis we ignore scored goals. In this statistic Alexander-Arnold, as a defender, does not stand a chance with the other players. However, his ability to make accurate passes is exceptional and is worth a look.
![Playmakers](https://user-images.githubusercontent.com/111128309/218097429-c144dd2a-1c51-471d-b89c-b95efb0e2ce0.jpg)

De Bruyne has played fewer minutes than the other players, but numerically he is still ahead of most of them. Not surprisingly, then, taking into account the statistics of passes and chances per minutes, his advantage over the rest of the rate grows even more. We also see that Trent performs better than Son in both of these statistics, but we can see that the 2019/20 season was very successful for him in terms of efficiency. Despite a relatively small number of key passes, these were very qualitative situations (the best ratio of assists to such passes). He is also the best dribbler of the three, and is much more often involved in such actions, which may suggest that at times he is closer to a winger than a playmaker after all. However in this battle, de Bruyne's victory is indisputable.

<i><b> Zaha vs Mane (vs Son) </i></b>
![Wingers](https://user-images.githubusercontent.com/111128309/218105030-f32f35c9-3d24-4e53-80e7-491452c39880.jpg)

Zaha performs the weakest of the entire list. The only thing he dominates in is the number of dribbles. However, he loses all other competitions. Mane's and Son's dribbling is almost identical, except for the 2020/21 season, where Mane's dominance is evident. In addition, it can be noted that Mane seems to be a better shooter than Son and probably plays more as a striker. Son, on the other hand, is characterized by better passes. So it comes out that the only real winger in the lineup is Zaha, but he loses all the important competitions he takes part in. Mane is more of a winger-striker type, while Son is a winger-playmaker. Qualitatively they both surpass Zahe, but through different characteristics it is hard to choose the best of them.

<i><b> Salah vs Kane vs Vardy (vs Mane) </i></b>
![Forwards](https://user-images.githubusercontent.com/111128309/218105069-c5e94b9b-e29b-46ff-95a7-0e882944dc23.jpg)

Vardy is certainly the most effective striker. In two seasons he has the best goals per minute ratio (once equally to Salah) and each time he has the best goals per shots ratio. The chart of dribbles per shots shows that Mane engages in such actions much more often than the other players on the list. Only in the last season his dribbling numbers are close to the rest of the players, but even then he is far from the shooting efficiency of all the rest. Salah takes the most shots of the entire roster. Analyzing all 4 charts at the same time, it is also possible to see that he is the most equal of the players compared here (good goals per shot ratio, good number of dribbles, very many goals and goals per minute ratio). Kane, on the other hand, looked best in the 2020/21 season when he dominated the goals and shots per minutes ratio. His efficiency, on the other hand, in that season was similar to Salah and slightly worse than Vardy.

<b> PART 3 </b>

It's time to compare the best individual performances. This is difficult because you have to take into account all the statistics of the players in question, and they often have different tasks on the field. However, the most important statistic is the number of goals and assists.

![BI](https://user-images.githubusercontent.com/111128309/218113261-6a635e36-7095-418b-b5b3-86644cba8635.jpg)

From these lists, it is easy to pick out the 3 best and most equal performances of the players and after that we can move on to a deeper analysis of these 3 seasons.

![Bestindividual](https://user-images.githubusercontent.com/111128309/218113337-90315eba-fa01-42ce-aa09-32c25710d818.jpg)

![GA_plot](https://user-images.githubusercontent.com/111128309/222784313-8913da7d-d823-4428-9382-e24235c0621a.jpg)

All three have played a similar number of minutes in those years. After adding up the goals and assists, we see that Kane has 37 points, Salah has 36, while de Bruyne has 33. The first two, moreover, have a very similar number of shots taken and successful dribbles. However, in the statistics of chances created and key passes, Salah seems to be clearly in the lead. On top of that, he has played 324 minutes less than Kane, which puts him in the lead. De Bruyne is clearly a different type of footballer. The number of his assists, passes and created chances is on a completely different level from the rest. However, he is not as good a scorer as Salah. They are different footballers and it seems that comparing them on a one-to-one basis is simply impossible.


<b> PART 4 </b>

However, it is also worth taking a long-term view.

![BestConsistency](https://user-images.githubusercontent.com/111128309/218113472-4a14113b-d786-4401-81c5-08dffb544d3b.jpg)

De Bruyne usually plays fewer minutes than Salah, which introduces a new factor into our analysis - injury susceptibility. Because of this, he is not able to put up an equal fight with his competitors on a long-term basis (over the course of a season) every year.


![Consistency](https://user-images.githubusercontent.com/111128309/218113537-a20e58d4-d327-43b4-9006-5d2b5fa846cd.jpg)

We also see that Salah appears in the statistics of goals and assists 3 times, while other players only once. All this makes it necessary to think of him as the biggest star and probably the best player in the league in the 2019-2022 period.

If we focus deeper on his playing style, we can see that he is giving the most shots in the whole league.

![GpTS](https://user-images.githubusercontent.com/111128309/235902514-a5f9fbc9-b27e-4f9a-9cc9-0806529fcfb3.jpg)

Moreover, he is a very cosistent player. His total shots per season are always in the range of 126-139, so differences between each season are very small. The same is true of his goal statistics, where the difference between seasons is a maximum of 4 goals.

![GaPM_Mo](https://user-images.githubusercontent.com/111128309/235903591-2f0295cb-b8f1-40b7-a832-1d5aaebe75ba.jpg)

His goals and assists per minutes stats are on the very high level, as he is the first player to appear twice on this list.

![GApM](https://user-images.githubusercontent.com/111128309/235903955-63c69a89-f690-4d81-b796-65c01d5339c3.jpg)

From the chart we can also see that he is also the only player who hasn't gone even once during these three seasons below 25 goals and assists (and he has the highest score in the whole league).

All of this summed up shows that Salah is probably the most complete offensive player in this comparasion.



Data source:

https://www.kickest.it/en/premier-league/stats
, transfermakt.pl

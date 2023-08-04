# **Movie Data Analysis**

## **Authors**:
Bobby Daly, DS; Michael Romanski, DS

![image](https://github.com/rbdaly16/Movie-Data-Analysis/assets/126971652/c40b4bde-61df-40a6-9fda-fe5230da8888)


## **Overview**
Our project involves the examination of film data sourced from the Internet Movie Database (IMDb), the Numbers database (TN), and The Movie Database (TMDB). By analyzing a film's worldwide gross, budgets, genres, ratings, and directors, we hope to gain insights that will guide decision-making within the film industry. Our aim is to evaluate trends in these specific categories associated with film success. Through this comprehensive analysis, we will be able to make recommendations leading to a successful production.


## **Business Problem**
Now that we've successfully taken over the aviation industry, it's time to expand our company, newly renamed to AirFlix Studios, to the next frontier: film. This will allow our company to grow while also providing our passengers with top of the line entertainment during their flights.

To facilitate this transition, we focused on three ways AirFlix can start out ahead in this industry. First, we want to focus on Worldwide success. We want to utilize the world's boundless market and focus on films that can be enjoyed not just in the States, but abroad as well. Second, we want to create blockbuster films. We want movies that draw wide-ranging audiences with all different tastes and preferences. And finally, we want to build brand recognition. We want the public to associate our name with high-quality films. We want people lining up at the theatre just because they saw our name in the trailer.

In order to accomplish all three of those, our data analysis led to the following recommendations:

Worldwide Success ----> Big Budgets<br>
Blockbuster Films ----> Adventurous, Musical Animations<br>
Brand Recognition ----> High-Quality Directors<br>

Continue below to see how we arrived at these recommendations.

## **Data Understanding**
![image](https://github.com/rbdaly16/Movie-Data-Analysis/assets/126971652/249888ab-976b-46af-a555-8a04a69717a8)
![image](https://github.com/rbdaly16/Movie-Data-Analysis/assets/126971652/fc889856-43a5-4e86-b4c9-b561c877984d)
![image](https://github.com/rbdaly16/Movie-Data-Analysis/assets/126971652/075d0053-d494-468d-8f6b-e204e9609105)

The datasets used in this analysis come from the Internet Movie Database (IMDb), the Numbers database (TN), and The Movie Database (TMDB).

For Budget, we focused on over 2,000 movies from The Numbers and The Movie Database to find correlations between budget and worldwide gross.

For Genre and Director, we used the IMDb data and honed in on those blockbuster films by removing movies with less than 10,000 votes for their rating. The reason for this was that we saw films under this threshold as not having substantial Worldwide Gross numbers.

For Director analysis, we created a director rating by averaging the IMDb's movie ratings for every movie that director worked on. We focused on about 70 experienced Directors that have at least 3 films and a rating of at least 7.0.

## **Data Preparation and Analysis**
To focus on Genre and Director, we consolidated the IMDb data by joining the movie_basics, directors, movie_ratings, and persons tables. To focus on wide-spread blockbuster films, we removed movies with less than 10,000 votes for their rating. We decided on 10,000 votes because further research online found that movies with less than 10,000 votes had very low gross, and we wanted to focus on films with a wider audience.

As for Budget, we updated the relevant columns to be numeric so that we could run aggregates and gather insights.

Our analysis consisted of bar graphs and linear regression models focusing on budget, genre, and director. To see what we found, continue on to our Recommendations!

## Recommendations
**Budget**
For budget, our recommendation is that you have to spend money to make money. As we can see in our linear regression graph, our data suggests that the bigger the budget, the bigger the return. Furthermore the R^2 value suggests that the budget accounts for 63% of variance in worldwide gross. This, along with a p-value smaller than .05 from the anova, shows that we can reject the null hypothesis and say that a film's budget does impact it's worldwide gross.
![Screenshot 2023-08-04 at 3 35 16 PM](https://github.com/rbdaly16/Movie-Data-Analysis/assets/126971652/93dea09e-ab2e-4161-94b5-f6649708e2a7)

**Genre**
For genre, we split movies out into each category they fell into and plotted the average worldwide gross by genre. Based on the graph below, we recommend creating adventurous, musical animations. These three genres had the highest average worldwide gross in our data and can easily pair well together in a film, as Olaf has proved.
![Screenshot 2023-08-04 at 3 36 28 PM](https://github.com/rbdaly16/Movie-Data-Analysis/assets/126971652/ab293549-e729-4f8b-8cc4-950b9d146187)


**Director**
For director, we created a director rating by averaging all of the IMDb movie ratings for each director. From there we joined this data with the worldwide gross data to see which directors acquired the most gross across the globe. Directors have fans, and if you want to start building a brand, why not start with a director who has a large population already on board?

This graph represents the best available Directors who also are Writers for the films they make based on the director rating score we calculated. For Western-Centric audiences, we recommend Christopher Nolan, Damien Chazelle, or Wes Anderson. Nuri Bilge Ceylan did not have any data regarding budget and gross, so we do not feel comfortable selecting him. For the Indian Film market, S.S. Rajamouli would be an excellent selection as Director. Neeraj Pandey and Anurag Kashyap did not have any data regarding budget and gross, so we do not feel comfortable selecting them.

![Screenshot 2023-08-04 at 3 37 46 PM](https://github.com/rbdaly16/Movie-Data-Analysis/assets/126971652/b0a0eae9-560f-46d1-81a0-e3e3ec4ba467)
![Screenshot 2023-08-04 at 3 37 21 PM](https://github.com/rbdaly16/Movie-Data-Analysis/assets/126971652/d49a1900-1d35-4433-a647-a6c014c154ad)


## **Next Steps**
Based on the project findings, there are several potential next steps to further enhance the analysis of film success. These steps include:

Genre Investigation: To enhance marketability, we would like to further investigate why these three genres (adventure, musical, and animation) are so successful. We hypothesize it may be because they are so accessible to all age ranges, but with more data we would be able to get a clearer picture. If we're able to glean more information as to the why, we would be able to better customize our ads for the demographics we have and the demographics we don't yet have but could be an opportunity.

Release Date Investigation: Our analysis with this data found no correlation between a film's release date and its worldwide gross. However, we would like to dive deeper into this and see if certain genres have a correlation with worldwide gross based on their release date. If so, strategically timing movie premieres could make blockbuster films even more successful.

Worldwide Gross vs. Director Rating Investigation: While our statistical analysis of director rating and worldwide gross produced a low R^2 value, we think it would be beneficial to further investigate this correlation. Knowing how a director rating influences worldwide gross could help guide hiring decisions in the future.

By pursuing these next steps, the analysis of film success could be strengthened, enabling more informed decision-making for AirFlix Studios in the film industry.

## Thank You!
Thank you for taking the time to review our recommendations.
We hope this information helps and we look forward to working with you more on the next steps.

Sincerely, <br>
Bobby Daly, Michael Romanski <br>
Airflix Studios

## Further Details
Further details are available in the full analysis presented in the [Jupyter Notebook](https://github.com/rbdaly16/Movie-Data-Analysis/blob/bobby/Movie%20Data%20Analysis.ipynb). 

## Repository Structure
```
├── data
├── Scratch_notebook_folder
├── images
├── README.md
├── .gitignore
├── .DS_Store
├── Movie Data Analysis Presentation.pdf
└── Movie Data Analysis final.ipynb
```

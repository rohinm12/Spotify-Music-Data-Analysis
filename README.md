# Spotify-Music-Data-Analysis - Report

Introduction -->

With the growing demand for streaming music platforms like Amazon music, iTunes, YouTube etc., Spotify has emerged as one of the largest digital service to contribute in music industry. It has over 286 million monthly active users worldwide. So, what makes streaming music popular?  Do music genres influence the popularity of a track? Are audio features of music responsible for affecting the general trend of music? Analyzing some of those questions could lay a dynamic impact on informed decision making for music business. One of the most eminent ways where Spotify uses data science is by utilizing data from customer interaction to reinforce their music content according to the specific tastes of the user. Their most significant goal is to streamline the music listening experience and encourage the user to discover new music and engage them in streaming every day. This can be achieved using several data mining techniques and approaches. Exploratory Data Analysis and building predictive models with machine learning algorithms are some of those!

The project is about performing Exploratory Data Analysis on a Spotify music dataset which comprises of songs streamed from year 2010 through 2019. As Spotify offers one of the largest music streaming service to the users on a global scale, it is evident that understanding different styles of music is an essential step for deriving insights. For the project, we have explored the data to the extent where we could figure out the key elements that influence track popularity.

How it helps music artists and distributors -->

This data exploration is primarily performed to extend support to the music distributors who are operating on digital streaming platforms. Identifying the trend of music would help the distributors to make their music contributions more efficient. Our Project aims to discover insightful patterns with the use of descriptive statistics and visual representations and conduct an in-depth analysis of Spotify Data  which would eventually help music artists to recognize their customers.

Why Data Analysis is Needed? -->
Performing Data Analysis here is essential to produce the best results for well informed and efficient decisions and identify general trend of music with respect to Spotify music listeners. Data Analysis on Spotify Data extracts key metrics and characteristics of a song which can be represented in form of graphical representations.

How music data analysis will improve the decision making? -->
Analyzing music data will improve decision making because we are exploiting the distinct audio features of a track such as energy, speechiness, valence, duration, tempo, key etc. which are essential in classifying songs based on track popularity. Our Analysis focuses on identifying key influencers that affect the popularity of the track.

Data Source --> 
We have obtained our data from one of the github’s repository i.e. Tidytuesday which was already scraped using Spotify’s API. We have selected data from this source because it had all the characteristics of a track necessary for music analysis.

Primary Data Variables -->
Important Variables in our analysis include: Track_artists, track_popularity, release year, Song_genre, danceability, energy, valence, key, mode, tempo and duration.

Variables ---->
track_name	     -->  Song Name.
track_artist     --> 	Song Artist.
track_popularity -->  Song Popularity (0-100) where higher is better.
track_album_name -->  Song album name.
release_year     -->  Year when album released.
song_genre       -->  Song genre.
danceability     -->  Danceability   how suitable a track is for dancing.
energy           -->  Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy. 
key		           -->  The estimated overall key of the track. Integers map to pitches using standard Pitch Class notation.
                      E.g. 0 = C, 1 = C♯/D♭, 2 = D, and so on. 
loudness         -->	The overall loudness of a track in decibels (dB). 
mode		         -->  Mode indicates the modality (major or minor) of a track. Major is represented by 1 and minor is 0.
speechiness      -->  Speechiness detects the presence of spoken words in a track. Values above 0.66 describe tracks that are probably made entirely of spoken words. 
acousticness     -->  A confidence measure from 0.0 to 1.0 of whether the track is acoustic.
instrumentalness -->	Predicts whether a track contains no vocals. 
liveness         -->  Detects the presence of an audience in the recording. 
valence          -->	A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. 
tempo		         -->  In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration.
duration_ms	     -->	Duration of song in milliseconds.

Data Cleaning Process -->
We cleaned the data with the help of R programming and Microsoft Excel. Removing missing values and unwanted columns pulled out inconsistencies and major errors from the dataset. We also removed duplicate observations to avoid ambiguity. Further, we detected outliers in some of the numerical features of track and removed them to improve statistical analysis.

Descriptive Statistics -->
The average popularity for Spotify tracks release from year 2015- 2019 is 41.78. The range for the track popularity can be observed from 0 to 98. The histogram for track popularity is normally distributed and can be observed as symmetric. In last the decade, following number of songs were released for the respective genres. 

Pop: 3408      Latin: 2386      Edm: 2965                             
Rap: 3001      R&b: 1699        Rock: 849

Exploratory Data Analysis -->
Question 1:
Which artist has most number of songs in top 100 popular tracks over the last decade?

![image](https://user-images.githubusercontent.com/57821332/115646913-fe771580-a2f0-11eb-83b4-12d757ac226f.png)

Answer: 
Post Malone has the highest number of hits over last decade.

Question 2:
Which music genre has become most popular and least popular over the last decade?

![image](https://user-images.githubusercontent.com/57821332/115647005-1fd80180-a2f1-11eb-8f51-30b11fd309d7.png)

Answer:
Rap Music has had the highest increase in average popularity over the years while pop music has had a substantial fall.

Question 3:
For top popular songs in the last decade, does duration play a significant role?

![image](https://user-images.githubusercontent.com/57821332/115647048-2c5c5a00-a2f1-11eb-93d1-82c41f057c18.png)

Answer:
Yes, the duration of the song impacts its track popularity. As the duration of a track decreases, its popularity has increased over the years. So, it shows that users prefer    listening to tracks with less run-time.

Question 4:
For the top 50 popular artists in the previous decade, is there a preference for the keys used for composition? And is there a relationship between these preferred keys and valence (positivity) for popular tracks?

![image](https://user-images.githubusercontent.com/57821332/115647141-4dbd4600-a2f1-11eb-9d7f-79a08b6c4a21.png)

Answer:
It's evident that most of the popular tracks are based on the scale of G. And yes, there is a relationship between keys and valence levels for popular songs. So higher valence keys resemble positive Emotion or mood.

Question 5:
Analyzing songs by top six popular artists (based on average popularity and a minimum of 20 tracks) for the last three years.

![image](https://user-images.githubusercontent.com/57821332/115647189-5f9ee900-a2f1-11eb-869a-3a69737932f8.png)

Answer:
For the top six artists we have faceted the plot which shows the type of songs composed by them. We made a simple classification to represent the emotions as happy (when both valence and energy levels are high), sad (both valence and energy levels are low), agitated (low valence levels and high energy levels) and for calm (high valence levels and low energy levels) 
Example:  Among top six Artists we can see tracks composed by ed Sheeran fall into happy songs category with high energy and valence levels.

Results ----->
Findings -->
Our findings signify that track popularity is influenced by some of the quantitative features of a song. These explanatory variables interact with the popularity of a track in distinct ways. Duration is one the key determinants to affect track popularity. It clearly indicates that users prefer to listen songs with less run-time. Moreover energy, key, mode and valence are crucial factors in determining emotions and positiveness of a track. Further, our analysis also exhibited the trend of music genres over the years and its impact on track popularity.

Proposed Prediction Method -->
For the predictive modelling process, we want to classify tracks based on their popularity with the help of music audio features. We will use classification algorithms like K- nearest neighbor, decision trees and random forest to classify track popularity. This will allow music artists and analysts to understand customer preferences and discover music trends among Spotify users.

Conclusion -->
We have performed data exploration with the help of graphical representations in R programming and summarized the key characteristics involved in analyzing popularity of music streaming on Spotify. Our proposed prediction model will allow Spotify to make better informed decisions by relating the type of music which user usually gravitates towards and optimize their music listening experience.











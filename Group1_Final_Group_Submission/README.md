# Analysis of Lyrics during the Covid-19 Pandemic


## 1.Introduction and Background

Many people have done some research on the impact of COVID-19 on the economy, education and medication, but we are more interested in culture, especially music. The epidemic has affected everyone in the world in one way or another and we were curious to see if this situation had an impact on the artists who write the songs. We decided to use the lyrics of popular songs as a study to see if there were any changes in the lyrics of songs before and after the epidemic, especially before and after 2020 when COVID-19 widely spread in most countries around the world.


## 2.Research Question

Does COVID-19 have any effect on lyrics? If it does, it is good or bad?

## 3.Dataset
We've selected three music year charts from the the UK, the US and Taiwan：Officialchart、Billboard、KKBOX.
(1) Hot 50 songs in 2018, including titles, artists, lyrics;
(2) Hot 50 songs in 2019, including titles, artists, lyrics;
(3) Hot 50 songs in 2020, including titles, artists, lyrics;
(4) Hot 50 songs in 2021, including titles, artists, lyrics;
(5) Hot 50 songs in 2022, including titles, artists, lyrics.


## 4.Tutorials
### (1)Collecting Data 

We used Genius API and LyricsGenius to collect the titles, artists and lyrics of the hot 50 songs from 2018 to 2022 in Billboard, Officialchart. When we scraped the Chinese website we found this website is dynamic, so we imported a Chrome webdriver to scrape the titles and artists.
Then we found that we couldn't find all the Chinese lyrics through the Genius API, so we found a KKBOX API through which we could find the lyrics of the songs.
For copyright reasons,  with the KKBOX API we can only find links to lyrics by searching for the artist and song title first, so we defined a few functions to find the lyrics URL by artist and song title. Then we used request and Beautifulsoap functions to grab the lyrics from these urls.

### (2)Analysing Data 

We used vaderSentiment to analyse the sentiment scores of the lyrics to see whether there was a positive or negative impact of the epidemic on the sentiment of the songs. We also used WordCloud and TfidfVectorizer to analyse the frequency of words in the lyrics.

### (3)Active Learning Exercises 

In this part we show how to translate texts in different languages.
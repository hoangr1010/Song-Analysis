# Song-Analysis
## Project summary 
- This project aims to collect data from Spotify, LastFM about all Taylor Swift songs to analyze the correlation between her music style and her tracks popularity. 
- Project follows the following steps: 
  - Step 1: Collect data 
  - Step 2: Process and clean data
  - Step 3: Analyzing data by visualization to answer questions: 
    - What are types of genres that is most popular at the moment?
    - How Taylor Swift song style change through the time? How it change with popularity?

## Step 1: Collect data

In this project, I will collect these kinds of data: 
- song_id
- album_id
- song_name
- album_name
- release_date (of each song/album)
- song_features
- popularity (of each song)
- Song genres

### Data Collecting Method
- Most of data is provided through Spotify API, but song genres is not provided in Spotify API.
#### Song genres:
- Problem: Song genres is not provided by any data sources currently
- Solution: In order get song genres of each tracks, I will use LastFM API to get song tags including mixed information of data, then I will filter song tags into song-genres-related tags only. <img width="1006" alt="Screenshot 2022-12-24 at 11 13 22 AM" src="https://user-images.githubusercontent.com/117782458/209447213-e751da7d-68a4-4a73-9130-6816aa9b2bfa.png">

## Step 2: Process and clean data
- Problem: There are many Taylor's albums reposted leading to a lot of duplicated albums and tracks. Based on analysis purpose, we need to get only those original tracks.
## Data Cleaning Method
### album_name:
- Problem: There are mayny albums reposted, we need to drop all duplicate albums and tracks
- Solution: In order to drop duplicated albums and tracks, I will only delete duplicate albums leading all duplicated tracks will be deleted after that. In order delete duplicate albums, I delete all albums have special words like: Version, Karaoke, Acoustic,...

## Data Processing Method
### popularity
- Problem: Since there are many duplicated tracks, audiences might not listen to original tracks -> make the popularity of original tracks is not accurate
- Solution: Within all duplicate of one track, I will get the highest popularity metric to present that track popularity.

## Step 3: Analyzing data by visualization to answer questions
### First question: What are types of genres that is most popular at the moment?
In this questions, I will get top 10 popularity tracks and create a bar chart of song genres in these tracks
<img width="695" alt="Screenshot 2022-12-24 at 11 23 03 AM" src="https://user-images.githubusercontent.com/117782458/209447460-03ee9282-3baf-477b-8885-65c7f30c0427.png">
- Main insight: pop is still and always the main genres in Taylor's music, so it's currently her fans' most favorite genres in her music, including synthpop, dreampop and darkpop.

### Second question: How Taylor Swift song style change through the time? How it change with popularity?
In this question, I use 3 chart to reveal about the his songs' trend on popularity, feature and genres through each albums in time order:
- Ridgeline chart: to present features distribution
- Violinplot: to present popularity distribution
- Genres: to present what main genres in each album. This data is not totally accurate and sufficient, but it's still good present a main genres on each Taylor's song and album.
- Notice: All 3 chart have the same y axis and order of y axis: album ~ release date of that album
<img width="777" alt="Screenshot 2022-12-24 at 11 26 20 AM" src="https://user-images.githubusercontent.com/117782458/209447527-08dba598-fab3-43dc-a026-d2078983d9f4.png">
<img width="1440" alt="Screenshot 2022-12-24 at 11 26 38 AM" src="https://user-images.githubusercontent.com/117782458/209447532-36586f1b-359d-4db2-9720-ca8f886f19df.png">

#### Main insights: 
- As observations, there's no clear relations between 3 charts, but there're some noticeable insights from these charts.
  - Popularity: Generally, Taylor's songs are mostly remaining relatively good popularity between 60 to 80 popularity, excluding the lattest albums with 80 to 100 popularity.
  - Song Genres: she changes her song genres continously throughout a decade.
  - Song feature: her song features on accousticness, valence and energy chiefly remain the same through the time.
#### Conclusion:
- Key takeaway: These insights show that her music style have special attraction that appeals tons of audiences who still listens her old songs that released up to 10 years ago.
- Taylor's main music style: she mainly use little acoustic instruments, her music tone (valence) is neutral (not sad but not happy tone, and her music have a wide range of energy, from 0.4 to 0.8; However, she tend to reduce her energy slightly after each album.





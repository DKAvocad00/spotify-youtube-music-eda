# Spotify YouTube Music EDA

## Overview
This repository contains an exploratory data analysis (EDA) of a dataset that combines information from Spotify and YouTube Music. 
The dataset includes details about various songs, such as their attributes, popularity on Spotify (streams), and popularity 
on YouTube (views, likes, comments).

## Dataset Structure
The dataset comprises 26 features, each providing valuable insights into the songs. Here are some key features:

- **Track:** Name of the song on Spotify.
- **Artist:** Name of the artist.
- **Url_spotify:** URL of the artist on Spotify.
- **Album:** Album in which the song is contained on Spotify.
- **Album_type:** Indicates if the song is released on Spotify as a single or part of an album.
- **Danceability:** Describes how suitable a track is for dancing.
- **Energy:** Represents a perceptual measure of intensity and activity.
- **Key:** The key the track is in.
- **Loudness:** The overall loudness of a track in decibels (dB).
- **Speechiness:** Detects the presence of spoken words in a track.
- ...
- **Licensed:** Indicates whether the video represents licensed content.
- **Official_video:** Boolean value indicating if the video found is the official video of the song.

## Analysis and Code
The repository includes a Jupyter notebook (`spotify_youtube_eda.ipynb`) with Python code that performs various analyses on the dataset. 
Some notable analyses include finding the most streamed song, identifying the artist with the most views on YouTube, calculating the average 
duration of all songs, determining the most commonly used key, and more.

### Example Analyses:

1. **Most Streamed Song:**
   - Function: `max_id(data,column_name)`
   - Output: The most streamed song on Spotify is "Blinding Lights" by The Weeknd, with 3,386,520,288 streams.

```python
output_by_id(max_id(df,'Stream'),'Stream')
```
2. **Artist with the Most YouTube Views:**
   - Function: `max_sum(data,group_column,sum_column)`
   - Output:  Ed Sheeran has the highest number of views on YouTube, with 15,460,207,769.

```python
output_max(max_sum(df,'Artist','Views'),'Views')
```
3. **Average Duration of All Songs:**
   - Function: `mean_duration(data)`
   - Output: The mean duration of all songs is approximately 3.75 minutes.

```python
print("Mean duration of all songs in minutes is {}".format(mean_duration(df)))
```

## Questions Explored
The notebook addresses several questions, including:

- Finding the most danceable song.
- Identifying the song with the highest energy score.
- Determining the most positive (high valence) song.
- Exploring the relationship between valence and popularity on Spotify and YouTube.
- Analyzing the correlation between energy and loudness.
- Investigating the popularity of songs released as singles versus albums.

## Conclusion
The exploratory data analysis provides valuable insights into the characteristics and popularity of songs on both 
Spotify and YouTube Music. Users can explore the notebook to gain a deeper understanding of the dataset and the 
relationships between different features.

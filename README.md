# Spotify 2023 Data Analysis

## Overview

This repository contains a Jupyter Notebook that performs an exploratory data analysis (EDA) on a Spotify dataset from 2023. The analysis aims to uncover trends and relationships between various song features and their popularity (measured by streams).

## Dataset

The dataset used in this analysis is stored in the file `spotify-2023.csv` and it is taken from Kaggle. It contains information about songs, including:

- **track_name:** Name of the track.
- **artist(s)_name:** Name of the artist(s).
- **artist_count:** Number of artists contributing to the track.
- **released_year:** Year of release.
- **released_month:** Month of release.
- **released_day:** Day of release.
- **in_spotify_playlists:** Number of Spotify playlists the track is included in.
- **in_spotify_charts:** Position of the track on Spotify charts.
- **streams:** Number of streams on Spotify.
- **in_apple_playlists:** Number of Apple Music playlists the track is included in.
- **in_apple_charts:** Position of the track on Apple Music charts.
- **in_deezer_playlists:** Number of Deezer playlists the track is included in.
- **in_deezer_charts:** Position of the track on Deezer charts.
- **in_shazam_charts:** Position of the track on Shazam charts.
- **bpm:** Beats per minute.
- **key:** Key of the song.
- **mode:** Mode of the song (Major or Minor).
- **danceability_%:** Danceability score.
- **valence_%:** Valence score (positivity).
- **energy_%:** Energy score.
- **acousticness_%:** Acousticness score.
- **instrumentalness_%:** Instrumentalness score.
- **liveness_%:** Liveness score.
- **speechiness_%:** Speechiness score.

## Analysis Steps

The Jupyter Notebook performs the following analysis steps:


1. **Data Exploration and Visualization:**
   - Calculates descriptive statistics (mean, standard deviation, quartiles, etc.) for numerical features.
   - Creates various visualizations to explore the data, including:
     - Scatter plots to examine relationships between variables (e.g., bpm vs. danceability).
     - Bar plots to visualize categorical data (e.g., distribution of song modes).
     - Histograms to understand the distribution of numerical features.

2. **Feature Engineering:**
   - Creates a new column 'track_id' to assign unique IDs to each track.
   - Applies one-hot encoding to categorical features ('key' and 'mode') to convert them into numerical format.
   - Renames columns for better readability.
   - Scales numerical features using Min-Max scaling to a range between 0 and 1.

3. **Correlation Analysis:**
   - Calculates the correlation matrix between selected features and the target variable ('streams').
   - Visualizes the correlation matrix using a heatmap.


## Findings

The analysis reveals some interesting insights:

- There is a weak negative correlation between 'bpm' and 'danceability'.
- The majority of songs in the dataset are in Major mode.
- Majority of top songs by streams have the key C# which looks likely to be the key to making a song that is in the top 100 streams.

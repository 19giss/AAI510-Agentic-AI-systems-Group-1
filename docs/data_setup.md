# Data Setup

The VibeML data pipeline uses two Kaggle datasets for the MVP:

1. Spotify Tracks Dataset  
   Used as the main recommendation dataset because it contains audio features such as danceability, energy, valence, tempo, acousticness, instrumentalness, and speechiness.

2. Spotify Global Music Dataset (2009–2025)  
   Used as supporting data for artist popularity, followers, genres, release dates, and album metadata.

## Required Databricks Tables

The `data/raw` and `data/processed` folders are included for project organization. Full datasets are not committed to GitHub because the working data is stored in Databricks Catalog. 

The `01_data_pipeline` notebook expects the following raw tables to exist in Databricks Catalog:

Raw Databricks tables:
- `main.default.spotify_tracks_raw`
- `main.default.spotify_data_clean_raw`
- `main.default.track_data_final_raw`

Processed Databricks table:
- `main.default.vibeml_tracks_processed`

## MVP Data Decision

For the MVP, VibeML uses the Kaggle datasets as the main data foundation. Live Spotify API access is a stretch goals for now.
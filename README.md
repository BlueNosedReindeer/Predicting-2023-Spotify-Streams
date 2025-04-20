# Predicting 2023 Spotify Streams with Supervised Learning

Welcome to the project repository for **Predicting Spotify Streams (2023)** — a supervised machine learning analysis using real-world music data from the most streamed Spotify songs of the year.

This project aims to explore which song attributes and platform features (like playlist/chart placements) can best predict a track's total number of Spotify streams.

---

## Dataset

**Source**: [Kaggle – Most Streamed Spotify Songs 2023](https://www.kaggle.com/datasets/nelgiriyewithana/top-spotify-songs-2023)

Each row represents a song and includes:
- Track/artist metadata (e.g. title, release date)
- Platform data (e.g. playlist/chart placements across Spotify, Apple Music, Deezer, Shazam)
- Audio features (e.g. BPM, danceability, energy, valence)
- Target variable: **Total Spotify Streams**

---

## Modeling Summary

We tested multiple regression approaches to predict stream counts:

| Model                               | RMSE           | MAE            | R²     |
|------------------------------------|----------------|----------------|--------|
| **Tuned Random Forest**            | 264M           | 171M           | 0.7437 |
| Untuned Random Forest              | 266M           | 173M           | 0.7402 |
| Linear Regression (Combined Score) | 358M           | 240M           | 0.5278 |

Tree-based models performed best, with the **tuned Random Forest** explaining ~74% of the variance in stream counts.

---

## Key Insights

- Playlist/chart placement features like `in_spotify_playlists` and `in_apple_playlists` are **strongly predictive** of streaming success.
- Combining features into a single exposure score led to **worse performance** than using them separately.
- Linear regression **underperformed** due to the non-linear nature of the data.
- Random Forest captured complex interactions without requiring feature scaling or transformations.

---

## Video Presentation

[Link to Presentation Video]()  
_(To be added once your video is uploaded — YouTube or shared file link)_

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/BlueNosedReindeer/Predicting-2023-Spotify-Streams.git
   cd Predicting-2023-Spotify-Streams

2. Open Jupyter and begin to run all of the cells.

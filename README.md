# Spotify Audio Feature Analyzer
**Mood, Rhythm, and Texture Analysis Using Unsupervised Learning**

---

## Overview

This project explores the latent structure of music using unsupervised learning techniques applied to Spotify audio features. By analyzing musical attributes such as valence, energy, tempo, and acousticness, the system identifies meaningful patterns related to emotional mood, rhythmic structure, sonic texture, and musical outliers.

Rather than relying on genre labels, this project utilizes clustering algorithms to uncover natural groupings directly from audio characteristics. This approach enables deeper insights into music recommendation, playlist generation, and musical structure analysis.

---

## Objectives

This project investigates the following core questions:

*   Can songs be grouped into emotional mood clusters using audio features alone?
*   Do rhythm features form distinct groove patterns and reveal outliers?
*   Can sonic texture distinguish acoustic versus electronic production styles?
*   How do different clustering algorithms compare in capturing musical structure?
*   Do certain musical moods correlate with higher popularity?

---

## Dataset

The dataset consists of Spotify tracks with audio features extracted directly from the Spotify API. 

### Key Features Analyzed

| Category | Features |
| :--- | :--- |
| **Emotional** | Valence (positivity), Energy (intensity), Danceability (rhythmic suitability) |
| **Rhythm** | Tempo (BPM), Energy, Danceability |
| **Texture** | Acousticness, Instrumentalness, Loudness |
| **Metadata** | Popularity score, Track duration, Genre *(used exclusively for interpretation, not clustering)* |

---

## Methodology

Multiple clustering approaches were applied to capture different facets of musical structure:

### 1. Hierarchical Clustering
*   **Purpose:** Identifying emotional mood clusters.
*   **Key Findings:** Grouped tracks into four primary states: Calm/Positive, Sad/Low Energy, Happy/Energetic, and Angry/High Energy.

### 2. Gaussian Mixture Models (GMM)
*   **Purpose:** Probabilistic clustering to identify hybrid emotional tracks.
*   **Key Findings:** Enabled soft cluster assignments, successfully capturing overlapping and complex emotional states.

### 3. DBSCAN (Density-Based Clustering)
*   **Purpose:** Rhythm analysis and outlier detection.
*   **Key Findings:** Identified dense groove regions and flagged experimental, unconventional tracks as outliers.

### 4. K-Means Clustering
*   **Purpose:** Sonic texture analysis.
*   **Key Findings:** Categorized tracks into distinct texture environments, including Electronic/Processed, Acoustic/Organic, Hybrid Vocal-Oriented, and Hybrid Instrumental/Ambient.

### 5. Spectral Clustering
*   **Purpose:** Capturing non-linear emotional structures.
*   **Key Findings:** Revealed curved emotional boundaries and continuous emotional transitions between tracks.

### 6. HDBSCAN Outlier Detection
*   **Purpose:** Identifying rare and extreme musical structures.
*   **Key Findings:** Detected strict outliers, including highly experimental tracks, spoken-word content, instrumental extremes, and non-mainstream music.

---

## Project Structure

```text
spotify-clustering/
│
├── data/
│   └── spotify_tracks.csv
│
├── clustering/
│   ├── dbscan.py
│   ├── gmm.py
│   ├── hierarchical.py
│   ├── kmeans.py
│   └── spectral.py
│
├── main.py
├── outlier_detection.py
├── preprocessing.py
├── visualization.py
└── README.md

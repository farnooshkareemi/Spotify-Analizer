# Spotify-Analizer
Spotify Audio Feature Clustering

Mood, Rhythm, and Texture Analysis Using Unsupervised Learning

Overview

This project explores the latent structure of music using unsupervised learning techniques applied to Spotify audio features. By analyzing musical attributes such as valence, energy, tempo, and acousticness, the system identifies meaningful patterns related to emotional mood, rhythmic structure, sonic texture, and musical outliers.

Rather than relying on genre labels, this project uses clustering algorithms to uncover natural groupings directly from audio characteristics, enabling deeper insight into music recommendation, playlist generation, and musical structure analysis.

Objectives

This project investigates the following questions:

Can songs be grouped into emotional mood clusters using audio features alone?

Do rhythm features form distinct groove patterns and reveal outliers?

Can sonic texture distinguish acoustic vs electronic production styles?

How do different clustering algorithms compare in capturing musical structure?

Do certain musical moods correlate with higher popularity?

Dataset

The dataset consists of Spotify tracks with audio features extracted from the Spotify API.

Key Features Used

Emotional features:

Valence (positivity)

Energy (intensity)

Danceability (rhythmic suitability)

Rhythm features:

Tempo (BPM)

Energy

Danceability

Texture features:

Acousticness

Instrumentalness

Loudness

Additional metadata:

Popularity score

Track duration

Genre (used only for interpretation, not clustering)

Methods Used

Multiple clustering approaches were applied to capture different aspects of musical structure:

1. Hierarchical Clustering

Used to identify emotional mood clusters.

Findings:

Calm / Positive

Sad / Low Energy

Happy / Energetic

Angry / High Energy

2. Gaussian Mixture Models (GMM)

Provides probabilistic clustering and identifies hybrid emotional tracks.

Advantages:

Soft cluster assignments

Captures overlapping emotional states

3. DBSCAN (Density-Based Clustering)

Used for rhythm analysis and outlier detection.

Findings:

Dense groove regions identified

Experimental and unconventional tracks detected as outliers

4. K-Means Clustering

Used for sonic texture analysis.

Identified texture environments:

Electronic / Processed

Acoustic / Organic

Hybrid Vocal-Oriented

Hybrid Instrumental / Ambient

5. Spectral Clustering

Captures non-linear emotional structure.

Reveals:

Curved emotional boundaries

Continuous emotional transitions

6. HDBSCAN Outlier Detection

Identifies rare and extreme musical structures.

Outliers include:

Experimental tracks

Spoken-word content

Instrumental extremes

Non-mainstream music
spotify-clustering/
│
├── data/
│   └── spotify_tracks.csv
│
├── preprocessing.py
├── clustering/
│   ├── hierarchical.py
│   ├── gmm.py
│   ├── dbscan.py
│   ├── kmeans.py
│   └── spectral.py
│
├── visualization.py
├── outlier_detection.py
├── main.py
│
└── README.md

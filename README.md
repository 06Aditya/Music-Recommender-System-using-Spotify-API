# Spotify Recommendation System

A music recommendation system that suggests songs based on a given playlist or track using content-based filtering and Spotify audio features.

---

## Demo

Live Demo :
https://user-images.githubusercontent.com/107134115/201241072-06681109-72ad-4416-b5f0-35322646dc1e.mp4

---

## Overview

This project builds a recommendation system that helps users discover music similar to their existing preferences. It leverages playlist data, Spotify audio features, and metadata to generate personalized recommendations.

The system uses content-based filtering techniques and similarity measures to recommend songs aligned with user taste.

---

## Dataset

The project uses the **Million Playlist Dataset (MPD)**.

* https://www.aicrowd.com/challenges/spotify-million-playlist-dataset-challenge

### Dataset Details

* 1 million playlists
* Metadata includes:

  * Playlist name
  * Track list
  * Number of artists
  * Duration and other attributes

---

## Approach

### Data Collection

* Extracted playlist data from MPD
* Used Spotify API to fetch additional features:

  * Audio features
  * Track popularity
  * Artist popularity
  * Genres

---

### Data Preprocessing

* Merged multiple datasets into a single dataframe
* Handled missing values and duplicates
* Bucketed features such as:

  * Track release year
  * Popularity scores

---

### Feature Engineering

* Applied **TF-IDF vectorization** on artist genres
* Combined metadata and audio features
* Converted playlists into vector representations

![TF-IDF](https://user-images.githubusercontent.com/107134115/201203710-c1a48e8b-1365-4cc3-bba4-58a1102bafde.png)

---

### Modeling

* Used **cosine similarity** to compare playlist vectors with songs

![Cosine Similarity](https://user-images.githubusercontent.com/107134115/201203569-6bcd14fd-6704-4ad7-9577-44095bd65f74.png)

#### Models Implemented

* **Model 1:** Higher weight to genres
* **Model 2:** Equal weight to all features
* **Spotify API Model:** Baseline comparison

---

## Deployment

The application is deployed using **Streamlit** on Hugging Face Spaces.

### Run Locally

```bash
cd Streamlit
streamlit run main.py
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Project Structure

```id="k2z8rp"
Spotify-Recommendation-System/
│── notebooks/
│── data/
│── Streamlit/
│── README.md
```

---

## Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* Spotipy (Spotify API)
* Streamlit

---

## Future Improvements

* Improve recommendation diversity
* Incorporate collaborative filtering
* Optimize performance for large datasets
* Enhance UI/UX of the application

---

## Contact

* LinkedIn: https://www.linkedin.com/in/aditxya/

---

If you found this project useful, consider giving it a ⭐

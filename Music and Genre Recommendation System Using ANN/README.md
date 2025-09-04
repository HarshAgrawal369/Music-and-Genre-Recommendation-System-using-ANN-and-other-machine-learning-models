Emotion-Based Music Recommender System
Abstract

Conventional music recommendation systems typically rely on historical user data such as listening history, time of access, or frequently played genres.

This project introduces a mood-aware music recommendation approach. By analyzing a user’s image to detect their emotional state, the system generates personalized music recommendations aligned with their current mood.

Description

1. Emotion Detection

User images are captured and processed using OpenCV.

A CNN + DNN hybrid model predicts the user’s mood (Happy or Sad).

2. Music Clustering and Recommendation

Songs are grouped into two categories — Very Entertaining (Class 0) and Relaxing (Class 1) — using the K-Means clustering algorithm.

Recommendations are ranked by the current popularity of tracks within each cluster.

3. Differentiating Feature

Unlike traditional systems that recommend sad tracks when a user feels low, this system recommends uplifting songs when the mood is Sad and relaxing songs when the mood is Happy.

The training code is available in the Emotion_detector_version2 notebook. The trained model (final_model.h5) can be modified or retrained as required.

Dataset

Source: Spotify Dataset (1921–2020, 160k tracks)

Features include acousticness, energy, loudness, and danceability, enabling effective clustering and recommendations.

Technologies and Libraries Used

Computer Vision: OpenCV

Deep Learning: TensorFlow, Keras

Machine Learning: Scikit-learn, LightGBM

APIs: Spotipy (Spotify API)

GUI Development: Tkinter, Pillow

How to Use

Run run.py to start the application.

Enter an artist’s name in the GUI.

The system retrieves albums via the Spotify API and activates the webcam.

Press ‘q’ to stop capturing the image.

The GUI generates recommendations based on the detected mood.

Click Print to display the recommended tracks.
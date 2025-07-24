# Spotify Music Recommender System
This repository contains a Google Colab notebook for building a comprehensive Spotify Music Recommender System. The project leverages various machine learning techniques to provide song recommendations based on their audio features. It uses the spotipy library to interact with the Spotify API and a Kaggle dataset for a rich source of track data.

# 🚀 Features
This recommender system implements four distinct models:

Content-Based Filtering: Recommends songs that are most similar to a chosen track based on the cosine similarity of their audio features (e.g., danceability, energy, valence). This model is memory-optimized to handle large datasets efficiently.

Clustering-Based Recommender (K-Means): Groups songs into a predefined number of clusters using the K-Means algorithm. When you select a song, it recommends other tracks from the same cluster.

Dimensionality Reduction-Based Recommender (PCA): Uses Principal Component Analysis (PCA) to reduce the feature space into two dimensions and then recommends songs that are closest to the selected track in this reduced space (nearest neighbors).

Hybrid Recommender: A more advanced model that first gathers a large pool of similar songs using content-based filtering and then re-ranks them based on their popularity score on Spotify. This provides recommendations that are both similar in sound and popular among listeners.

# 🛠️ Tech Stack
Programming Language: Python

Environment: Google Colab / Jupyter Notebook

Core Libraries:

pandas & numpy for data manipulation

scikit-learn for machine learning (StandardScaler, KMeans, PCA, Cosine Similarity)

spotipy for interacting with the Spotify Web API

Visualization:

matplotlib & seaborn for static plots (histograms, heatmaps)

plotly for interactive radar charts

TSNE for high-dimensional cluster visualization

# 📋 Setup and Usage
To get this project running, follow these steps:

Clone the Repository:
```bash
git clone https://github.com/your-username/spotify-recommender-system.git
cd spotify-recommender-system
```

Open in Google Colab: Upload the Spotify_Music_Recommender_System.ipynb notebook to your Google Colab account.

Get Spotify API Credentials:

Go to the Spotify Developer Dashboard. https://developer.spotify.com

Log in and create a new application to get your Client ID and Client Secret.

Download the Dataset: 

Download the "Spotify Tracks DB" from this Kaggle page. https://www.kaggle.com/datasets/yamaerenay/spotify-dataset-19212020-600k-tracks or from the code

You will need the tracks.csv file.

Run the Notebook:

Open the notebook in Colab.

enter your Client ID and Client Secret into the respective fields.

upload the tracks.csv file to your Colab session's file storage.

Run the cells sequentially from top to bottom.

Get Recommendations:

Navigate to the final section (Section 6).

Change the input_track_name variable to any song title you want recommendations for.

Run the cell to see the output from all four recommender models.

# 📊 Evaluation and Visualization
The notebook includes several methods to evaluate the models and visualize the data:

Elbow Method: Used to determine the optimal number of clusters (K) for the K-Means algorithm.

t-SNE Cluster Plot: Visualizes the song clusters in a 2D space, showing how well the K-Means algorithm has separated the tracks.

Clustering Metrics: The Silhouette Score and Davies-Bouldin Index are calculated to quantitatively evaluate the performance of the clustering model.

Radar Charts: Interactive plots that compare the audio feature profiles of an original song and a recommended song, providing a clear visual understanding of their similarity.

Feature Correlation Heatmap: Shows the relationships between different audio features in the dataset.

CREDITS to https://www.kaggle.com/code/akershishukla/music-recommendation-system/notebook, Made the first Music recommendation system using KMeans Music_Recommendation_System.ipynb

# COMP 6321 Machine Learning Project - Group 18
Recommender system for spotify 1M playlist dataset using k-NN and NeuMF models

## Dependencies
* Pytorch
* Pandas
* Scipy
* Numpy
* tqdm


## Folder Structure
```
./code/environment.yaml <-- conda environment for our project
./code/preprocessing.ipynb <-- notebook to preprocess our data
./code/recommender_models.ipynb <-- primary notebook to run the k-NN and NeuMF models
./code/raw_data/ <-- subset of spotify's original 5gb dataset
./code/dataframes/ <-- preprocessed dataframes containing playlists, tracks, genres
./code/model/ <-- trained neuMF model will save to this folder when run
```

## Instructions
* create conda environment from `environment.yml` using
```
conda env create -f environment.yml
```
* activate your conda environment using
```
conda activate recommender
```
* `recommender_models.ipynb` is the main notebook to run
* it uses preprocess dataframes that are in the dataframes/ folder so there is no need to run preprocessing.ipynb again
* GPU is required to train the model faster, but our code is GPU agnostic will also work with a cpu
* Training takes ~10 min with GPU

The spotify playlists dataset was downloaded from https://www.aicrowd.com/challenges/spotify-million-playlist-dataset-challenge

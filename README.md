# COMP 6321 Machine Learning Project - Group 18
Recommender system for spotify 1M playlist dataset using k-NN and NeuMF models

## Main Dependencies
* Pytorch
* Pandas
* Scikit learn
* Numpy
* Spotipy

## Folder Structure
```
./code/environment.yaml <-- conda environment for our project
./code/preprocessing.ipynb <-- notebook to preprocess our data
./code/recommender_models.ipynb <-- primary notebook to run the k-NN and NeuMF models
./code/raw_data/ <-- subset of spotify's original 5gb dataset
./code/dataframes/ <-- preprocessed dataframes containing playlists, tracks, genres
./code/model/ <-- trained neuMF model will save to this folder when run
```



## Setup
* create conda environment from `environment.yml` using
```
conda env create -f environment.yml
```
* activate your conda environment using
```
conda activate recommender
```
* If using a jupyter notebook, use this command to create this pykernel, later change your kernel to this on jupyter.
```
python -m ipykernel install --user --name recommender --display-name "Recommender"
```

## Instructions
* `recommender_models.ipynb` is the main notebook to run
* it uses preprocess dataframes that are in the dataframes/ folder so there is no need to run preprocessing.ipynb again
* GPU is required to train the model faster, but our code is GPU agnostic will also work with a cpu
* Training takes ~10 min with GPU

## Dataset
The spotify playlists dataset was downloaded from https://www.aicrowd.com/challenges/spotify-million-playlist-dataset-challenge


## Acknowledgements
Some of the resources we've used to learn how to create a recommender model
1. https://github.com/microsoft/recommenders - Has the best practices for recommender systems
2. https://github.com/guoyang9/NCF - as a reference to build our NeuMF model
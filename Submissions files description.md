# ECS750P-MSc-Project-Computing-and-Information-Systems

#Introduction

The code in the two Jupyternotebook files, 'Movie Collaborative Filtering Recommendation with SVD and KNNWithMeans.ipynb' and 'Hybrid context-based Collaborative Filtering model using Tensorflow.ipynb', was used to create multiple recommendation system models for my MSc Project. The files only contain a selection of the full code that I produced during this project as I experimented with many different tensorflow and KNN models. Almost all of the code in the files was used to create the models referenced in my MSc paper and I have omitted code involved in creating the other models. 

#File 1: 'Hybrid context-based Collaborative Filtering model using Tensorflow.ipynb'

There are three sections to this file. The first part performs data cleaning and features selection, helping to put the user-ratings data into a sutiable format to be fed into the Tensorflow model. The second section builds tensorflow models and visualises the results. The models referred to in my report are model 14 and 15. Model 15 creates two embeddings- one from user-id and and one from film_id. Model 14 creates 3 embeddings- one for each of contextual information, user_id and film_id. The purpose of creating these two models is to compare the effect of incorporating contextual information into the tensorflow model and to develop an effective hybrid approach for recommendation using deep learning. The third section was carried out before section two and prepares the contextual information in a suitable format to be fed into model 14. In this section, contextual information is extracted from the dataset and put into a separate 'bagofwords' column. TF-IDF is then applied to the bagofwords column. This creates a large number of columns from the bagofwords column, so PCA was then performed on the data to reduce dimensionality.

#File 2: 'Movie Collaborative Filtering Recommendation with SVD and KNNWithMeans.ipynb'

This file uses the surprise library to create variations of recommendation systems using SVD and KNNWithMeans. I chose to use the surprise library since it is geared towards parameter tuning and granted me high control over my experiments. I applied neighborhood (KNNWithMeans) and matrix-factorisation-based (SVD) methods to the user_ratings data. I experimented with adding pearson and cosine similarity measures to the KNN models, and created a mixture of user-based and item-based collaborative-filtering models. 


# Predicting Global Clustering Coefficient with Graph Neural Network
In graph analytics, one of the most important graph-level metrics is the global clustering coefficient. This statistic measures the tendency of the graph to 'cluster' and can provide valuable insights in many real-world applications. The literature offers many methods with different definitions of clustering coefficient and propose different algorithms for its computation, which can either yield exact results or approximated estimates. In particular, one of the most widely studied problem is the computation of graph analytics for large graphs. In this report is proposed an approach based on a Graph Neural Network (GNN) model to compute the global clustering coefficient. The research aims to contribute to the development of a fast and reliable model for predicting the global clustering coefficient. The experimental results highlight the difficulty of this regression task, particularly the high risk of underfitting in small models when working with datasets of graphs of different sizes and domains under limited computational resources. However, this work may enable future advancements in methods for scaling GNN models for large graphs.

This project aims to design and train a Graph Neural Network (GNN) for predicting, given in input an undirected graph and its node feature vectors, its global clustering coefficient. 

# Repository structure
The repository is structured in folders:
-  The `root` contains all the Jupyter notebooks needed for preparing the dataset and training the GNN model.
-  The `/model` folder contains the trained model.
-  The `/datasets` folder contains the all the datasets folders and the `/test_data` folder where is stored/saved the data for replicating the model test.

NOTE: the `/datasets` folder should include all the folders extracted from the `.zip` files of the datasets considered for the experiment.

# Execution steps for model training and validation
In order to perform the training of the GNN, the execution must follow these steps:
1.  For each dataset in `/dataset`, run the `graph_label_dataset.ipynb` notebook to compute the labels of the graphs in the datasets. The output is saved inside the relative dataset folder.
2.  For each dataset in `/dataset`, run the `graph_to_tensor.ipynb` notebook to compute the tensors containing the edge indices of the graphs in the datasets. The output is saved inside the relative dataset folder.
3.  For each dataset in `/dataset`, run the `node_features.ipynb` notebook to compute the tensors containing the node feature vectors of the graphs in the datasets. The output is saved inside the relative dataset folder.
4.  Run the `training_gnn.ipynb` notebook to train, validate, test and save the GNN model.
5.  Run the `test_gnn.ipynb` notebook to replicate the test.

NOTE: for the the first three Jupyter notebooks in the enumerated list, it is needed to change the variable `dataset_name` with the name of the dataset to process.

# Datasets
The considered datasets are `ENZYMES`, `DD` and `COLLAB`, which are composed by graphs coming from different domains.

The datasets contains a total of 6778 graph samples, divided in 80% for training, 10% for validation and 10% for testing.

-  ENZYMES link: [https://networkrepository.com/ENZYMES.php](https://networkrepository.com/ENZYMES.php)
-  DD link: [https://networkrepository.com/DD.php](https://networkrepository.com/DD.php)
-  COLLAB link: [https://networkrepository.com/COLLAB.php](https://networkrepository.com/COLLAB.php)

It is possible to download the precomputed labels, node feature vectors and graph tensors in the following link: [https://drive.google.com/drive/folders/1AT7ghxuobigcdKEIoQontgZlBwdDqM9u?usp=sharing](https://drive.google.com/drive/folders/1AT7ghxuobigcdKEIoQontgZlBwdDqM9u?usp=sharing)

# Authors
-  Fabrizio Genilotti
-  Federico Pivotto
-  Francesco Boscolo Meneguolo

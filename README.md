# Predicting Global Clustering Coefficient with Graph Neural Network
Graph Neural Network to predict the global clustering coefficient on graphs of different sizes and verify its accuracy with respect to the ground truth.

# Repository structure
The repository is structured in folders:
-  The `root` contains all the Jupyter notebooks needed for preparing the dataset and training the GNN model.
-  The `/model` folder contains the trained model.
-  The `/datasets` folder contains the all the datasets folder.

# Execution steps for model training and validation
In order to perform the training of the GNN, the execution must follow these steps:
1.  For each dataset in `\dataset`, run the `graph_label_dataset.ipynb` notebook to compute the labels of the graphs in the datasets. The output is saved inside the relative dataset folder.
2.  For each dataset in `\dataset`, run the `graph_to_tensor.ipynb` notebook to compute the tensors containing the edge indices of the graphs in the datasets. The output is saved inside the relative dataset folder.
3.  For each dataset in `\dataset`, run the `node_features.ipynb` notebook to compute the tensors containing the node feature vectors of the graphs in the datasets. The output is saved inside the relative dataset folder.
4.  Run the `training_gnn.ipynb` notebook to train, validate, test and save the GNN model.

# Datasets
The considered datasets are `ENZYMES`, `DD` and `COLLAB`, which are composed by graphs coming from different domains.

The datasets contains a total of 6778 graph samples, divided in 80% for training, 10% for validation and 10% for testing.

-  ENZYMES link: [https://networkrepository.com/ENZYMES.php](https://networkrepository.com/ENZYMES.php)
-  DD link: [https://networkrepository.com/DD.php](https://networkrepository.com/DD.php)
-  COLLAB link: [https://networkrepository.com/COLLAB.php](https://networkrepository.com/COLLAB.php)

# Authors
-  Fabrizio Genilotti
-  Federico Pivotto
-  Francesco Boscolo Meneguolo

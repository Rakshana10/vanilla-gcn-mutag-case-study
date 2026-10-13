# vanilla-gcn-mutag-case-study
Implementation of Vanilla GCN for molecular graph classification using the MUTAG dataset.

# Vanilla GCN for Molecular Graph Classification Using MUTAG

1. Introduction
This project implements a Vanilla Graph Convolutional Network (GCN) for molecular graph classification using the MUTAG dataset.

2. Objective
- Understand the mathematical foundation of GCN.
- Calculate the normalized adjacency matrix manually.
- Implement graph convolution using PyTorch Geometric.
- Classify molecular graphs into two classes.
- Evaluate performance using classification metrics.

3. Dataset
MUTAG is a molecular graph classification dataset containing 188 graphs. Nodes represent atoms, edges represent bonds, and each graph has a binary class label.

Dataset: https://pytorch-geometric.readthedocs.io/en/latest/generated/torch_geometric.datasets.TUDataset.html

4. Methodology
1. Load the MUTAG dataset.
2. Perform manual graph convolution calculations on a small example.
3. Split the dataset into training and testing sets.
4. Train a two-layer Vanilla GCN.
5. Apply global mean pooling for graph-level classification.
6. Evaluate the model using accuracy, precision, recall, F1-score and a confusion matrix.

5. Graph Convolution Equation
H(l+1) = σ(D̃^(-1/2) Ã D̃^(-1/2) H(l) W(l))

Where Ã = A + I, D̃ is the degree matrix, W is the learnable weight matrix, and σ is an activation function.

6. Technologies
- Python
- PyTorch
- PyTorch Geometric
- NumPy
- Matplotlib
- Scikit-learn

7. Results
The notebook generates the actual test metrics, a confusion matrix and a training loss plot. Results depend on the training configuration and random seed.

8. Execution
Open `vanilla_gcn_mutag.ipynb` in Google Colab and run the cells sequentially.

9. Limitations
MUTAG is a small dataset. The reported test metrics are based on a single train/test split and should not be interpreted as proof of generalization to other molecular datasets.

## 9. Limitations
MUTAG is a small dataset. The reported test metrics are based on a single train/test split and should not be interpreted as proof of generalization to other molecular datasets.

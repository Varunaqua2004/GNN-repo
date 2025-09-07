# GNN-repo
Graphical Neural Networks for predicting Molecular Properties.
<br>
# Tool Stack:
1. Python
2. PyTorch Geometric (PyG)
3. RDKit
4. DeepChem
5. Scikit-Learn
6. TensorFlow
7. Keras
8. Matplotlib
## Graph Neural Networks for predicting Solubility of ESOL Dataset Molecules.

### Step 1. Dataset: ESOL

> ESOL (Delaney dataset): ~1,128 compounds with experimental aqueous solubility values.

> Each molecule is given as a SMILES string (text form) that we’ll convert into a graph.

> Labels: solubility values (LogS).

### Step 2. Graph Construction

For each molecule:

> Nodes: atoms (features = atomic number, valence, aromaticity, etc.).

> Edges: bonds (features = bond type: single, double, aromatic).

> We’ll use RDKit to process SMILES into graphs and PyTorch Geometric (PyG) to store them as Data objects.

### Step 3. Model: GCN Baseline

> We’ll build a Graph Convolutional Network (GCN):

> Input layer → takes atom features.

> GCN layers → perform message passing between atoms.

> Global pooling → aggregates all atom embeddings into a molecule embedding.

> Fully connected layer → predicts solubility value.

### Step 4. Training Pipeline

> Loss: MSE (Mean Squared Error), since this is regression.

> Optimizer: Adam.

> Evaluation: RMSE (Root Mean Squared Error).

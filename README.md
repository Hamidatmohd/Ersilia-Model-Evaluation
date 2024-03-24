# Ersilia Model-Evaluation - Eos6oli

# Repository Organization
The repository is organized as follows:
* '/data' contains the reference_libraby dataset used for the model bias and aqsol dataset used for model reproducibility.
* '/notebooks' contains the jupyter notebooks that houses all the code used.
* '/src' contains important functions used to aviod repetition.
* '/figures' contains the plot produced during the model validation from the model bias task.
* 'requirement.txt' lists all the required packages and libraries needed to run the notebooks.
  
# Model Abstract
The contents of this repository encompass the codes and datasets utilized in validating the eos6oli model. This model, chosen for predictions in the Model Bias and Reproducibility initiative for Outreachy contributors in 2024, centers on implementing the SolTranNet tool. It leverages the molecular transformer to forecast the aqueous solubility of compounds, a crucial aspect in drug discovery. Input for this prediction is based on the SMILES representation of a molecule.

# Model Characteristics
* Input: `Compound (SMILES)`
* Input shape: `Single`
* Task: `Regression`
* Output: `Experimental value`
* Output shape: `Single (Predicted log of solubility of the compound)`

# Installation Process for Ersilia
Follow this [step](https://ersilia.gitbook.io/ersilia-book/ersilia-model-hub/installation) to install Ersilia on Ubuntu

OR follow this for a python enivornmnet [Ersilia Google Colab Guide](https://github.com/ersilia-os/ersilia/blob/master/notebooks/ersilia-on-colab.ipynb)

# Installation Process for SolTranNet

Getting Started: Tested on Ubuntu 18.04.5, Ubuntu 20.04.2, Debian 10, Fedora 33, CentOS 8.3.2011, Windows 10, and Ubuntu 20.04.2 subsystem for Windows 10

First, install [RDKit](https://github.com/rdkit/rdkit). Installation instructions are available [here](https://github.com/rdkit/rdkit/blob/master/Docs/Book/Install.md)

After RDKit has finished installing, you can install SolTranNet via pip:

`python3 -m pip install soltrannet`

NOTE: This installation method often mismatches installation of PyTorch for enabling CUDA if it needs to install PyTorch as a dependency.

If you wish to do a more careful installation:
`python3 -m pip install --install-option test soltrannet`

This will run our unit tests to ensure that GPU-enabled torch was setup correctly, and the proper functioning of SolTranNet as a command line tool and within a python environment.

# References
[Soltrannet](https://github.com/gnina/SolTranNet)

[Soltranet Datasets and Figures Generations Repository](https://github.com/francoep/SolTranNet_paper)

[Publication](https://pubs.acs.org/doi/10.1021/acs.jcim.1c00331)




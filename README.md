# ViRel: Unsupervised Visual Relations Discovery with Graph-level Analogy

[Paper](https://arxiv.org/abs/2207.00590) | [Poster](https://github.com/snap-stanford/virel/blob/master/poster.pdf) | [Project page](http://snap.stanford.edu/virel/)

This is the official repo for [ViRel: Unsupervised Visual Relations Discovery with Graph-level Analogy](https://arxiv.org/abs/2207.00590) (Zeng et al. ICML 2022 Beyond Bayes Workshop). ViRel is a method for unsupervised discovery and learning of visual relations with graph-level analogy.


Abstract:

We introduce Visual Relations with graph-level analogy (ViRel), a method for unsupervised discovery and learning of visual relations with graph-level analogy. In a grid-world based dataset that test visual relation reasoning, it achieves above 95% accuracy in unsupervised relation classification, discovers the relation graph structure for most tasks, and further generalizes to unseen tasks with more complicated relational structures.


Installation
==========================================================================
First clone the directory. Then run the following command to initialize the submodules:

```bash
git submodule init; git submodule update
```
(If you encounter a "no permission" error, you may need to [add a new SSH key to your GitHub account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account).)

This repository also has the following dependencies:

- `PyTorch <https://pytorch.org/>`_ >= 1.9.1
- `pytorch-geometric <https://github.com/rusty1s/pytorch_geometric>`__
- networkx

The included `environment.yml` file can be used to create a conda environment with all dependencies installed:

```bash
conda env create -f environment.yml
conda activate virel
```

# Dataset:
The dataset files can be generated using the BabyARC engine in the `BabyARC` submodule.

# Running:
To run the code, use the following command:

```bash
python relation_analogy.py
```

To specify the hyperparameters, pass in the path to the .yaml file config, such as:

```bash
python relation_analogy.py --yaml config/main1.yaml
```

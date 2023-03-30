# Tabular

Examples of training neural network on tabular data.

### Example 1: Quick Start

**notebooks/train_neural_network_tabular.ipynb**:

* Simple Feedforward Neural Network.
* How to perform basic tasks in PyTorch: create DataLoader, training/evaluation loop, etc...
* Comparison with untuned XGBoost.

## Installation

```
conda create -yn tabular python=3.9
conda activate tabular 
pip install -r requirements.txt

# Cleanup
conda deactivate tabular
conda env remove -n tabular
```

## Data

Whether a person subscribes to a term deposit (yes/no).
* https://archive.ics.uci.edu/ml/datasets/bank+marketing


## Sanity checklist

* [ ] Did you start with a simple model?
* [ ] Does training loss go to zero if I fit on a single batch?
* [ ] Did you toggle between train/eval mode?
* [ ] Did you zero out the previous gradients (optimizer.zero_grad) before calculating the new ones (loss.backward)?
* [ ] Does model training loss go down as I increase it's capacity?
* [ ] Does the model perform worse when I zero out my training data?
# Tabular Neural Network

Self-contained examples of training neural networks on tabular data.

**train_neural_net**

* Simple Feedforward Neural Network.
* How to perform basic tasks in PyTorch: create DataLoader, training/evaluation loop, etc...
* Comparison with untuned XGBoost.

**train_transformer**

* Replace simple Feedforward Neural Network with Transformer network.
* Otherwise, same as before.

**hpo_sweep**

* Run a simple HPO sweep on a variety of hyperparameters.
* Parallelize search on CPU using `Parallel` from `joblib`.

**optimal_learning_rate**

* Run a single epoch and observe change in loss as you gradually increase the learning rate.


## Installation

```
conda create -yn tabular python=3.9
conda activate tabular 
pip install -r requirements.txt

# Cleanup
conda deactivate tabular
conda env remove -n tabular
```

## Development checklist

Here is a simple check-list, which I drew inspiration from Karpathy's [blog post](http://karpathy.github.io/2019/04/25/recipe/).

* [ ] Did you start with a simple model?
* [ ] Does training loss go to zero if I fit on a single batch?
* [ ] Did you toggle between train/eval mode?
* [ ] Did you zero out the previous gradients (optimizer.zero_grad) before calculating the new ones (loss.backward)?
* [ ] Does model training loss go down as I increase it's capacity?
* [ ] Does the model perform worse when I zero out my training data?
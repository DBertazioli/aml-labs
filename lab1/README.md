# Lab 1: Optimization

Training a neural network in Keras, how optimizers behave, and a training competition against the class.

## Plan

- Framework basics, sanity checks and toy data (notebook 1).
- Optimizer recap and the 3D optimizer race.
- Depth recap (vanishing gradients) and the Going Deep demo.
- Competition (notebook 2).

## Notebooks

| Notebook | Keras | PyTorch |
|---|---|---|
| 1. Framework basics, toy data, optimizer and depth recaps | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DBertazioli/aml-labs/blob/main/lab1/1_toy_keras.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DBertazioli/aml-labs/blob/main/lab1/1_toy_pytorch.ipynb) |
| 2. Training competition | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DBertazioli/aml-labs/blob/main/lab1/2_competition_keras.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DBertazioli/aml-labs/blob/main/lab1/2_competition_pytorch.ipynb) |

Registration on the class server (campus email and nickname) is in notebook 2, at the start of the competition.

## Demos

- Optimizer race in 3D: https://dbertazioli.github.io/aml-labs/lab1/race3d/
- Going Deep (signal tower, plain vs residual playground): https://dbertazioli.github.io/aml-labs/lab1/deep/#tower

## Competition

Leaderboard: https://dbertazioli-aml-labs.hf.space/board?c=speedrun,light

The dataset is "nested shells": 5 classes, 20 columns. In 3-D the same rule is 5 shells, one inside the other, and the class is the shell a point lies in. The competition data uses the same rule in 20 dimensions, which cannot be drawn. Two formats:

- **speedrun**: any MLP, at most 1000 optimizer steps at batch size 128.
- **light**: any MLP, at most 50,000 parameters and at most 40 epochs.

Rules:

- Honor system: the server does not check the limits. The notebook helpers count steps, epochs, batch size and parameters from the real training, refuse a submission over budget, and send the numbers with every submission.
- Unlimited submissions (at most one every 20 seconds, counted separately for each leaderboard).
- Any MLP: Dense layers, any activation, BatchNorm and Dropout are allowed; no convolutions or other model types.
- The score you see uses half of the test set. The final ranking uses, for each student, the submission with the best visible score, scored on the hidden half.

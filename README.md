# POS-Tagging
POS tagging using the Viterbi algorithm and n-gram models.

## Tech :hammer_and_wrench: Languages and Tools :

<div>
  <img src="https://github.com/devicons/devicon/blob/master/icons/python/python-original.svg" title="Python" alt="Python" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/jupyter/jupyter-original.svg" title="Jupyter Notebook" alt="Jupyter Notebook" width="40" height="40"/>&nbsp;
  <img src="https://assets.st-note.com/img/1670632589167-x9aAV8lmnH.png" title="Google Colab" alt="Google Colab" width="40" height="40"/>&nbsp;
  <img src="https://raw.githubusercontent.com/psf/requests/master/ext/requests-logo.png" title="Request" alt="Request" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/numpy/numpy-original.svg" title="Numpy" alt="Numpy" width="40" height="40"/>&nbsp;
  <img src="https://avatars.githubusercontent.com/u/83768144?s=200&v=4"  title="Pandas" alt="Pandas" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/matplotlib/matplotlib-original.svg"  title="MatPlotLib" alt="MatPlotLib" width="40" height="40"/>&nbsp;
  <img src="https://cdn.worldvectorlogo.com/logos/seaborn-1.svg"  title="seaborn" alt="seaborn" width="40" height="40"/>&nbsp;
</div>

## Run the Notebook on Google Colab

You can easily run this code on google colab by just clicking this badge [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AsadiAhmad/POS-Tagging/blob/main/Code/POS_Tagging.ipynb)

## Dataset

the dataset is a train set and the test set we create the validation set from the train set for validating our model. 

here is part of the train set frame :

<img src="/Pictures/1.PNG"/>

here is part of the test set frame :

<img src="/Pictures/2.PNG"/>

## Formula

here is our formula we need

```math
P(T|W) = argmax_T P(W|T)P(T_i) \quad \text{(Unigram)}
```

```math
P(T|W) = argmax_T P(W|T)P(T_i|T_{i-1}) \quad \text{(Bigram)}
```

```math
P(T|W) = argmax_T P(W|T)P(T_i|T_{i-1},T_{i-2}) \quad \text{(Trigram)}
```

so for calculating the `P(T|W)` we should calculate the `emission` and `transition` model.\
the `P(W|T)` is the `emission` section and the `P(Ti)` is the transition section calculated by ngram

## Conclusion

here is different accuracy from different N-gram model we can compare them together :

`Uni-gram` :

Accuracy: 25.5772\
Precision: 40.7354\
Recall: 40.7354\
F1-score: 40.7354

`Bigram` :

Accuracy: 92.4962\
Precision: 96.1019\
Recall: 96.1019\
F1-score: 96.1019

`Trigram` :

Accuracy: 92.3538\
Precision: 96.0249\
Recall: 96.0249\
F1-score: 96.0249

## License

This project is licensed under the MIT License.

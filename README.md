# recurrent-slds
Recurrent Switching Linear Dynamical Systems (rSLDS), like the standard SLDS upon which they are based, are models for decomposing nonlinear time-series data into discrete segments with relatively simple dynamics.  The _recurrent_ SLDS introduces an additional dependency between the discrete and continuous latent states, allowing the discrete state probability to depend upon the previous continuous state.  These dependencies are highlighted in red in the graphical model below. 

![Probabilistic Model](https://raw.githubusercontent.com/slinderman/recurrent-slds/master/aux/rslds_inputs_colorful.jpg)

These dependencies effectively cut up the continuous latent space into partitions with unique, linear dynamics.  Composing these pieces gives rise to globally nonlinear dynamics.  Here's an example of a 2D continuous latent state:

![Probabilistic Model](https://raw.githubusercontent.com/slinderman/recurrent-slds/master/aux/prior2.jpg)

In control literature, these models are known as _hybrid systems_.  We develop efficient Bayesian inference algorithms for a class of recurrent SLDS. The important ingredient is an augmentation scheme to enable conjugate block Gibbs updates of the continuous latent states. Complete details of the algorithm are given in the following paper:

Linderman, S. W., Miller, A. C., Adams, R. P., Blei, D. M., Paninski, L., & Johnson, M. J. (2016). Recurrent switching linear dynamical systems. _arXiv preprint arXiv:1610.08466_.

```
@inproceedings{linderman2016recurrent,
  title={Recurrent switching linear dynamical systems},
  author={Linderman, Scott W and Miller, Andrew C and Adams, Ryan P and Blei, David M and Paninski, Liam and Johnson, Matthew J},
  booktitle={To appear in AISTATS},
  year={2017}
}
```





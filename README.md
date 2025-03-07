# TT-layer learning
A small and simple application of TT-layer to neural network.  

"TT" is the abbreviation of "Tensor Train",which is a tensor decomposition method proposed by [I. V.OSELEDETS](https://users.math.msu.edu/users/iwenmark/Teaching/CMSE890/TENSOR_oseledets2011.pdf).  

See [Tensorizing Neural Networks](https://arxiv.org/abs/1509.06569) for a detailed description of TT-layers.Basically it can replace the fully connected layer by tensoring input vector, weight matrix and output vector to cut the numbers of parameters while maintaining nearly the same accuracy of the operation.  

The pytorch implementation of Tensor-Train decomposition and TT-layer are contributed to by [Ion Gabriel Ion](https://github.com/ion-g-ion/torchTT).

In "train.ipynb" we use the TT-layer to replace a fully connected layer of a simple convolutional neural network with a TT-layer(with different tt_ranks) on CIFAR-10 dataset and compare the parameters and other performance of the two different models.  

It's just a simple application of TT-layer with no innovation.

# Requirements
Following requirements are needed:

- `python>=3.8`
- `torch>=1.7.0`
- `numpy>=1.18`
- [`opt_einsum`](https://pypi.org/project/opt-einsum/)

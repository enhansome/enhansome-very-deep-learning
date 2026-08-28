# Awesome very deep learning with stars

<div align="center">
  <img width='600px' src="http://i.imgur.com/XjCXXap.png"><br><br>
</div>

***

**awesome-very-deep-learning** is a curated list for papers and code about implementing and training very deep neural networks.

## Neural Ordinary Differential Equations

**ODE Networks** are a kind of continuous-depth neural network. Instead of specifying a discrete sequence of hidden layers, they parameterize the derivative of the hidden state using a neural network. The output of the network is computed using a black-box differential equation solver. These continuous-depth models have constant memory cost, adapt their evaluation strategy to each input, and can explicitly trade numerical precision for speed.

### Papers

* [Neural Ordinary Differential Equations (2018)](https://arxiv.org/abs/1806.07366) [\[original code\]](https://github.com/rtqichen/torchdiffeq) ⭐ 6,477 | 🐛 95 | 🌐 Python | 📅 2025-04-04, introduces several ODENets such as continuous-depth residual networks and continuous-time latent variable models. The paper also constructs continuous normalizing flows, a generative model that can train by maximum likelihood, without partitioning or ordering the data dimensions. For training, the authors show how to scalably backpropagate through any ODE solver, without access to its internal operations. This allows end-to-end training of ODEs within larger models. NIPS 2018 best paper.
* [Augmented Neural ODEs (2019)](https://arxiv.org/abs/1904.01681), neural ODEs preserve topology, thus their learned flows can't intersect with each other. Therefore some functions can't be learned. Augmented NODEs improve upon this by adding an additional dimension to learn simpler flows.

### Implementations

1. Authors [Autograd Implementation](https://github.com/HIPS/autograd/blob/master/examples/ode_net.py) ⭐ 7,524 | 🐛 181 | 🌐 Python | 📅 2026-08-24

## Value Iteration Networks

**Value Iteration Networks** are very deep networks that have tied weights and perform approximate value iteration. They are used as an internal (model-based) planning module.

### Papers

* [Value Iteration Networks (2016)](https://arxiv.org/abs/1602.02867) \[[original code](https://github.com/avivt/VIN) ⭐ 291 | 🐛 10 | 🌐 Python | 📅 2017-04-21], introduces VINs (Value Iteration Networks). The author shows that one can perform value iteration using iterative usage of convolutions and channel-wise pooling. It is able to generalize better in environments where a network needs to plan. NIPS 2016 best paper.

## Densely Connected Convolutional Networks

**Densely Connected Convolutional Networks** are very deep neural networks consisting of dense blocks. Within dense blocks, each layer receives the feature maps of all preceding layers. This leverages feature reuse and thus substantially reduces the model size (parameters).

### Papers

* [Densely Connected Convolutional Networks (2016)](https://arxiv.org/abs/1608.06993) \[[original code](https://github.com/liuzhuang13/DenseNet) ⭐ 4,869 | 🐛 30 | 🌐 Lua | 📅 2024-01-09], introduces DenseNets and shows that it outperforms ResNets in CIFAR10 and 100 by a large margin (especially when not using data augmentation), while only requiring half the parameters. CVPR 2017 best paper.

### Implementations

1. [Keras Implementation](https://github.com/tdeboissiere/DeepLearningImplementations/tree/master/DenseNet) ⭐ 1,812 | 🐛 24 | 🌐 Python | 📅 2020-10-23 by tdeboissiere.
2. [Lasagne Implementation](https://github.com/Lasagne/Recipes/tree/master/papers/densenet) ⭐ 935 | 🐛 37 | 🌐 Python | 📅 2022-10-15 by Jan Schlüter.
3. [PyTorch Implementation](https://github.com/bamos/densenet.pytorch) ⭐ 839 | 🐛 7 | 🌐 Python | 📅 2018-08-16
4. [Tensorflow Implementation](https://github.com/YixuanLi/densenet-tensorflow) ⭐ 563 | 🐛 10 | 🌐 Python | 📅 2019-05-07 by Yixuan Li.
5. [PyTorch Implementation (including BC structures)](https://github.com/andreasveit/densenet-pytorch) ⭐ 486 | 🐛 6 | 🌐 Python | 📅 2018-02-28 by Andreas Veit
6. Authors' [Caffe Implementation](https://github.com/liuzhuang13/DenseNetCaffe) ⭐ 267 | 🐛 9 | 🌐 Python | 📅 2017-08-11
7. [Tensorflow Implementation](https://github.com/LaurentMazare/deep-models/tree/master/densenet) ⭐ 144 | 🐛 4 | 🌐 Python | 📅 2018-11-30 by Laurent Mazare.
8. [Chainer Implementation](https://github.com/yasunorikudo/chainer-DenseNet) ⭐ 39 | 🐛 1 | 🌐 Python | 📅 2017-07-15 by Yasunori Kudo.
9. [Keras Implementation](https://github.com/robertomest/convnet-study) ⭐ 35 | 🐛 0 | 🌐 Python | 📅 2017-03-24 by Roberto de Moura Estevão Filho.
10. Authors' more memory-efficient [Torch Implementation](https://github.com/gaohuang/DenseNet_lite) ⭐ 29 | 🐛 0 | 🌐 Lua | 📅 2017-05-11.
11. [Chainer Implementation](https://github.com/t-hanya/chainer-DenseNet) ⭐ 5 | 🐛 0 | 🌐 Python | 📅 2017-11-12 by Toshinori Hanya.

## Deep Residual Learning

**Deep Residual Networks** are a family of extremely deep architectures (up to 1000 layers) showing compelling accuracy and nice convergence behaviors. Instead of learning a new representation at each layer, deep residual networks use identity mappings to learn residuals.

### Papers

* [Deep Residual Learning for Image Recognition (2015)](http://arxiv.org/abs/1512.03385) \[[original code](https://github.com/KaimingHe/deep-residual-networks) ⭐ 6,753 | 🐛 58 | 📅 2017-10-28], original paper introducing residual neural networks
* [Squeeze-and-Excitation Networks](https://arxiv.org/abs/1709.01507) \[[original code](https://github.com/hujie-frank/SENet) ⭐ 3,646 | 🐛 16 | 🌐 Cuda | 📅 2019-02-25], introduces Squeeze-and-Excitation (SE) block, that adaptively recalibrates channel-wise feature responses. It achieved the 1st place on ILSVRC17.
* [Wide Residual Networks (2016)](http://arxiv.org/abs/1605.07146) \[[orginal code](https://github.com/szagoruyko/wide-residual-networks) ⭐ 1,315 | 🐛 24 | 🌐 Lua | 📅 2019-08-20], studies wide residual neural networks and shows that making residual blocks wider outperforms deeper and thinner network architectures
* [Identity Mappings in Deep Residual Networks (2016)](http://arxiv.org/abs/1603.05027) \[[original code](https://github.com/KaimingHe/resnet-1k-layers) ⭐ 936 | 🐛 1 | 🌐 Lua | 📅 2017-05-24], improving the original proposed residual units by reordering batchnorm and activation layers
* [Deep Networks with Stochastic Depth (2016)](http://arxiv.org/abs/1603.09382) \[[original code](https://github.com/yueatsprograms/Stochastic_Depth) ⭐ 480 | 🐛 1 | 🌐 Lua | 📅 2018-08-13], dropout with residual layers as regularizer
* [The Reversible Residual Network: Backpropagation Without Storing Activations](https://arxiv.org/abs/1707.04585v1) \[[code](https://github.com/renmengye/revnet-public) ⭐ 362 | 🐛 5 | 🌐 Python | 📅 2018-06-19] constructs reversible residual layers (no need to store activations) and surprisingly finds out that reversible layers don't impact final performance.
* [Aggregated Residual Transformation for Deep Neural Networks (2016)](https://arxiv.org/abs/1611.05431), introduces ResNeXt, which aggregates a set of transformations within a a res-block. It achieved the 2nd place on ILSVRC16.
* [Residual Networks of Residual Networks: Multilevel Residual Networks (2016)](https://arxiv.org/abs/1608.02908), adds multi-level hierarchical residual mappings and shows that this improves the accuracy of deep networks
* [Swapout: Learning an ensemble of deep architectures (2016)](https://arxiv.org/pdf/1605.06465v1.pdf), improving accuracy by randomly applying dropout, skipforward and residual units per layer
* [Inception-v4, Inception-ResNet and the Impact of Residual Connections on Learning (2016)](http://arxiv.org/abs/1602.07261), inception network with residual connections

### Implementations

1. Tensorflow with skflow, with MNIST: [code](https://github.com/tensorflow/tensorflow/blob/master/tensorflow/examples/skflow/resnet.py) ⭐ 197,765 | 🐛 2,955 | 🌐 C++ | 📅 2026-08-28
2. Tensorflow with tflearn, with CIFAR-10 and MNIST: [code](https://github.com/tflearn/tflearn/blob/master/examples/images/residual_network_cifar10.py) ⭐ 9,576 | 🐛 579 | 🌐 Python | 📅 2024-05-06
3. Neon, Preactivation layer implementation: [code](https://github.com/NervanaSystems/neon/blob/master/examples/cifar10_msra.py) ⚠️ Archived
4. Torch by Facebook AI Research (FAIR), with **training code in Torch and pre-trained ResNet-18/34/50/101 models for ImageNet**: [blog](http://torch.ch/blog/2016/02/04/resnets.html), [code](https://github.com/facebook/fb.resnet.torch) ⚠️ Archived
5. ResNet in TensorFlow 0.9+ with pretrained caffe weights: [code](https://github.com/ry/tensorflow-resnet) ⚠️ Archived
6. Lasagne, CIFAR-10, with ResNet-32 and ResNet-56 and training code: [code](https://github.com/Lasagne/Recipes/tree/master/papers/deep_residual_learning) ⭐ 935 | 🐛 37 | 🌐 Python | 📅 2022-10-15
7. Torch, CIFAR-10, with ResNet-20 to ResNet-110, training code, and curves: [code](https://github.com/gcr/torch-residual-networks) ⭐ 582 | 🐛 10 | 🌐 Jupyter Notebook | 📅 2020-03-16
8. ResNet in PyTorch: [code](https://github.com/ruotianluo/pytorch-resnet) ⭐ 229 | 🐛 3 | 🌐 Python | 📅 2019-06-06
9. Neon, CIFAR-10, with pre-trained ResNet-32 to ResNet-110 models, training code, and curves: [code](https://github.com/NervanaSystems/ModelZoo/tree/master/ImageClassification/CIFAR10/DeepResNet) ⚠️ Archived
10. A winning entry in Kaggle's right whale recognition challenge: [blog](http://blog.kaggle.com/2016/02/04/noaa-right-whale-recognition-winners-interview-2nd-place-felix-lau/), [code](https://github.com/felixlaumon/kaggle-right-whale) ⭐ 173 | 🐛 2 | 🌐 Python | 📅 2016-04-16
11. Stochastic dropout in Keras: [code](https://github.com/dblN/stochastic_depth_keras) ⭐ 139 | 🐛 2 | 🌐 Python | 📅 2020-07-21
12. Wide Residual Networks in Keras: [code](https://github.com/asmith26/wide_resnets_keras) ⭐ 138 | 🐛 6 | 🌐 Python | 📅 2024-01-18
13. Ladder Network for Semi-Supervised Learning in Keras : [code](https://github.com/divamgupta/ladder_network_keras) ⭐ 99 | 🐛 6 | 🌐 Python | 📅 2021-04-30
14. ResNet in Chainer: [code](https://github.com/yasunorikudo/chainer-ResNet) ⭐ 55 | 🐛 2 | 🌐 Python | 📅 2017-07-27
15. Stochastic dropout in Chainer: [code](https://github.com/yasunorikudo/chainer-ResDrop) ⭐ 40 | 🐛 1 | 🌐 Python | 📅 2016-04-11
16. Torch, MNIST, 100 layers: [blog](https://deepmlblog.wordpress.com/2016/01/05/residual-networks-in-torch-mnist/), [code](https://github.com/arunpatala/residual.mnist) ⭐ 26 | 🐛 7 | 🌐 Lua | 📅 2016-01-10
17. Neon, Place2 (mini), 40 layers: [blog](http://www.nervanasys.com/using-neon-for-scene-recognition-mini-places2/), [code](https://github.com/hunterlang/mpmz/) ⭐ 16 | 🐛 0 | 🌐 Python | 📅 2016-02-05

In addition, this [code](https://github.com/ry/tensorflow-resnet) ⚠️ Archived by Ryan Dahl helps to convert the pre-trained models to TensorFlow.

## Highway Networks

**Highway Networks** take inspiration from Long Short Term Memory (LSTM) and allow training of deep, efficient networks (with hundreds of layers) with conventional gradient-based methods

### Papers

* [Recurrent Highway Networks (2016)](https://arxiv.org/abs/1607.03474) \[[original code](https://github.com/julian121266/RecurrentHighwayNetworks) ⭐ 404 | 🐛 3 | 🌐 Python | 📅 2019-10-09], introducing recurrent highway networks, which increases space depth in recurrent networks
* [Training Very Deep Networks (2015)](http://arxiv.org/abs/1507.06228), introducing highway neural networks

### Implementations

1. Lasagne: [code](https://github.com/Lasagne/Lasagne/blob/highway_example/examples/Highway%20Networks.ipynb) ⭐ 3,858 | 🐛 139 | 🌐 Python | 📅 2022-03-26
2. Torch: [code](https://github.com/yoonkim/lstm-char-cnn/blob/master/model/HighwayMLP.lua) ⭐ 837 | 🐛 15 | 🌐 Lua | 📅 2016-08-24
3. Caffe: [code](https://github.com/flukeskywalker/highway-networks) ⭐ 96 | 🐛 2 | 🌐 C++ | 📅 2015-09-20
4. Tensorflow: [blog](https://medium.com/jim-fleming/highway-networks-with-tensorflow-1e6dfa667daa#.r2msk226f), [code](https://github.com/fomorians/highway-cnn) ⭐ 56 | 🐛 0 | 🌐 Python | 📅 2016-09-18
5. PyTorch: [code](https://github.com/c0nn3r/pytorch_highway_networks/blob/master/layers/highway.py) ⚠️ Archived

## Very Deep Learning Theory

**Theories** in very deep learning concentrate on the ideas that very deep networks with skip connections are able to efficiently approximate recurrent computations (similar to the recurrent connections in the visual cortex) or are actually exponential ensembles of shallow networks

### Papers

* [Identity Matters in Deep Learning](https://arxiv.org/abs/1611.04231) considers identity parameterizations from a theoretical perspective and proofs that arbitrarily deep linear residual networks have no spurious local optima
* [The Shattered Gradients Problem: If resnets are the answer, then what is the question?](https://arxiv.org/abs/1702.08591) argues that gradients of very deep networks resemble white noise (thus are harder to optimize). Resnets are more resistant to shattering (decaying sublinearly)
* [Skip Connections as Effective Symmetry-Breaking](https://arxiv.org/pdf/1701.09175) hypothesizes that ResNets improve performance by breaking symmetries
* [Highway and Residual Networks learn Unrolled Iterative Estimation](https://arxiv.org/abs/1612.07771), argues that instead of learning a new representation at each layer, the layers within a stage rather work as an iterative refinement of the same features.
* [Demystifying ResNet](https://arxiv.org/abs/1611.01186), shows mathematically that 2-shortcuts in ResNets achieves the best results because they have non-degenerate depth-invariant initial condition numbers (in comparison to 1 or 3-shortcuts), making it easy for the optimisation algorithm to escape from the initial point.
* [Wider or Deeper? Revisiting the ResNet Model for Visual Recognition](https://arxiv.org/abs/1611.10080v1), extends results from Veit et al. and shows that it is actually a linear ensemble of subnetworks. Wide ResNet work well, because current very deep networks are actually over-deepened (hence not trained end-to-end), due to the much shorter effective path length.
* [Residual Networks are Exponential Ensembles of Relatively Shallow Networks](http://arxiv.org/abs/1605.06431), shows that ResNets behaves just like ensembles of shallow networks in test time. This suggests that in addition to describing neural networks in terms of width and depth, there is a third dimension: multiplicity, the size of the implicit ensemble
* [Bridging the Gaps Between Residual Learning, Recurrent Neural Networks and Visual Cortex](http://arxiv.org/abs/1604.03640), shows that ResNets with shared weights work well too although having fewer parameters
* [A Simple Way to Initialize Recurrent Networks of Rectified Linear Units](https://arxiv.org/abs/1504.00941), pre-ResNet Hinton paper that suggested, that the identity matrix could be useful for the initialization of deep networks
* [ResNet with one-neuron hidden layers is a Universal Approximator](https://arxiv.org/abs/1806.10909v2), ResNet increases representational power for narrow deep networks because the skip connection and one neuron per hidden layer can uniformly approximate any Lebesgue integrable function in d dimensions (in contrast to fully connected networks).

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-08-28._

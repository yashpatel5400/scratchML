# scratchML
ML from scratch (w/ accompanying blog posts)

## Motivation
This is an educational project, so the final state will be likely incomplete in terms of supported features and will almost certainly not have nearly the performance of any large scale industry equivalent. But developing these features directly from the math seemed like a really neat exercise that I wanted to improve on, especially since many of the features of modern ML libraries (at least the well developed ones) are so cleanly implemented that it's easy to completely ignore the abstracted away internals.

Most of the features I want to implement I'm hoping to pair up with blog posts upon their completion. This project should end up with features from both scikit-learn and PyTorch. I'll likely do one on more traditional CV stuff at some point in the future if this project turns out to be interesting (which it should be!).

## Features
From "scratch" here means that I'll be going from math to C++ implementations of the code. I also want to try to hook the C++ into a Python interface, since I've been curious about trying that out, and this seems like the perfect excuse. The C++ libraries I use should only come into the std:: or boost:: namespace, although maybe some unforeseen issues will arise. The features I want to implement are (probably in this order -- will add more detail to the list as I hit them):

Traditional ML
- Regressions (interesting part will be adding support for high dimensional matrix inversion using sparsity patterns -- if not for this, the closed form solutions lend themselves very easily to implementation)
  - Linear
  - w/ Regularization
  - Logistic (not really a regression, but I'll put it here out of tradition)
- Decision trees
- Decision forests
- AdaBoost
- Discriminant Analysis

Deep Learning -- want to model off of PyTorch. Goal is to have a Python interface with dynamic graph evaluation that can learn the MNIST dataset (i.e. with either just fully connected layers or using convolutions)

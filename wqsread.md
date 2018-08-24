# LDMNet: Low Dimensional Manifold Regularized Neural Networks

Implementation of the article ![LDMNet: Low Dimensional Manifold Regularized Neural Networks](http://www.ipam.ucla.edu/abstract/?tid=14951&pcode=DLT2018)

This project contains the python source and matlab source code for LDMNet.

The python source include mnist_1.py and mnist_2.py, which have the similar method, mnist_1.py contains the identity-layer.
And mnist_2.py contains the multi-task loss.

## How to Install MatConvNet Toolbox
The matlab source use the MatConvNet toolbox. If you don't have MatConvNet installed yet. Follow instructions to get it.
First install the MatConvNet toolbox (test the code on matconvnet-1.0-beta13 & matlab-R2014a with a Linux machine)

1.in the terminal, type
```
export LD_LIBRARY_PATH="$LD_LIBRARY_PATH:/usr/local/cuda-7.0/lib64"
```
2.Clone or Fork this repo, start matlab by open command window or `matlab -nodesktop -nosplash`
```
addpath MATLAB/matconvnet_extended/matlab
vl_compilenn('enableGpu', true, 'enableImreadJpeg',false,'cudaRoot', '/usr/local/cuda-7.0','enableCudnn', true, 'cudnnRoot', '/usr/local/cuda/lib64') ; 
run vl_setupnn
```
3.`cd MATLAB;run mnist.m` for a demo of LDMNet on the MNIST dataset.

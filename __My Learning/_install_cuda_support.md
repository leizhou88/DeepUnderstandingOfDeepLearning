# Install CUDA Support for PyTorch

Use this [main instruction](https://github.com/clementw168/install-and-test-gpu?form=MG0AV3) to complete the installation. 

___Important___: I have a Windows PC with GeForce RTX 4070 Ti Super, Nvdia CUDA Toolkit was already installed. I had to uninstall it and use the instruction provided on PyTorch website to install a CUDA driver whose version is compatible both to my GPU and the PyTorch version. 

## My installed versions

* Nvdia CUDA Toolkit 11.8 (WIndows install)
* Nvdia cuDNN API Frontend: cuDNN 9.6.0 Frontend for CUDA 11.x - I used `pip install` method as described on the [Nvidia Website's Python Install instruction](https://docs.nvidia.com/deeplearning/cudnn/latest/installation/windows.html)
* Pytorch install: pip install using website instruction 

Below are `pip` command lines - it means that _cuDNN and PyTorch are both installed to the venv only_: 

```python
python -m pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
```
```python
python -m pip install nvidia-cudnn-cu11==9.6.0.74
```

## Other useful links:

* https://en.wikipedia.org/wiki/CUDA#GPUs_supported
* https://pytorch.org/get-started/locally/

# Install cuDNN

This is needed for Pytorch and Tensorflow to effectively leverage the GPU capabilities. 

Here is the link: https://developer.nvidia.com/cudnn

According to Co-Pilot's explanation, I decided to install the cdDNN frontend API. 

## cuDNN Library
The cuDNN library is a GPU-accelerated library of primitives for deep neural networks. It provides highly optimized implementations for standard routines such as forward and backward convolution, attention, matrix multiplication (matmul), pooling, and normalization1. It's designed to deliver high performance on NVIDIA GPUs.

## cuDNN Frontend
The cuDNN Frontend is a C++ header-only library that wraps the cuDNN C backend API. It provides a more user-friendly interface and simplifies the workflow for defining and executing deep learning operations2. The Frontend API is less verbose and adds functionality on top of the backend API, such as errata filters and autotuning

## Do You Need Both?
For most users, it's recommended to use the cuDNN Frontend API as it simplifies the process of working with cuDNN. The Frontend API provides the same functionality as the backend API but with a more convenient and less verbose interface2. However, if you need more control or are working on specialized cases, you might choose to use the backend API directly.

In summary, while you don't necessarily need both, starting with the cuDNN Frontend API is generally recommended for ease of use and convenience.
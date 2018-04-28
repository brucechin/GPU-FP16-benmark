#Multi-GPU CUDA benchmark for half-precision

Although NVIDIA has brought up this idea for a long time, I can not find a benchmark to test my TITAN V GPU. This benchmark only for FP16 is based on [gpu-burn](https://github.com/wilicc/gpu-burn). My contribution is very small.

Makefile is only for Volta architecture.If you change the Makefile to make it compatible with other archs like Pascal/Tesla/Kepler and test it, the outcome will be slower than single-precision. Currently only P100(Pascal arch) is faster with half-precision than single-precision.

We use half-precision to speed up deep learning for it doesn't need much preicision, and this benchmark is just simply calculate matrix multiplication.

For more info on Tensor Core and Volta Arch:

[Volta Architecture](http://images.nvidia.com/content/volta-architecture/pdf/volta-architecture-whitepaper.pdf)

[Programming in Tensor Core](https://devblogs.nvidia.com/programming-tensor-cores-cuda-9/)

[NVIDIA Tensor Core Programmability,Performance & Precision](https://arxiv.org/pdf/1803.04014.pdf)

[why half-precision is slower more than single-precision when I use on GTX1070?](https://devtalk.nvidia.com/default/topic/972337/gpu-accelerated-libraries/why-cublashgemm-is-slower-more-than-cublassgemm-when-i-use-/)

#Usage

./gpu-burn 10(seconds)

You can modify SIZE or USEMEM to change the size of matrix or the percentage of used memory when testing.

By default, it will test all the GPU chips on your machine.

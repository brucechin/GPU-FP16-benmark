#Multi-GPU CUDA benchmark for half-precision

Makefile is only for Volta architecture.If you change the Makefile to make it compatible with other archs like Pascal/Tesla/Kepler and test it, the outcome will be slower than single-precision. Currently only P100(Pascal arch) is faster with half-precision than single-precision.

We use half-precision to speed up deep learning for it doesn't need much preicision, and this benchmark is just simply calculate matrix multiplication.

For more info on Tensor Core and Volta Arch:

[Volta Architecture]{http://images.nvidia.com/content/volta-architecture/pdf/volta-architecture-whitepaper.pdf}

[Programming in Tensor Core]{https://devblogs.nvidia.com/programming-tensor-cores-cuda-9/}

[NVIDIA Tensor Core Programmability,Performance & Precision]{https://arxiv.org/pdf/1803.04014.pdf}





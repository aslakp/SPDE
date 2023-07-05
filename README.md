# SPDE
This is a simple library aimed at doing simple vector arithmetic as well as some BLAS functionality. To start it is should be considered a learning experiment. The goal is to create a library where only a small amount of C++ knowledge is needed but still be able to get speedy performance. Hence, using the library for personal projects should be simple.

## Vector arithmetic
In the quest to solve e.g. PDE's or large linear systems, having an efficient vector class and operations is crucial. Additionally, from a user perspective, simplicity is crucial.
The implementation of basic vector arithmetic (BLAS1) is based on operator overloads and to achieve effiency we employ expression templates.

## Blas functionality
Any numerical library that aims to solve linear equations needs some form of BLAS implementation. We already touched upon BLAS1 functionality in the previous section. But here we will discuss BLAS functionality in greater detail.
We will not be targeting the performance of highly optimized libraries, but we will of course aim to achieve decent performance.

## Paralisation
For high performance libraries, it is not enough to simply use a high performance language like C++, we should also use the computational resources available. For this purpose the use of parallel programming techniques is central. The main driver will be openMP as it is simple, efficient and well supported by most compilers. In the future we also aim to leverage the power of the GPU. Currently openACC is considered for this application as it is a rather light weight implementation, directive based and can run on multiple platforms. Eventually, further parallisation might be added in the form of e.g. MPI to support distributed memory systems. 

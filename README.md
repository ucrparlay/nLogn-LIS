# Logn-LIS

## Compile
ParlayLib is required if you want to compile

## Usage
Type 0: Sequential LIS algorithm based on AVL

Type 1: Our weighted parallel LIS algorithm

Type 2: Array-based sequential LIS algorithm and our unweighted parallel LIS algorithm running on one core

Type 3: Our unweighted parallel LIS algorithm
```
./weighted_lis arraySize typeNumber inputfile

```
We implemented all algorithms in C++ using ParlayLib for fork-join parallelism and some parallel primitives. Here is some introduction about ParlayLib.

# ParlayLib - A Toolkit for Programming Parallel Algorithms on Shared-Memory Multicore Machines

[![Build status](https://github.com/cmuparlay/parlaylib/actions/workflows/build.yml/badge.svg?branch=master)](https://github.com/cmuparlay/parlaylib/actions)
[![Build status](https://ci.appveyor.com/api/projects/status/2458wr1nbcusxhqb/branch/master?svg=true)](https://ci.appveyor.com/project/DanielLiamAnderson/parlaylib/branch/master)
[![codecov](https://codecov.io/gh/cmuparlay/parlaylib/branch/master/graph/badge.svg)](https://codecov.io/gh/cmuparlay/parlaylib)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)


ParlayLib is a C++ library for developing efficient parallel algorithms and software on shared-memory multicore machines. It provides additional tools and primitives that go beyond what is available in the C++ standard library, and simplifies the task of programming provably efficient and scalable parallel algorithms. It consists of a sequence data type (analogous to std::vector), many parallel routines and algorithms, a work-stealing scheduler to support nested parallelism, and a scalable memory allocator. It has been developed over a period of seven years and used in a variety of software including the [PBBS benchmark suite](http://www.cs.cmu.edu/~pbbs/benchmarks.html), the [Ligra](http://jshun.github.io/ligra/), [Julienne](https://dl.acm.org/doi/pdf/10.1145/3087556.3087580), and [Aspen](https://github.com/ldhulipala/aspen) graph processing frameworks, the [Graph Based Benchmark Suite](https://github.com/ParAlg/gbbs), and the [PAM](https://cmuparlay.github.io/PAMWeb/) library for parallel balanced binary search trees, and an implementation of the TPC-H benchmark suite.

Parlay is designed to be reasonably portable by being built upon mostly standards-compliant modern C++. It builds on [GCC](https://gcc.gnu.org/) and [Clang](https://clang.llvm.org/) on Linux, GCC and Apple Clang on OSX, and Microsoft Visual C++ ([MSVC](https://visualstudio.microsoft.com/vs/)) and [MinGW](http://www.mingw.org/) on Windows. It is also tested on GCC and Clang via Windows Subsystem for Linux ([WSL](https://docs.microsoft.com/en-us/windows/wsl/about)) and [Cygwin](https://www.cygwin.com/). Support beyond x86-64 has not yet been explored. We would warmly welcome contributions that seek to achieve this.

# Documentation

You can find Parlay's full reference documentation [here](https://cmuparlay.github.io/parlaylib/)

# Examples

Parlay comes with over 50 example applications that you can learn from. You can find them in the [examples](./examples) directory.

# Developer documentation

If you are interested in contributing to Parlay, the following pages describe useful information about our testing and benchmarking setups. If you just want to use Parlay in your own projects, these links are not relevant to you.

* [Static analysis](./analysis/README.md)
* [Unit tests](./test/README.md)
* [Benchmarks](./benchmark/README.md)

# Optimize your code

This section provides a few "easy-to-implement" tips and trick to optimize (Python) code. Note that the Notebooks are *read-only* create a local copy to edit them and play around.

## Activity O1 - Python and C optimization notebook

You can access and copy the following Google [Colab notebook](https://colab.research.google.com/drive/10F_LoZgLSoruaVk5jKzAQ6Mz2PyD3--a?usp=sharing) to follow along.

## Activity O2 - Python profiling

In order to measure what to optimize we need to *profile* our code or scripts.

The Research Computing group of University of Leeds provides a Python notebook on profiling as part of their [high performance Python course](https://arc.leeds.ac.uk/training/courses/swd6/). It is available [here](https://colab.research.google.com/github/ARCTraining/swd6_hpp/blob/master/docs/01_profiling.ipynb)

## Activity O3 - Python HPC (high performance computing)

This Google [Colab notebook](https://colab.research.google.com/drive/1AWTMJ9VKkWwJyf5Xc8wlHeAY5I3x5PYs?usp=sharing) goes through several possibilities to optimize a Python function, from optimized libraries such as Numpy, to parallel computations, and GPU.

# Go back

[Go back to the main section](../README.md)

# Bash pipelines

**WIP**: This will be available in future versions of the workshop, don't hesitate to come and discuss if this is of interest to you.

**Bash pipelines tips and tricks**. Bash is often used to write scripts and pipelines in bioinformatics, so we'll show a few tricks that can help you in your research.

Methods include make good usage of multiple CPU core, e.g., use [pigz (parallel gzip)](https://zlib.net/pigz/) instead of gzip, use [GNU parallel](https://www.gnu.org/software/parallel/), monitor your CPU and RAM usage, plan your pipelines, optimize intra-tool data exchange (e.g., pipe uncompressed, binary data between your pipeline tools), etc.

# Algorithmic complexity

Example: Comparison of a few sorting algorithms : https://www.toptal.com/developers/sorting-algorithms

Understand algorithms through visualizations : https://visualgo.net/en

**WIP**: Exercises on this subject will be available in future versions of the workshop, don't hesitate to come and discuss if this is of interest to you.

# Cluster and Cloud computing

**WIP**: Cluster / Cloud computing access is not easily setup for a workshop, however if you are interested in methods to optimize your cluster / cloud computing usage, feel free to come and discuss !

Topics include, when to store data vs when to recompute, how to parallelize tasks, how to split your workloads, inter-task dependencies, spot compute vs high priority and more.
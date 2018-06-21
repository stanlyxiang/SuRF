# Succinct Range Filter (SuRF)
[![Build Status](https://travis-ci.org/efficient/SuRF.svg?branch=master)](https://travis-ci.org/efficient/SuRF)
[![Coverage Status](https://coveralls.io/repos/github/efficient/SuRF/badge.svg?branch=master)](https://coveralls.io/github/efficient/SuRF?branch=master)

**SuRF** is a fast and compact filter that provides exact-match filtering,
range filtering, and approximate range counts. This is the source code for our
[SIGMOD best paper](http://www.cs.cmu.edu/~huanche1/publications/surf_paper.pdf)
We also host a [demo website](https://www.rangefilter.io/).

## Build
    git submodule init
    git submodule update
    mkdir build
    cd build
    cmake ..
    make -j

## Run Unit Tests
    make test

## Benchmark

### Step 1: Download YCSB
    cd bench/workload_gen
    bash ycsb_download.sh

### Step 2: Generate Workloads
    cd bench/workload_gen
    bash gen_workload.sh
You must provide your own email list to generate email-key workloads.

### Step 3: Run Workloads
    cd bench
    bash run.sh
Note that `run.sh` only includes several representative runs.
Refer to `bench/workload.cpp`, `bench/workload_multi_thread.cpp`
and `bench/workload_arf.cpp` for more experiment configurations.

## License
    Copyright 2018, Carnegie Mellon University

    Licensed under the [Apache License](https://github.com/efficient/SuRF/blob/master/LICENSE)

---
title: "Systolic Array-based Matrix Multiplier for Neural Networks"
description: "Systolic Array-based Matrix Multiplier for Neural Networks (very in-progress)"
image: "https://upload.wikimedia.org/wikipedia/commons/thumb/3/39/Weights_Stationary_Systolic_Array_Example.png/500px-Weights_Stationary_Systolic_Array_Example.png"
startDate: "2025-12-18"
skills: ["SystemVerilog", "Vivado", "Computer Architecture", "Systolic Arrays", "AXI-Stream","QuestaSim", "Python"]
sourceLink: "https://github.com/dantonklein/Systolic-Array-Matrix-Multiplier-for-Neural-Networks"
---

## About This Project

This project implements a weight-stationary 8x8 systolic array matrix multiplier designed for neural network acceleration. It currently has a complete datapath with a controller for computation, with current plans to implement tiling to allow for any-sized matrix multiplication. It currently supports the INT8 data-type and is written in SystemVerilog.

## Features

### Weight-Stationary Systolic Array Architecture
- 64 processing elements in an 8x8 grid, where the weight matrix (B matrix) remains in the PEs while the activation (A) matrix  flows horizontally and the partial sums flow vertically.
- Utilizes heavy parallelism to achieve the calculation in 15 cycles

### Skew Buffers
- Utilizes two skew buffers: one for the activation matrix input and one for the systolic array output to properly order the data  for interfacing with AXI-Stream buffers

## Verification Methodology

### Testbenches!
- Comprehensive testbenches for all modules to test timing and corner cases

### Golden Models
- Python-generated golden models using Numpy

## In-Progress Improvements and Future Plans

### Tiling
- The most important functionality improvement I'm working on is tiling which allows for any-sized matrix multiplication by splitting it into 8x8 tiles.

- Working on some key optimizations, such as loading columns while computations occur to save 8 cycles for loading. This will require more advanced buffering. This is a necessary improvement for the high data volume of tiling.
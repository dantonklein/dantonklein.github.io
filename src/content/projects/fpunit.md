---
title: "Floating-Point ALU for IEEE-754 Single-Precision Numbers"
description: "SystemVerilog-based design and FPGA implementation of a full-featured pipelined floating-point ALU"
image: "https://media.geeksforgeeks.org/wp-content/uploads/Single-Precision-IEEE-754-Floating-Point-Standard.jpg"
startDate: "2025-09-01"
endDate: "2025-11-30"
skills: ["SystemVerilog", "RTL Design", "IEEE-754", "Constrained-Random Verification", "Static Timing Analysis"]
sourceLink: "https://github.com/dantonklein/Floating-Point-ALU"
---

## Project Overview

This project implements a 32-bit single-precision floating-point Arithmetic Logic Unit compliant with the IEEE 754 standard, written in SystemVerilog and designed for simulation and hardware implementation on FPGA. The ALU supports floating-point addition, subtraction, multiplication, division, square root, comparison, and max/min operations.

## Features

- Arithmetic operations on floating-point values: add, subtract, multiply, divide, square root, comparison, and max/min.
- Exception and edge-case handling(zero, infinity, both types of NaNs, overflow/underflow, rounding)

## Architecture
- Fully pipelined architecture with various optimizations such as carry-lookahead adders(specifically kogge-stone adders), dadda multipliers, and look-up tables with Newton's method to improve performance. 
- Runs at 110 MHz on an Artix-7 FPGA after I completed several iterative timing optimizations
- Design is verified using many constrained-random verification testbenches for the main operations
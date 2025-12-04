---
title: "6 Stage Pipeline RISC-V Cpu"
description: "SystemVerilog-based implementation of a RISC-V CPU core with a 6 stage pipeline and various pipeline optimizations"
image: "https://raw.githubusercontent.com/dantonklein/RISC-V-CPU/refs/heads/master/Danton_RISCV6.png"
startDate: "2025-06-01"
endDate: "2025-10-01"
skills: ["SystemVerilog", "RTL Design", "Computer Architecture", "Static Timing Analysis"]
---

## Description

This project implements a RISC-V CPU with to the RV32I instruction set architecture, using SystemVerilog. It consists of a 6 stage pipeline design with Fetch, Decode, Jumps/Branch Handling, Execution, Memory, and Write-Back stages. It contains data forwarding, hazard detection, and branch prediction. 

## Features

- Full support for the unpriveledged RV32I instruction set
- Implementation of datapath with many submodules for easier verification
- Various pipeline optimizations like data forwarding, hazard detection, and branch prediction to improve IPC
- Various testbenches for submodules in addition to master testbench for top level design

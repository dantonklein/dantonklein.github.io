---
title: "8-Way Set-Associative Cache Design"
description: "8-Way Set-Associative Cache Design in addition to a Fully-Associative and a Direct-Mapped Cache"
image: "https://github.com/dantonklein/Cache-Designs/blob/master/pics/Cache%20Diagram.drawio.png"
startDate: "2025-12-01"
skills: ["SystemVerilog", "Vivado", "Computer Architecture", "QuestaSim"]
sourceLink: "https://github.com/dantonklein/Cache-Designs"
---

## About This Project

This project contains a design of a 8-way set associative cache utilizing a tree-based pseudo-LRU replacement policy. It also features a direct-mapped cache and a fully-associative cache which I designed to learn the topics that I later used in the set associative cache.

## Features

### Tree-Based Pseudo-LRU Replacement Policy
- Utilizes a tree-based pseudo-LRU for an accurate low-area solution for replacement upon cache misses

### Pipelined Cache Hits 
- Allows throughput of 1 read/write per cycle upon repeated cache hits

### Interfacing with real ram
- Cache is byte-addressable and supports byte, halfword, and word reads/writes
- Supports burst reads from the cache with a line buffer to support atomic memory updates



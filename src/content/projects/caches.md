---
title: "Parameterized Cache Designs (In-Progress)"
description: "Parameterized Direct Mapped, Fully Associative, and N-Way Associative Caches in SystemVerilog"
image: "https://api.dicebear.com/9.x/glass/svg?seed=Jocelyn"
startDate: "2025-12-01"
skills: ["SystemVerilog", "Vivado", "Computer Architecture"]
sourceLink: "https://github.com/dantonklein/Cache-Designs"
---

## About This Project

This repository will contain designs for direct-mapped, fully-associative, and n-way associative caches. I've completed the direct-mapped cache and now I am working on the fully-associative cache.

## Features

### Parameterized Design 
- User has option to choose address width, cache size, word offset
- Will support option for the user to decide set amount for N-Way Associative Cache

### Interfacing with real ram
- Cache is byte-addressable and supports byte, halfword, and word reads/writes
- Supports burst reads from the cache with a line buffer to support atomic memory changes



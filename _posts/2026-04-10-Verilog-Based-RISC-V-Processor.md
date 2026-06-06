---
title: "RISC-V Processor in Verilog"
date: 2026-03-20
author: "Arkadeb Manna"
words_per_minute : 100
read_time: true
tags :
    - Verilog
    - RISC-V
    - Project
---

## Project Overview :
* Developed a fully functional 5-stage pipelined RISC-V processor.
* Executed as a Course Project for CS224, Hardware Laboratory (Apr. 2026).
* Codebase and repository: bit.ly/RISCV_Processor

## Introduction
* Implements a custom RISC-V architecture to execute the RV32IMB instruction set.
* Focuses on reducing latency and maximizing instruction throughput.
* Designed, coded, and verified entirely using Verilog HDL.
* Validated through comprehensive testbenches and physical FPGA deployment.

## Key Features
* **5-Stage Pipeline:** Implements the standard stages for optimal instruction execution.
* **Instruction Set:** Full functional support for all RV32IMB instructions.
* **Hardware Accelerator:** Integrated custom accelerator specifically targeting matrix operations.
* **Performance Optimization:** Achieved a 20% latency reduction and performance gain during 4x4 Matrix Multiplication.
* **Performance Matrix:** Extensive analytical comparison between baseline and accelerated instruction execution.
* **Hazard Management:** Custom-built Forwarding Logic and Hazard Detection units to seamlessly resolve data dependencies.
* **FPGA Demonstration:** Real-world hardware validation showcasing all instruction types working natively.

## Real Life Applications
* **Deep Learning & AI:** The hardware-accelerated matrix multiplication directly benefits edge AI computations and neural network inferencing.
* **Embedded Systems:** The efficient 5-stage pipeline architecture is highly applicable for low-power, high-performance embedded IoT controllers.
* **Scientific Computing:** Accelerated matrix operations drastically enhance the execution speed of complex numerical simulations.

## Conclusion
* Successfully realized a robust, pipelined RISC-V processor natively on an FPGA.
* Demonstrated tangible computational improvements using targeted hardware acceleration for matrix math.
* Effectively handled complex pipeline synchronization using custom forwarding and hazard mitigation logic.
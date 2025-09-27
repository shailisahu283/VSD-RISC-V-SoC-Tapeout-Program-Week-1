# VSD-RISC-V-SoC-Tapeout-Program-Week-1


This week focused on the fundamentals of **Verilog RTL design, synthesis, optimizations, and simulation techniques** using open-source tools like **Icarus Verilog (iverilog)**, **GTKWave**, and **Yosys** with **Sky130 PDK**.

---

## 📌 Day 1 – Introduction to Verilog RTL Design and Synthesis

* Learned basics of Verilog RTL design.
* Introduction to **Icarus Verilog (iverilog)** as the simulator.
* Setup of repository structure:

  ```
  lib/                 -> sky130 standard cell libraries  
  my_lib/verilog_models -> standard cell Verilog models  
  verilog_files/        -> lab experiment source files  
  intro_iverilog/       -> example Verilog + testbench files  
  ```
* Example design: **good_mux.v**
* Example testbench: **tb_good_mux.v**
* Command to simulate:

  ```bash
  iverilog good_mux.v tb_good_mux.v
  ./a.out
  ```
* Generate waveform with GTKWave:

  ```bash
  gtkwave tb_good_mux.vcd
  ```
* Introduction to **Yosys** for logic synthesis (RTL → Netlist).

---

## 📌 Day 2 – Timing Libraries, Hierarchical vs Flat Synthesis, and Flop Coding Styles

* Studied **timing .lib files** characterized for PVT (Process, Voltage, Temperature).
* Difference between **Hierarchical** and **Flat synthesis**:

  * Hierarchical → preserves module hierarchy.
  * Flat → flattens into single-level netlist for optimization.
* Learned **sub-module level synthesis** for modular RTL.
* Explored **efficient flop coding styles** (sync vs async reset).
* Labs on synthesizing flops and simple arithmetic operations (mult2, mult9).

---

## 📌 Day 3 – Combinational and Sequential Optimizations

* Introduction to **logic optimizations** for area/power efficiency.
* **Combinational optimization techniques**:

  * Constant propagation
  * Boolean algebra simplification
* **Sequential optimization techniques**:

  * Sequential constant propagation
  * Retiming
  * Sequential logic cloning (floorplan-aware synthesis)
* Labs included optimizing small RTL modules and counters.

---

## 📌 Day 4 – GLS, Blocking vs Non-Blocking, and Simulation-Synthesis Mismatches

* Introduction to **Gate-Level Simulation (GLS)** for verifying synthesized netlists.
* Causes of **synthesis-simulation mismatches**:

  * Missing sensitivity list
  * Blocking (`=`) vs Non-blocking (`<=`) assignments
  * Non-standard coding practices
* Labs on:

  * Ternary operator MUX (correct behavior)
  * Bad MUX (missing sensitivity list issue)
  * Blocking caveat examples showing mismatch

---

## 📌 Day 5 – Optimization in Synthesis

* Focused on **advanced synthesis optimizations**.
* Explored how Yosys performs **logic cleaning, dead code elimination, and resource sharing**.
* Applied optimizations to complex modules for area-efficient netlists.

---

## 🛠 Tools & PDKs Used

* **Icarus Verilog (iverilog)** – simulation
* **GTKWave** – waveform visualization
* **Yosys** – logic synthesis
* **Sky130 PDK** – standard cell libraries

---

✅ **End of Week 1 Deliverables:**

* Basic Verilog design & simulation flow setup
* Netlist generation using Yosys
* Hands-on with timing libraries
* Logic optimizations at both combinational & sequential levels
* GLS for post-synthesis verification



# 5-Stage Pipelined RV32I Processor in SystemVerilog

A self-directed, open-source project designing and verifying a classic 5-stage RISC-V (`RV32I` Base Integer ISA) processor core from scratch using SystemVerilog.

---

## 🎯 Project Goals
- **Architecture:** 5-stage in-order pipeline (`IF`, `ID`, `EX`, `MEM`, `WB`).
- **ISA Scope:** RISC-V 32-bit Integer Base ISA (`RV32I` - 37 instructions).
- **Hazard Handling:** Full bypass/forwarding network and load-use hazard stall unit.
- **Verification:**
  - Dynamic simulation with **Icarus Verilog** and **Verilator**.
  - Waveform analysis using **GTKWave**.
  - Instruction-level co-simulation against **Spike ISS** via SystemVerilog DPI-C.
  - Integration with **Google `riscv-dv`** for randomized instruction generation.

---

## 📂 Repository Structure
```text
my_riscv/
├── rtl/          # Synthesizable SystemVerilog core modules
├── tb/           # Testbenches, monitors, and DPI-C co-sim wrappers
├── sim/          # Simulation scripts, Makefiles, and test runners
├── software/     # RISC-V assembly/C test programs
└── doc/          # Architecture block diagrams and pipeline charts
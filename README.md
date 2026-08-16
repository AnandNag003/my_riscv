# Moola-V (MR5): 5-Stage Pipelined RV32I Processor in SystemVerilog

**Moola-V** (derived from the Kannada word **ಮೂಲ / Moola**, meaning *Root*, *Origin*, or *Foundation*, and abbreviated as **MR5**) is a self-directed open-source hardware project designing and verifying a classic 5-stage RISC-V (`RV32I` Base Integer ISA) processor core from scratch using SystemVerilog.

The name reflects the core objective: building a solid architectural foundation in processor design, hazard handling, and industry-standard verification methodology.

---

## 🎯 Architectural Specifications & Goals
- **Core Name:** Moola-V (MR5 Core)
- **Pipeline Depth:** 5-stage in-order classic pipeline (`IF`, `ID`, `EX`, `MEM`, `WB`).
- **ISA Scope:** RISC-V 32-bit Integer Base ISA (`RV32I` — 37 instructions).
- **Hazard Handling:** Full operand bypass/forwarding network and load-use hazard stall unit.
- **Verification:** 
  - Dynamic simulation with **Icarus Verilog** and **Verilator**.
  - Waveform analysis using **GTKWave**.
  - Instruction-level lock-step co-simulation against **Spike ISS** via SystemVerilog DPI-C.
  - Integration with **Google `riscv-dv`** for randomized instruction generation.

---

## 📂 Repository Structure
```text
my_riscv/
├── rtl/          # Synthesizable SystemVerilog core modules (Moola-V RTL)
├── tb/           # Testbenches, monitors, and DPI-C co-sim wrappers
├── sim/          # Simulation scripts, Makefiles, and test runners
├── software/     # RISC-V assembly/C test programs
└── doc/          # Architecture block diagrams and pipeline charts
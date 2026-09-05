# Gowtham Kumar Maruthi

2026 graduate — M.S. Electrical & Computer Engineering, Virginia Commonwealth University.

Building a portfolio for entry-level RTL design and ASIC verification roles, with a focus on reproducible tests, clock-domain crossings, and clearly scoped formal verification. Expanding toward FPGA implementation and static timing analysis.

## Engineering work

### [Dual-clock asynchronous FIFO](https://github.com/gowthamaruthi/async-fifo-formal-sv)

Parameterized SystemVerilog FIFO with Gray-coded pointers and two-stage synchronization. The current default branch has a passing [compile/simulation baseline](https://github.com/gowthamaruthi/async-fifo-formal-sv/actions/runs/28349549532).

**Pending review:** [FIFO verification repair — PR #2](https://github.com/gowthamaruthi/async-fifo-formal-sv/pull/2) defines the reset/acceptance contract, fixes reset-time memory writes, adds concurrent simulation and negative tests, and separates local induction proofs from bounded data-safety checks. These changes are not yet merged.

| Demonstrated in the review branch | Supporting evidence |
|---|---|
| RTL and CDC reasoning | [Interface contract and implementation guidance](https://github.com/gowthamaruthi/async-fifo-formal-sv/blob/engineering/fifo-verification-contract/README.md) |
| Self-checking SystemVerilog verification | [Concurrent stimulus and transaction scoreboard](https://github.com/gowthamaruthi/async-fifo-formal-sv/blob/engineering/fifo-verification-contract/tb/tb_async_fifo.sv) |
| Formal verification with Yosys/SBY/Z3 | [Harness and task configuration](https://github.com/gowthamaruthi/async-fifo-formal-sv/tree/engineering/fifo-verification-contract/formal) — local induction, 22-step bounded data checks and reachable covers |
| Reproducible checks and failure detection | [Recorded results and source fingerprints](https://github.com/gowthamaruthi/async-fifo-formal-sv/tree/engineering/fifo-verification-contract/docs/results) |

The evidence is from digital simulation, formal checks and generic synthesis. Target-device timing closure and hardware measurements are future milestones.

## Development direction

Next: a small AXI4-Stream subsystem across clock domains with AXI4-Lite control/status, followed by processor verification and a constrained implementation/STA study. Projects will be linked when their source and reproducible results are ready for review.

## Contact

[Email](mailto:gowthamkumarmaruthi@gmail.com) · [LinkedIn](https://www.linkedin.com/in/gowthamkumar-maruthi-323020258)

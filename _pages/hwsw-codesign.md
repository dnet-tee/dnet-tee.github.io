---
layout: splash
title: Processor extensions for security
permalink: /hw-sw-co-design/
classes: wide
---

<div class="feature__item--center">
   <div class="archive__item">
    <h1>Processor extensions for extensions</h1>       
    <p>
      Short teaser text for applications<br >
    </p>
    
  </div>
</div>

## Processor extensions for security

The implementation of software security objectives can benefit substantially from
hardware support. Processors commonly implement instructions or extensions specifically
designed to support security. For instance, to implement isolation between processes, 
system software can rely on processor support for virtual memory. Or protection against
buffer overflow attacks can be made more efficient thanks to dedicated instructions for
bounds checking.

The research community has investigated a wide variety of such extensions, including
support for taint tracking, fast encryption, countermeasures for memory corruption
attacks, trusted computing, and so forth.

With the recent success of the open-source instruction set architecture RISC-V, it
becomes a realistic option to build custom processors that include security extensions
tailored for specific use-cases or applications.

In our research group, we are working on a RISC-V processor framework to support
security research. Unlike many other open source RISC-V implementations, this
processor is not designed with any efficiency criteria in mind. Instead, the
goal of the design is to allow for easy experimentation with processor
extensions and adaptations. To this end, the framework is implemented using
[SpinalHDL](https://github.com/SpinalHDL), a Scala-based HDL that allows to
create interesting hardware abstraction in a high-level programming language.
The processor framework itself is built around the concept of plugins: new logic
can be added simply by implementing a plugin without having to touch any other
implementation files.

Currently, this framework implements the following features:
- RV32I(M)
- Fully bypassed classic 5-stage RISC pipeline that is highly configurable:
  - Can be completely disabled (i.e., 5 CPI);
  - Easy to add and combine stages;
  - Bypassing could be replaced with stalling;
  - ...
- Supports instructions that take more than one cycle in a stage:
  - For example, the M-extension (MUL/DIV/REM);
  - Blocking memory accesses.
- Machine-Level ISA (CSRs, traps);
- SoC:
  - Integration with AXI4 and APB buses;
  - Simple peripherals (Machine Timer, UART,...).
- Tested using [riscv-tests](https://github.com/riscv/riscv-tests) and formally
  verified using [riscv-formal](https://github.com/SymbioticEDA/riscv-formal).

Some examples of extensions that we plan to implement and evaluate include:

 - Support for capability based security, see for instance the following papers:
    * CHERI
    * **TODO**

 - Extensions that enable the implementation of countermeasures against micro-architectural attacks, see for instance the following papers:
    * Spectre
    * Context



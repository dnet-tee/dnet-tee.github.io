---
layout: single
title: Processor extensions for security
permalink: /hw-sw-co-design/
---

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

In our research group, we are working on a RISC-V processor framework specifically
designed to support extensibility for security purposes.

**TODO**: brief description of the framework and its current status

Some examples of extensions that we plan to implement and evaluate include:

 - Support for capability based security, see for instance the following papers:
    * CHERI
    * **TODO**

 - Extensions that enable the implementation of countermeasures against micro-architectural attacks, see for instance the following papers:
    * Spectre
    * Context



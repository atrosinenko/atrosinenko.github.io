---
layout: default
---

_Finding some interesting technologies, testing, extending and [blogging about](https://habr.com/ru/users/atrosinenko/posts/) (in Russian)._

Areas of interests:
* [Fuzzing](#fuzzing)
  * [Instrumentation](#instrumentation)
* [Chisel HDL](#chisel-hdl)
* [IDEs / Tooling](#ides-and-tooling)
* [Executable jokes](#executable-jokes)
* [Misc](#misc)

## Fuzzing

Fuzzing is a software testing technic involving feeding the software under test with quasi-random data.

* [kBdysch](https://github.com/atrosinenko/kbdysch) -- a collection of user-space Linux kernel specific guided fuzzers based on [LKL](https://github.com/lkl/linux)

## Instrumentation

* [bpfinst-spec](https://github.com/atrosinenko/bpfinst-spec) / [docs](https://atrosinenko.github.io/bpfinst-spec) -- generic eBPF-based interface for implementing not-too-complex per-instruction instrumentations trivialy. You just write "pseudocode" in C with properly named functions, then compile it into eBPF object file... and that pseudo-pseudocode is inserted before every corresponding instruction in an efficient manner. These functions can process corresponding instructions operands, and get/set associated 64-bit-wide tags
  * [QInst](https://github.com/atrosinenko/qinst) -- a QEMU-based dynamic instrumentation engine. Able to instrument user-space processes on Linux host (via traditional `qemu-user-*` emulators). Technically, should be almost ready for full-system instrumentation
  * [SimpleInst](https://github.com/atrosinenko/simpleinst) -- a proof-of-concept instrumenter built into particular instance of [RocketChip](https://github.com/chipsalliance/rocket-chip) soft-processor at the time of Verilog code generation (not yet supports tags)
  * [LLInst](https://github.com/atrosinenko/llinst) -- a static white-box instrumentation engine implemented as an LLVM pass

## Chisel HDL

Chisel is a hardware description language embedded into Scala as a DSL. It makes it possible to write some hardware description in Scala with rich Scala IDE support for navigating, refactoring, etc. in a much FPGA vendor-agnostic way. Then just compile & run to produce Verilog source to be fed to vendor-dependent tool.

* [SimpleInst](https://github.com/atrosinenko/simpleinst) -- RoCC accelerator implementation that is able to turn simple functions from eBPF object files into CPU instructions
* Patched RocketChip implementation to be used with SimpleInst that invokes RoCC accelerator instructions as a bpfinst instrumenters

## IDEs and tooling

* Sent numerous patches to [OpenModelica](https://github.com/OpenModelica/)
  * implemented context-aware code completion in OMEdit by bridging the gap between pre-existing rudimentary snippet suggester and pre-existing link to OMC backend
* PMD
  * implementation of language module for Modelica
  * [Source Code Minimizer](https://github.com/pmd/pmd-scm) utility that reuses existing (full PMD, not CPD) language support to minimize a source code file preserving some invariant

## Executable jokes

[QEMU.js](https://github.com/atrosinenko/qemujs) (WIP) -- a proof-of-concept port of QEMU to web browser featuring machine-code-to-WASM JIT compiler

## Misc

* [afl-dr](https://github.com/atrosinenko/afl-dr) -- implementation of specific AFL-like instrumentation with [DynamoRIO](http://dynamorio.org/), not a bpfinst instrumenter
* [Analog video signal generator](https://github.com/atrosinenko/composite-video-generator) in Chisel -- video signal generator (works only for B/W) for [Marsohod2](https://marsohod.org/howtostart/marsohod2) FPGA board... and rudimentary oscilloscope for self-debugging :)

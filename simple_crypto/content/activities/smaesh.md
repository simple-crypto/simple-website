---
title: SMAesH
---

**SMAesH** is a hardware implementation of the AES block cipher that uses
masking as a countermeasure against side-channel attacks.
More precisely, we use the Hardware Private Circuits (HPC) masking scheme, which
provides state-of-the-art guarantees in terms of resistance against physical
defaults (i.e., glitches and transitions) and composability.

The SMAesH implementation package is a generic HDL code (Verilog) that
describes a hardware implementation of the AES protected with arbitrary number
of shares.

Scientific publications introduce [HPC](https://eprint.iacr.org/2020/185) and
its [application to the AES](https://eprint.iacr.org/2022/252).

Current status:
- AES 128-bit encryption implemented
- FPGA-validated
- [Lifetime stage](/about/organization#lifetime): Public evaluation
- An [Evaluation challenge](https://smaesh-challenge.simple-crypto.org/) with a side-channel dataset was organized for [CHES2023](https://ches.iacr.org/2023/challenge.php).

Get the
- [Source code](https://github.com/simple-crypto/SMAesH)
- [Technical documentation](/pdfs/SMAesH_documentation.pdf)
- [Preliminary evaluation report](/pdfs/SMAesH_preliminary_eval.pdf)

**Releases**:

- [v1.0.0](https://github.com/simple-crypto/SMAesH/releases/tag/v1.0.0) (Jun 15, 2023)
- [v1.0.1](https://github.com/simple-crypto/SMAesH/releases/tag/v1.0.1) (Apr 28, 2023)
- [v1.1.0](https://github.com/simple-crypto/SMAesH/releases/tag/v1.1.0) (Sep 02, 2024)

---
title: Activities
---

## Open-source codes

SIMPLE-Crypto develops and maintains open-source projects related to secure
implementations of cryptographic algorithms in embedded systems.

* [**SMAesH**](/projects/smaesh) A hardware implementation of the AES block cipher with masking as a countermeasure against side-channel attacks.
* [**SCALib**](/projects/scalib) SIMPLE's Side-Channel evaluation library.
* *More to come!* 

## Trainings

*(In devlopment.)*

The SIMPLE-Crypto Association will organize both general and specialized trainings in order to help
designers integrating our open source solutions in their products.

**Side-channel analysis and leakage-resistance.** This yearly training
covers the foundations of side-channel analysis, countermeasures and leakage-resistance.
Its focus is on understanding the general principles behind the attacks
and solutions to prevent them. The training is combined with hands on sessions 
based on toy implementations of standard algorithms.

**Using SCALib to evaluate the SIMPLE-Crypto implementations** This more specialized 
training is aimed at designers willing to integrate side-channel resistant
SIMPLE-Crypto implementations in their products. Since such integration may modify the leakage behavior
of our stand-alone codes, the training aims at helping designers re-assessing our implementations
after integration.



<!--
* <strong><em>LR-BC.</em></strong> Leakage-resistant modes of operation are aimed to 
offer security against side-channel analysis while limiting the need of implementation-level
countermeasures. LR-BC is an example of such modes that
leverages the AES co-processor that many 32-bit microcontrollers currently embed.
It limits the number of side-channel traces that an adversary can observe both during
initialization/finalization (thanks to a leakage-resilient PRF) and during the bulk
computation (thanks to a leakage-resilient PRG). The publication on which this design
relies is available [here](https://tches.iacr.org/index.php/TCHES/article/view/8988/){:target="_blank"}.
-->

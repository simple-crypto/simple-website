---
layout: default
title: Outputs
---
# {{ page.title }}

The main outputs of the SIMPLE-Crypto Association are:
* [Code projects](#codes), 
* [Evaluation tools](#tools),
* [Trainings](#trainings).

**<a name="codes">Code projects</a>**

For each code project, we give a succint summary, a link to academic publications whenever possible
and the page hosting the code with documentation and data sets when moving to
the public evaluation stage.

**Under development**

* <strong><em>AES-HPC.</em></strong> Hardware Private Circuits (HPC) are a generic technique 
to protect cryptographic implementations against side-channel attacks thanks to masking (aka secret sharing).
It provides state-of-the-art guarantees in terms of resistance against physical defaults
(e.g., glitches) and composability. The AES-HPC implementation package is a generic HDL
code that describes a hardware implementation of the AES protected with arbitrary number of shares.
The publications introducing HPC and its application to the AES
are available [here](https://eprint.iacr.org/2020/185){:target="_blank"}
and [here](https://eprint.iacr.org/2022/252){:target="_blank"}

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


**<a name="tools">Evaluation tools</a>**

<strong><em>SCALib</em></strong>, the Side-Channel Analysis Library,
is a Python package that contains state-of-the-art tools for side-channel security evaluations. 
It focuses on providing efficient implementations of analysis methods widely used by the 
side-channel research community and maintaining a simple and flexible interface. The library
is used as a first tool to assess the security of our open source implementations.
Installation details and code are available [here](https://scalib.readthedocs.io/){:target="_blank"}.


**<a name="trainings">Trainings</a>**

The SIMPLE-Crypto Association organizes both general and specialized trainings in order to help
designers integrating our open source solutions in their products.

* <strong><em>Side-channel analysis and leakage-resistance</em></strong>. This yearly training
covers the foundations of side-channel analysis, countermeasures and leakage-resistance.
Its focus is on understanding the general principles behind the attacks
and solutions to prevent them. The training is combined with hands on sessions 
based on toy implementations of standard algorithms.

* <strong><em>Using SCALib to evaluate the SIMPLE-Crypto implementations</em></strong>. This more specialized 
training is aimed at designers willing to integrate side-channel resistant
SIMPLE-Crypto implementations in their products. Since such integration may modify the leakage behavior
of our stand-alone codes, the training aims at helping designers re-assessing our implementations
after integration.
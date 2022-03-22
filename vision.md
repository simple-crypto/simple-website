---
layout: default
title: 'Vision'
---
# {{ page.title }}

**The case of cryptographic algorithms**

One of the founding bases of modern cryptography is [Kerckhoff’s principles](https://en.wikipedia.org/wiki/Kerckhoffs_principle){:target="_blank"}: 
a cryptosystem should be secure even if everything about the system, except the key, 
is public knowledge. This concept can be opposed to so-called “security by obscurity”, 
which rather relies on the secrecy of the algorithms and protocols used
in an information system.

Since the early 1980s, Kerckhoff’s principles have been successfully
applied in the design of many cryptographic schemes. Research progresses have demonstrated that 
open designs can lead to secure solutions thanks to the large amount of scrutiny
that their public nature enables.
At a high level, and taking the case of symmetric encryption for illustration, 
this possibility to rely on open designs has been driven by three main ingredients.
First, cryptanalysis results against (reverse engineered) closed source algorithms
have recurrently shown that they rarely reach the level of security that open 
solutions relying on long-term public audits can reach (see for example the cases of
[Crypto-1](https://en.wikipedia.org/wiki/Crypto-1){:target="_blank"}, [COMP128](https://en.wikipedia.org/wiki/COMP128){:target="_blank"} 
or [Keeloq](https://en.wikipedia.org/wiki/KeeLoq){:target="_blank"}).
Next, new design ideas have been introduced in order to prevent such cryptanalysis results (as for example
surveyed in [\[KR11\]](#KR11) for block ciphers). Finally, 
formal definitions and reductions to well analyzed mathematical assumptions have increased the 
understanding and confidence in modern encryption schemes [\[KL14\]](#KL14). As a result, in a vast 
majority of the cases, the recommended practice nowadays is to use open and standardized 
primitives together with provably secure modes of operation rather than closed source ones. 

**From algorithms to implementations**

Research progresses have been an enabling factor for the development and deployment of open cryptographic 
algorithms and protocols. As a result, open source implementations have also become standard for 
different cryptographic functionalities: see for example the [OpenSSL](https://en.wikipedia.org/wiki/OpenSSL){:target="_blank"} 
and [NaCl](https://en.wikipedia.org/wiki/NaCl_(software)){:target="_blank"} libraries.
Yet, and despite these progresses, open source implementations of more advanced functionalities
or ensuring advanced security features are not yet systematically available.
One example of such advanced features is embedded security against physical attacks. 
In their seminal work on Differential Power Analysis, Kocher at al. showed that, without special care, cryptographic implementations 
leak "side-channel information" that can be easily exploited to recover the key material of 
cryptographic algorithms [\[KJJ99\]](#KJJ99). Boneh et al. showed that a similar issue occurs 
if faults can be injected during the execution of the algorithms [\[BDL97\]](#BDL97). 

In view of the limited (theoretical and practical) understanding of these new physical attack 
vectors, the first implementations to counteract them have been developed by the industry in a 
mostly closed source setting. This situation is reflected by evaluation practices 
for which requiring implementation details may increase the "perceived complexity" of an
attack (e.g., as rated by the [Common Criteria](https://www.commoncriteriaportal.org/){:target="_blank"} framework) 
and therefore (somewhat artificially) increase its certification 
level [\[L16\]](/pdfs/Lomne_16.pdf){:target="_blank"}.
While these approaches were necessary first steps towards solving
the embedded security challenge, <strong><em>our vision is that as research advances, the security 
by obscurity paradigm becomes less justified and its benefits are outweighted by its drawbacks</em></strong>. 
That is, while a closed source approach can limit the adversary's understanding of the target
implementations as long as their specifications remain opaque, it also limits the public
understanding of the mechanims on which security relies, and therefore the possibility to optimize them.
By contrast, an open approach to security can lead to a better evaluation of the worst-case
security level that is targeted by cryptographic designs.

**Goals and interest of an open implementation approach**

We envision the main goals and the interest of the SIMPLE-Crypto Association as follows:

* <strong><em>Improving the long-term security of cryptographic implementations</em></strong>. The rationale 
supporting our vision is that over time, the continuous and  public worst-case evaluation process that the SIMPLE-Crypto
Association leverages will lead to better confidence in the security of its open 
solutions than more time-constrained developments.

* <strong><em>Developing and preserving the integrity of open source security technologies</em></strong>. For this purpose, we 
provide an infrastructure for open source cryptographic hardware and software 
developments and maintain a team of expert developers with minimum operational cost.

* <strong><em>Encouraging public audits</em></strong>. Following an established practice in cryptography and
security research, we aim to combine all the solutions we implement with challenges based on public data sets and to reward the 
possible detection of security flaws in our designs with bug bounties. We will also make all our security analysis
tools available under open source licenses.

* <strong><em>Complementing the industrial ecosystem</em></strong>. As a non-profit organisation, 
the SIMPLE-Crypto Association does not aim to compete with established industrial actors. 
We rather see the development and evaluation of cryptographic implementations as becoming 
so specialized and expensive that pooling a part of its development in a joint effort is justified.
We envision this complementarity for designs (as it was in the past for cryptographic algorithms, 
but with more need of continuous development) and for evaluations (since our longer-term efforts
do not cancel the need of third-party evaluation and certification when integrating open source
solutions in complex systems).

* <strong><em>Amplifying standardization efforts</em></strong>. Standardized algorithms
and evaluation methodologies are essential ingredients towards systematizing research advances into technological
building blocks that can be leveraged in real-world applications. Yet, it generally aims at some
genericity that we hope to enrich by maintaining implementations and, in the case of
algorithms with embedded security guarantees, public evaluations and data sets on relevant
technologies.

* <strong><em>Performing applied research on cryptographic implementations</em></strong>. The primary focus of our developments
being on solutions with strong implementation security guarantees, the association aims to follow theoretical
advances in the field and to contribute to their prototyping, in order to make these advances more readily
exploitable by industrial actors.

* <strong><em>Identifying practically-relevant targets for constructive research.</em></strong>
Research in cryptography and security is driven by both theoretical advances and concrete case studies.
In application fields where implementations are closed source,
identifying good case studies may require expensive reverse engineering efforts that are 
of limited scientific interest. It may also lead to the discovery of bugs in deployed products,
leading to complex responsible disclosure issues. By identifying practically-relevent
targets for testing new attacks, the SIMPLE-Crypto Association aims at serving as a
constructive interface between academic and industrial research.


**References**

<font size="3">
<a name="BDL97">[BDL97]</a> Dan Boneh, Richard A. DeMillo, Richard J. Lipton: <em>On the Importance of Checking Cryptographic Protocols for Faults</em>. EUROCRYPT 1997: 37-51.<br>
<a name="KL14">[KL14]</a> Jonathan Katz, Yehuda Lindell: <em>Introduction to Modern Cryptography</em>. CRC Press 2014.<br>
<a name="KR11">[KR11]</a> Lars R. Knudsen, Matthew Robshaw: <em>The Block Cipher Companion</em>. Information Security and Cryptography, Springer 2011.<br>
<a name="KJJ99">[KJJ99]</a> Paul C. Kocher, Joshua Jaffe, Benjamin Jun: <em>Differential Power Analysis</em>. CRYPTO 1999: 388-397.
</font>

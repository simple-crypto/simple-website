# Vision: transparency as a measure of maturity

**The case of cryptographic algorithms**

One of the founding bases of modern cryptography is [Kerckhoff’s principles](https://en.wikipedia.org/wiki/Kerckhoffs_principle){:target="_blank"}: 
a cryptosystem should be secure even if everything about the system, except the key, 
is public knowledge. This concept can be opposed to so-called “security by obscurity”, 
which rather relies on the secrecy of both the algorithms and implementations used
in an information system.

Since the early 1980s, Kerckhoff’s principles have been successfully
applied in the design of many cryptographic algorithms. Research progresses have demonstrated that 
open designs can lead to secure solutions thanks to the large amount of scrutiny
that their public nature enables.
As illustrated in the left part of the following figure for the case of symmetric encryption, 
this possibility to rely on open designs has been driven by three main ingredients.

<br/>
![transparency](/figures/transparency.png)
<br/>

First, cryptanalysis results against (reverse engineered) closed source algorithms
have recurrently shown that they rarely reach the level of security that open 
solutions relying on long-term public audits can reach (see for example the cases of
[Crypto-1](https://en.wikipedia.org/wiki/Crypto-1){:target="_blank"}, [COMP128](https://en.wikipedia.org/wiki/COMP128){:target="_blank"} 
or [Keeloq](https://en.wikipedia.org/wiki/KeeLoq){:target="_blank"}).
Next, new design
ideas have been introduced in order to prevent such cryptanalysis results (as for example
surveyed in [\[KR11\]](#KR11) for block ciphers). Finally, 
formal definitions and reductions to well analyzed mathematical assumptions have increased the 
understanding and confidence in modern encryption schemes (see for example
[\[B+97\]](#B+97) for the case of symmetric encryption). As a result, in a vast 
majority of the cases, the recommended practice in 2020 is to use open and standardized 
primitives together with provably secure modes of operation rather than closed-source ones. 

**From algorithms to implementations**

Research progresses have been an enabling factor for the development and deployment of open cryptographic 
algorithms. Yet, these progresses also encountered new challenges with the first public 
reports of physical attacks in the late 1990s. For example, in their seminal work on Differential Power 
Analysis, Kocher at al. showed that, without special care, cryptographic implementations 
leak "side-channel information" that can be easily exploited to recover the key material of 
cryptographic algorithms [\[KJJ99\]](#KJJ99). Boneh et al. showed that a similar issue occurs 
if faults can be injected during the execution of the algorithms [\[BDL97\]](#BDL97). 

In view of the limited (theoretical and practical) understanding of these new physical attack 
vectors, the first implementations to counteract them have been developed by the industry in a 
mostly closed source setting. This is for example reflected by current evaluation practice 
for which requiring implementation details may increase the "perceived complexity" of an
attack (e.g., as rated by the [Common Criteria](https://www.commoncriteriaportal.org/){:target="_blank"} framework) 
and therefore decrease its certification 
level [\[L16\]](/pdfs/Lomne_16.pdf){:target="_blank"}.
While these approaches were necessary first steps towards solving
the embedded security challenge, <strong><em>our vision is that as research advances, the security 
by obscurity paradigm becomes less justified and its benefits are outweighted by its drawbacks</em></strong>. 
That is, while a closed source approach can limit the adversary's understanding of the target
implementations as long as their specifications remain opaque, it also limits the public
understanding of the mechanims on which security relies, and therefore the possibility to optimize them.
As for cryptographic algorithms, and as illustrated in the right part of the previous figure for 
the case of side-channel attacks, the increased relevance of open solutions for cryptographic
implementations is driven by three main ingredients. 

First, cryptanalysis results against unprotected implementations are now well documented and 
can be used to assess security in a close to worst-case manner (see for example [\[BS20\]](#BS20) for a
recent discussion of the relevance of open source designs for this purpose). 
Next, many countermeasures
have been introduced, working at different abstraction levels (see for example
[\[C+99\]](#C+99) and [\[DFS19\]](#DFS19) for one of the first papers on the masking countermeasure and a more recent discussion). 
Finally, sound definitions
enabling reductions towards physical assumptions that can be falsified by evaluation 
laboratories start to be available (see [\[DP08\]](#DP08) and [\[B+20\]](#B+20) for one of the first papers on leakage-resilience
and a more recent discussion). We also refer to the following [invited talk](https://www.youtube.com/watch?v=KdhrsuJT1sE){:target="_blank"}
for a general overview.

**Goals and interest of an open implementation approach**

We envision the main goals and the interest of the SIMPLE-Crypto Association as follows:

* <strong><em>Preserving the integrity of open source security technologies</em></strong>. For this purpose, we 
aim to provide an infrastructure for open source cryptographic hardware and software 
developments and to maintain a team of expert developers with minimum operational cost.

* <strong><em>Improving the long-term security of cryptographic implementations</em></strong>. Our rationale 
for this purpose is that over time, the continuous and public evaluation process that the SIMPLE-Crypto
Association leverages will lead to better confidence in the security of its open 
solutions than more time-constrained certifications.

* <strong><em>Encouraging public audits</em></strong>. Following an established practice in cryptography and
security research, we aim to complement all the solutions we implement with challenges and to reward the 
possible detection of security flaws in our designs with bug bounties.

* <strong><em>Complementing the industrial ecosystem</em></strong>. As a non-profit organisation, 
the SIMPLE-Crypto association does not aim to compete with established industrial actors. 
We rather see the development of secure cryptographic implementations as becoming 
so specialized that amortizing a part of its development efforts becomes justified, 
as it was in the past for cryptographic algorithms, but with more need of continuous 
development.  

**References**

<font size="3">
<a name="B+97">[B+97]</a> Mihir Bellare, Anand Desai, E. Jokipii, Phillip Rogaway: <em>A Concrete Security Treatment of Symmetric Encryption</em>. FOCS 1997: 394-403.<br>
<a name="B+20">[B+20]</a> Davide Bellizia, Olivier Bronchain, Gaëtan Cassiers, Vincent Grosso, Chun Guo, Charles Momin, 
Olivier Pereira, Thomas Peters, François-Xavier Standaert:
<em>Mode-Level vs. Implementation-Level Physical Security in Symmetric Cryptography - A Practical Guide Through the Leakage-Resistance Jungle</em>. 
CRYPTO (1) 2020: 369-400.<br>
<a name="BDL97">[BDL97]</a> Dan Boneh, Richard A. DeMillo, Richard J. Lipton: <em>On the Importance of Checking Cryptographic Protocols for Faults</em>. EUROCRYPT 1997: 37-51.<br>
<a name="BS20">[BS20]</a> Olivier Bronchain, François-Xavier Standaert: <em>Side-Channel Countermeasures' Dissection and the Limits 
of Closed Source Security Evaluations</em>. IACR Trans. Cryptogr. Hardw. Embed. Syst. 2020(2): 1-25 (2020).<br>
<a name="C+99">[C+99]</a> Suresh Chari, Charanjit S. Jutla, Josyula R. Rao, Pankaj Rohatgi:
<em>Towards Sound Approaches to Counteract Power-Analysis Attacks</em>. CRYPTO 1999: 398-412.<br>
<a name="DFS19">[DFS19]</a> Alexandre Duc, Sebastian Faust, François-Xavier Standaert:
<em>Making Masking Security Proofs Concrete (Or How to Evaluate the Security of Any Leaking Device)</em>. J. Cryptology 32(4): 1263-1297 (2019).<br>
<a name="DP08">[DP08]</a> Stefan Dziembowski, Krzysztof Pietrzak: <em>Leakage-Resilient Cryptography</em>. FOCS 2008: 293-302.<br>
<a name="KR11">[KR11]</a> Lars R. Knudsen, Matthew Robshaw: <em>The Block Cipher Companion</em>. Information Security and Cryptography, Springer 2011.<br>
<a name="KJJ99">[KJJ99]</a> Paul C. Kocher, Joshua Jaffe, Benjamin Jun: <em>Differential Power Analysis</em>. CRYPTO 1999: 388-397.
</font>
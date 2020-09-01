# Transparency as a measure of maturity

**The case of cryptographic algorithms**

One of the founding bases of modern cryptography is [Kerckhoff’s principles](https://en.wikipedia.org/wiki/Kerckhoffs_principle): 
a cryptosystem should be secure even if everything about the system, except the key, 
is public knowledge. This concept can be opposed to so-called “security by obscurity”, 
which rather relies on the secrecy of both the algorithms and implementations used
in a security system.

Since the early 1990s, Kerckhoff’s principles have been successfully
applied in the design of many cryptographic algorithms. Research progresses have demonstrated that 
open designs can lead to secure solutions based on sound mathematical principles. 
As illustrated in the left part of the following figure for the case of symmetric encryption, 
this possibility to rely on open designs has been driven by three main ingredients.

<br/>
![transparency](/figures/transparency.png)
<br/>

First, cryptanalysis results against (reverse engineered) closed source algorithms
have recurrently shown that they rarely reach the level of security that open 
solutions relying on long-term public audits can reach (see for example the cases of
[Crypto-1](https://en.wikipedia.org/wiki/Crypto-1), [COMP128](https://en.wikipedia.org/wiki/COMP128) 
or [Keeloq](https://en.wikipedia.org/wiki/KeeLoq)).
Next, new designs 
ideas have been introduced in order to prevent such cryptanalysis results (as for example
surveyed in [\[KR11\]](#KR11) for block ciphers). Finally, 
formal definitions and reductions to well understood assumptions have increased the 
understanding and confidence in modern encryption schemes (see for example
[\[B+97\]](#B+97) for the case of symmetric encryption). As a result, in a vast 
majority of the use cases, the standard practice in 2020 is to use open standardized 
algorithms and modes of operation rather than closed-source ones. 

<font size="3">
<a name="BR97">[B+97]</a> Mihir Bellare, Anand Desai, E. Jokipii, Phillip Rogaway:_A Concrete Security Treatment of Symmetric Encryption_. FOCS 1997: 394-403.<br>
<a name="KR11">[KR11]</a> Lars R. Knudsen, Matthew Robshaw:_The Block Cipher Companion_. Information Security and Cryptography, Springer 2011.
</font>

**From algorithms to implementations**

Research progresses have been an enabling factor for the development and deployment of open cryptographic 
algorithms. Yet, these progresses also encountered new challenges with the first public 
reports of physical attacks in the late 1990s. In his seminal work on Differential Power 
Analysis, Kocher at al. showed that without special care, cryptographic implementations 
leak "side-channel information" that can be easily exploited to recover the key material of 
cryptographic algorithms [\[KJJ99\]](#KJJ99). Boneh et al. showed that a similar issue occurs 
if faults can be injected during the execution of the algorithms [\[BDL97\]](#BDL97). 

In view of the limited (theoretical and practical) understanding of these new physical attack 
vectors, the first implementations to counteract them have been developed by the industry in a 
mostly closed source setting [?]. While these solutions were necessary first steps towards solving
the embedded security challenge, our vision is that as research advances, the security 
by obscurity paradigm becomes less justified and its benefits are outweighted by its drawbacks. 
As for the case of cryptographic algorithms, and as illustrated in the right part of the previous figure for 
the case of side-channel attacks, the increased relevance of open solutions for cryptographic
implementations is driven by three main ingredients. 

First, cryptanalysis results against unprotected implementations are now well documented and 
can be used to assess security in a close to worst-case manner [?]. Next, many countermeasures
have been introduced, working at different abstraction levels [?]. Finally, sound definitional 
framework enabling reductions towards physical assumptions that can be falsified by evaluation 
laboratories start to be available [?].

<font size="3">
<a name="KJJ99">[KJJ99]</a> Paul C. Kocher, Joshua Jaffe, Benjamin Jun:_Differential Power Analysis_. CRYPTO 1999: 388-397.<br>
<a name="BDL97">[BDL97]</a> Dan Boneh, Richard A. DeMillo, Richard J. Lipton:_On the Importance of Checking Cryptographic Protocols for Faults (Extended Abstract)_. EUROCRYPT 1997: 37-51.
</font>

**Goals and intererst of an open implementation approach**

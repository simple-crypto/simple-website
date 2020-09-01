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
surveyed in '[KR11]' for block ciphers). Finally, 
formal definitions and reductions to well understood assumptions have increased the 
understanding and confidence in modern encryption schemes [?]. As a result, in a vast 
majority of the use cases, the standard practice in 2020 is to use open standardized 
algorithms and modes of operation rather than closed-source ones. 

[KR11] Lars R. Knudsen, Matthew Robshaw: _The Block Cipher Companion_. Information Security and Cryptography, Springer 2011.

**From algorithms to implementations**



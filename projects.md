# Projects

The SIMPLE-Crypto Association is currently working on different code projects described below.
For each project, we give a succing summary, a link to academic publications whenever possible
and a link to the page hosting the code with documentation and data sets when moving to
the public evaluation stage.

**Under development**

* <strong><em>LR-BC.</em></strong> Leakage-resistant modes of operation are aimed to 
offer security against side-channel analysis while limiting the need of implementation-level
countermeasures. LR-BC is an example of such modes that
leverages the AES co-processor that many 32-bit microcontrollers currently embed.
It limits the number of side-channel traces that an adversary can observe both during
initialization/finalization (thanks to a leakage-resilient PRF) and during the bulk
computation (thanks to a leakage-resilient PRG). The publication on which this design
relies is available [here](https://tches.iacr.org/index.php/TCHES/article/view/8988/){:target="_blank"}.

* <strong><em>AES-HPC.</em></strong> Hardware Private Circuits (HPC) are a generic technique 
to protect cryptographic implementations against side-channel attacks thanks to masking (aka secret sharing).
It provides state-of-the-art guarantees in terms of resistance against physical defaults
(e.g., glitches) and composability. The AES-HPC implementation package is a generic HDL
code that describes a hardware implementation of the AES protected with arbitrary number of shares.
The publication introducing HPC is is available [here](https://eprint.iacr.org/2020/185){:target="_blank"}.


**Under public evaluation**

* <strong><em>SCALib</em></strong>, the Side-Channel Analysis Library,
is a Python package that contains state-of-the-art tools for side-channel security evaluations. 
It focuses on providing efficient implementations of analysis methods widely used by the 
side-channel research community and maintaining a simple and flexible interface. The library
is used as a first tool to assess the security of our open source implementations.
Installation details and code are available [here](https://scalib.readthedocs.io/){:target="_blank"}.

_A note on patents._ The SIMPLE-Crypto Association does not fill patents.
Our developments are all based on peer-reviewed published solutions and are either free of patents 
or should become free of patents in the long term. In the mid term, code projects are
provided “as is”, without warranty of any kind, express or implied, including but not limited to 
the warranties of merchantability, fitness for a particular purpose and noninfringement. 

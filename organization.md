# Organization 

The SIMPLE-Crypto Association is based on a flexible model with minimum 
overheads. It is aimed to enable the integration and maintenance of code projects from 
different partners. At high level, we
start funding researchers (possibly co-affiliated with 
other research institutes or universities) to evaluate and maintain the
codes once our scientific council expressed sufficient interest and we
collected sufficient sponsoring. Details about the yearly schedule of the association,
the lifetime of its projects and its licening policy are given next.

**Yearly schedule of the association**

A typical year of the SIMPLE-Crypto Association follows four main steps:
* <strong><em>Yearly report.</em></strong> The developers of the association write a public 
report describing yearly progresses and listing potential plans for the next year.   
* <strong><em>Sponsors' workshop.</em></strong> Sponsors meet during an annual workshop to discuss 
the report and identify promising developments. The report is updated based on this feedback.
* <strong><em>Scientific council.</em></strong> The scientific council reviews the proposed developments
and establishes a priority list with potential developers. The report is updated based on this feedack.
* <strong><em>Projects selection.</em></strong> The association board approves the report. 
Developers are contacted following the priority list and open source projects are 
launched for one year given the budget constraints.

The two main criteria driving the selection of the projects are:
* Their scientific maturity (i.e., the existence of a theoretical 
background or convincing proofs-of-concept from the academic literature).
* Their mid/long-term relevance for emerging industrial applications.

**Lifetime of the association's projects**

The typical lifetime of an open source project follows the following stages:
* <strong><em>Development.</em></strong> The selected projects are 
developed towards prototype codes with accurate documentation and test vectors. Their
(e.g., physical) security is evaluated internally, by the association's
researchers. More precisely:
	* Codes are based on standard interfacess (e.g., [AXI](https://en.wikipedia.org/wiki/Advanced_eXtensible_Interface)
for hardware developments). 
	* Documentation includes a tool for predicting the exact state of an implementation at any given cycle, 
in order to facilitate worst-case physical security evaluations.
	* Preliminary security evaluation based on the open source evaluation tools
of the association ends with a report describing the best attack vectors found.
* <strong><em>Public evaluation.</em></strong> The prototype code is released 
under a copyleft licence together with its documentation, prediction tool and
preliminary security evaluation report. A challenge is organized 
based on public data sets, linked to scientific conferences whenever possible.
Bug bounties reward the possible detection of security flaws in the association's designs.
* <strong><em>Gold sponsoring.</em></strong> The code starts is used by a sponsor.
For a period of X years, the sponsoring enables its integration under
a non-copyleft license, while the code remains available under a copyleft license
for non commercial use, which we denote as dual licensing.
During this period, the detection of security flaws and bugs 
goes through a separate incident response process, following standard responsible
disclosure practice. Bugs are first communicated to the association and forwarded
to sponsors. Their public release may be delayed. In case security flaws imply
a need of re-design, this re-design is automatically suggested as a potential development
for the coming year. 
* <strong><em>Final release.</em></strong> After X years, the code is released 
under a non-copyleft license for the whole community.

**Licencing policy of the association** 

* <strong><em>Contributor License Agreement (CLA).</em></strong>
We ask contributors (individual or enterprises) to sign a CLA. It aims to:
	* Ensure that SIMPLE-Crypto can relicense the works;
	* Enable the dual-licensing model;
	* Ensure that SIMPLE-Crypto has authority to enforce the (open source) license clauses;
	* Ensure that no contributor will sue any user of the code for patent infringement caused by the contribution.
	
	The contributor is still guaranteed that:
	* He/she retains copyright on his/her contributions;
	* The contributions will be publicly licensed according to the development stage of the project.
	* The CLA is with SIMPLE, a non-profit organization whose statutary goal is to develop open source cryptographic implementations.
	
	For these purposes, the CLA requests a perpetual, worldwide, non-exclusive, no charge, royalty-free and irrevocable license to contributors.

* <strong><em>Dual licensing approach</em></strong>. Unless exception, the codes developed by the association
will be made available under an open source GPL-like license. In order to allow sponsors
to integrate these codes in products without the GPL constraints, we propose a dual licensing model
providing the benefits of a non-copyleft license to our gold sponsors.
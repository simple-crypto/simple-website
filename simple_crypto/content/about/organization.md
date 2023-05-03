---
title: Organization
aliases: ["/organization"]
---

The SIMPLE-Crypto Association is based on a flexible model with minimum 
overheads. It is aimed to enable the integration and maintenance of code projects from 
different partners. At high level, we
start funding researchers (possibly co-affiliated with 
other research institutes or universities) to evaluate and maintain the
codes once our scientific council expressed sufficient interest and we
collected sufficient sponsoring.

## Yearly schedule of the association {#schedule}

A typical year of the SIMPLE-Crypto Association follows four main steps:
* **Yearly report** The contributors of the association write a report
  describing yearly progresses and listing potential plans (with a tentative
  time budget) for the next year.   
* **Sponsors' workshop** Sponsors meet during an annual workshop to discuss 
the report and identify promising developments. The report is updated based on this feedback.
* **Scientific council** The scientific council reviews the proposed developments
and establishes a priority list of projects. It also makes suggestions of developers to contact. 
The report is updated based on this feedack.
* **Projects selection** The association board approves the report which is published on the SIMPLE-Crypto website. 
Developers are contacted to work on the projects of the priority list by the association's contact points
(see the people tag) and open source projects are launched (e.g., via internships or other relevant means) 
for one year given the budget constraints.

The four main criteria driving the selection of the projects are:
* Their scientific maturity (i.e., the existence of a theoretical 
background or convincing proofs-of-concept from the academic literature).
* Their security in the worst-case evaluation setting that the association promotes.
* Their mid/long-term relevance for emerging industrial applications.
* Their genericity and portability on the widest possible range of devices and platforms.

## Lifetime of the association's projects {#lifetime}

The typical lifetime of an open source project follows the following stages:
* **Development** The selected projects are 
developed towards prototype codes with accurate documentation and test vectors. Their
(e.g., physical) security is evaluated internally, by the association's
researchers. More precisely:
	* Codes are based on standard interfaces.
	* Documentation includes a tool for predicting the exact state of an implementation at any given cycle, 
in order to facilitate worst-case physical security evaluations.
	* Preliminary security evaluation based on the open source evaluation tools
of the association ends with a report describing the best attack vectors found.
* **Public evaluation** The prototype code is released 
under a copyleft licence together with its documentation, prediction tool and
preliminary security evaluation report. A challenge is organized 
based on public data sets, linked to scientific conferences whenever possible.
A call for contributions aiming at improving the code is open.
* **Gold sponsoring** The code is used in industrial projects.
The gold sponsoring enables its integration under
a non-copyleft license during the membership year, while it remains available under a copyleft license
for open source developments, which we denote as dual licensing.
As long as a code is gold-sponsored, the detection of security flaws 
goes through a separate incident response process, following standard responsible
disclosure practice and rewarded by bug bounties.
Flaws are first communicated to the association and forwarded
to sponsors. Their public release may be delayed. In case security flaws imply
a need of re-design, this re-design is automatically suggested as a potential development
for the coming year. 
* **Final release** Once the code has been gold-sponsored 
for 5 years, it is released under a non-copyleft license for the whole community.


## Intellectual property policy of the association {#licenses}

**Licensing of SIMPLE-Crypto implementations**
The type of license under which SIMPLE-Crypto implementations are released depends on
the project stage:
* For the development and public evaluation stages, we use only copyleft licenses. Precisely,
we use the GPLv3 license for software developments and CERN OHL-S for hardware developments.
* During the gold sponsoring stage, we use a dual licensing approach. Codes are available under the 
same copyleft license as for the development and public evaluation stages for open source developments. 
Gold sponsoring gives access to a yearly non-copyleft license for commercial closed source developments.
Precisely, sponsors are granted a yearly MIT-like license during the gold sponsoring. 
* When final release takes place, the codes become available for the whole community
under a perpetual non-copyleft licenses. Precisely, we use a MIT-like license for both software and
hardware developments. 

Our evaluation tools are published under a copyleft license, namely the AGPLv3.
They will not be released under a perpetual non-copyleft license because we expect
tools to be continuously updated.
Silver sponsoring grants access to a yearly non-copyleft licence.

**Contributions welcome**
We welcome contributions to our projects! In order to enable the licensing
model explained above, we require contritubotors to signe a Contributor License
Agreement (CLA), see [the contributing page](/contributing) for more details.

**Patents**
The SIMPLE-Crypto Association does not fill patents.
Our developments are all based on peer-reviewed published solutions and are either free of patents 
or should become free of patents in the long term. In the mid term, code projects are
provided "as is", without warranty of noninfringement, express or implied.


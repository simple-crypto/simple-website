---
layout: default
title: Organization
---
# {{ page.title }}

The SIMPLE-Crypto Association is based on a flexible model with minimum 
overheads. It is aimed to enable the integration and maintenance of code projects from 
different partners. At high level, we
start funding researchers (possibly co-affiliated with 
other research institutes or universities) to evaluate and maintain the
codes once our scientific council expressed sufficient interest and we
collected sufficient sponsoring. We next detail:

* The [yearly schedule of the association](#schedule),
* The [lifetime of the association's projects](#lifetime),
* The [licencing policy of the association](#licenses).

**<a name="schedule">Yearly schedule of the association</a>**

A typical year of the SIMPLE-Crypto Association follows four main steps:
* <strong><em>Yearly report.</em></strong> Thecontributors of the association write a report describing yearly progresses and listing potential plans (with a tentative time budget) for the next year.   
* <strong><em>Sponsors' workshop.</em></strong> Sponsors meet during an annual workshop to discuss 
the report and identify promising developments. The report is updated based on this feedback.
* <strong><em>Scientific council.</em></strong> The scientific council reviews the proposed developments
and establishes a priority list of projects. It also makes suggestions of developers to contact. 
The report is updated based on this feedack.
* <strong><em>Projects selection.</em></strong> The association board approves the report which is published on the SIMPLE-Crypto website. 
Developers are contacted to work on the projects of the priority list by the association's contact points
(see the people tag) and open source projects are launched (e.g., via internships or other relevant means) 
for one year given the budget constraints.

The four main criteria driving the selection of the projects are:
* Their scientific maturity (i.e., the existence of a theoretical 
background or convincing proofs-of-concept from the academic literature).
* Their security in the worst-case evaluation setting that the association promotes.
* Their mid/long-term relevance for emerging industrial applications.
* Their genericity and portability on the widest possible range of devices and platforms.

**<a name="lifetime">Lifetime of the association's projects</a>**

The typical lifetime of an open source project follows the following stages:
* <strong><em>Development.</em></strong> The selected projects are 
developed towards prototype codes with accurate documentation and test vectors. Their
(e.g., physical) security is evaluated internally, by the association's
researchers. More precisely:
	* Codes are based on standard interfaces (e.g., [AXI](https://en.wikipedia.org/wiki/Advanced_eXtensible_Interface){:target="_blank"}
for hardware developments). 
	* Documentation includes a tool for predicting the exact state of an implementation at any given cycle, 
in order to facilitate worst-case physical security evaluations.
	* Preliminary security evaluation based on the open source evaluation tools
of the association ends with a report describing the best attack vectors found.
* <strong><em>Public evaluation.</em></strong> The prototype code is released 
under a copyleft licence together with its documentation, prediction tool and
preliminary security evaluation report. A challenge is organized 
based on public data sets, linked to scientific conferences whenever possible.
A call for contributions aiming at improving the code is open.
* <strong><em>Gold sponsoring.</em></strong> The code is used in industrial projects.
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
* <strong><em>Final release.</em></strong> Once the code has been gold-sponsored 
for 5 years, it is released under a non-copyleft license for the whole community.

**<a name="licenses">Licencing policy of the association</a>** 

* <strong><em>Contributor License Agreement (CLA).</em></strong>
We welcome contributions to our projects, see <a href="/contributing">this
page</a> for more details.

* <strong><em>Licensing of SIMPLE-Crypto implementations.</em></strong> 
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

Our evaluation tools will be published under a copyleft license, namely the AGPLv3 one.
Silver sponsoring grants access to a yearly non-copyleft licence, namely a MIT-like one.
They will not be released under a perpetual non-copyleft license because we expect
tools to be continuously updated.

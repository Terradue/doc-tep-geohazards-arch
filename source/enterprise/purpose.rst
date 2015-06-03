Enterprise Viewpoint - Purpose of the system
############################################

The Enterprise Viewpoint describes the Geohazards Exploitation Platform's science and business requirements and how to meet them.

Community contract
------------------

The main purpose of the system gathering together the GEP community is expressed in a contract that specifies how the community objective can be met. This contract:

+ states the objective for which the community exists;

+ governs the structure, the behaviour and the policies of the community;

+ constrains the behaviour of the members of the community;

+ states the rules for the assignment of enterprise objects to roles.

The satellite EO and geohazards community is growing in size and importance, with the advent of large new initiatives and projects of global interest. 
The Committee on Earth Observation Satellites (CEOS) is coordinating globally this community, through its Disasters Working Group.
The geohazards platform or GEP contributes to this expanding community a unique set of tools, allowing them to forge new applications in direct collaboration with large numbers of actors. 

In particular, the community will benefit from a cloud-based workspace, allowing advanced EO data exploitation activities and offering access to a broad range of shared processing tools. 
GEO is a community platform. Each partner brings tools and processing chains, but also has access in the same workspace to large data sets and shared processing tools. 

The vision for the Platform was inspired by the Scientific & Technical Memorandum of the the International Forum on Satellite EO for Geohazards [R1]_.

The platform is intended to support operational users with a mandate in seismic risk management, 
as well as a range of geoscience users in research institutes and universities. 
Operational users are focused on disaster prevention, preparedness, early warning, and response.
Academic users are focused on the scientific use of data, with the main goal of understanding the physics of earthquakes, thereby improving our ability to characterize, understand, and model seismic risk.
Overall, the Satellite EO for Geohazards community encompasses the following actors:

* Satellite data providers

  * National or international space agencies like ESA, which operate satellites (CEOS has 9 space agencies members). 
  * Commercial satellite operators or commercial suppliers of data.

* Value-adder companies (or VACs)

  * Companies using satellite data to generate information products that can be used directly by end users to address a need. 
  * Companies active in a wide range of information sectors ranging from oil & gas industries to environmental applications, disaster risk management and many others.

* Research institutes and academia

  * Involved through government-sponsored grants for basic research 
  * Involved in support of applied research objectives

* Industrial partners with an interest in geohazards research

* Operational geohazards actors

  * National and regional civil protection agencies
  * Seismological centres 
  * National and local authorities in charge of seismic risk management 

* Other forms of association of researchers

  * the Geohazard Supersites and Natural Laboratories (GSNL)
  * the European Plate Observing System (EPOS)

The CEOS Working Group on Disasters is committed to support and enhance the access to in-situ and satellite observations, at the global scale, for this geohazards community.
This is defining the main purpose of the Geohazards Thematic Exploitation Platform, that we refine hereafter into a set of community objectives.
The system is then designed in terms of processes that meet these objectives. 
Such processes (see the next section "Scope of the system) allow the system actors to interact and behave in order to fulfill the stated goal and objectives.
According to the RM-ODP approach, the complete behaviour for a role in the community is modelled by the actions for that role in a number of processes.
Processes (activity or sequence diagrams) and behaviors (state diagrams) are modelled in this Enterprise viewpoint of the RM-ODP architecture.

As a summary, the community is modeled in the RM-ODP Enterprise Specification as a set of stakeholders and their identified roles, governed by a set of community rules.

<< EV_Community >>

Community objectives
--------------------

The community contract models the agreement amongst the members to work together to meet a shared goal, and more concretely a set of objectives.
For the GEP community, the designed system has to implement technical processes that help achieve the following set of objectives.

**Exploitation and collaboration**

* EV_Objective **comm1**: Evolve SSEP to promote a reference platform for different thematic domains, starting with geohazards
* EV_Objective **comm2**: Measure community validated usages of EO data 
* EV_Objective **comm3**: Investigate means for accessing and exploiting commercial data assets
* EV_Objective **comm4**: Involve stakeholders for long term sustainable operations

**Processor integration**

* EV_Objective **integ1**: Support processor integration for massive parallel processing
* EV_Objective **integ2**: Demonstrate a smooth transition from integration to operations
* EV_Objective **integ3**: Investigate means for accessing and exploiting commercial processor assets

**Cloud bursting**

* EV_Objective **burst1**: Allow the selection from a range of Cloud Providers to run a processing task 
* EV_Objective **burst2**: Support application deployments on a selected Cloud Provider
* EV_Objective **burst3**: Demonstrate an exploitation approach based on a pay-per-use model

**Digital science**

* EV_Objective **digit1**: Allow the rapid creation and web-publication of added-value science products (e.g. co-seismic interferograms)
* EV_Objective **digit2**: Review, re-produce and qualify science products from 3rd parties 
* EV_Objective **digit3**: Support increased access to EO derived information, through inter-disciplinary exchange and cooperation

**CEOS Pilots synergy**

* EV_Objective **ceos1**: Foster EO resource & knowledge sharing for capacity building at global scale
* EV_Objective **ceos2**: Provide EO data (InSAR, optical) and processing capacities to existing initiatives
* EV_Objective **ceos3**: Demonstrate advanced science products for rapid earthquake response and to reduce impact & risk from volcanic eruptions

**Geohazards Supersites and Natural Laboratories synergy**

* EV_Objective **gsnl1**: Map hazard prone land surfaces in geologically active regions
* EV_Objective **gnsl2**: Monitor terrain deformations in geologically active regions
* EV_Objective **gnsl3**: Ensure easy access to Earth Science data to promote their use and advance scientific research
* EV_Objective **gnsl4**: Manage Permanent Supersites, Candidate Supersites, Event Supersites, and Natural Laboratories

**Seismic hazards knowledge**

* EV_Objective **seismic1**: Support production of new observations of the seismic belts (~15% of land surface)
* EV_Objective **seismic2**: Contribute to improved understanding of seismic events
* EV_Objective **seismic3**: Support Geoscience users to characterize, understand, and model seismic risk

**Volcanic eruptions monitoring**

* EV_Objective **volcano1**: Support monitoring of all Holocene era volcanoes on a global basis (~1500 vocanoes)
* EV_Objective **volcano2**: Involve National and Regional Civil Protection authorities, Seismological centers, National & Local authorities

The next section identifies the GEP processes (EV_Process) to be modelled as activity diagrams.



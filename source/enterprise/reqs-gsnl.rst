Enterprise Viewpoint - Requirements - GEO Supersites and Natural Laboratories 
#############################################################################

The ESA Geohazards Exploitation Platform is pursuing and developing a synergy with the GEO/GEOSS Geohazards Supersites and Natural Laboratories (GSNL) effort (http://supersites.earthobservations.org/).

"Supersites is an initiative of the geohazard scientific community. The Supersites provide access to spaceborne and in-situ geophysical data of selected sites prone to earthquake, volcano or other hazards". A list of Permanent Geohazard Supersites is selected for scientific reasons as well as for community building opportunities.

The list of Permanent Supersites as of June 2015 is as follows:
* Marmara Region
* San Andreas Fault, USA
* Campi Flegreii and Vesuvius, Italy
* Mt Etna, Italy
* Hawaiian volcanoes, USA
* Iceland volcanoes, Iceland
* New Zealand volcanoes, New Zealand
* Ecuadorian volcanoes, Ecuador

In support of this effort, the ESA Geohazards Exploitatin Platform provides a Cloud Platform connected to EO data catalogues and is aiming at facilitating data staging and data processing for users accessing these data sources from the Platform. 

The interoperability of the Platform with EO data catalogues and repositories is coordinated in order to reduce the data gaps in a number of key domain objectives. The GSNL domain is one of them, and is supported by the Platform data access and processing capabilities in the realization of four pragmatic objectives:

* **EV_Objective gsnl1**: Map hazard prone land surfaces in geologically active regions;
* **EV_Objective gnsl2**: Monitor terrain deformations in geologically active regions;
* **EV_Objective gnsl3**: Ensure easy access to Earth Science data to promote their use and advance scientific research;
* **EV_Objective gnsl4**: Manage Permanent Supersites, Candidate Supersites, Event Supersites, and Natural Laboratories.

These objectives are contributing the present Geohazards Exploitation Platform architecture as part of the EV_Community_Contract aimed at supporting the GSNL initiative.

They relate to several EV_Processes of the ESA Geohazards Exploitatin Platform, and enabled for users as EV_Interactions on the Platform in which Enterprise Objects participate (Cloud resources, Processing services, Web Portal, ...).

The corresponding system requirements for the implementation of the 4 identified objectives are as follows:

* The GEP is meant to allow users to easily exploit EO data resources by combining fast data access, processing facilities and flexibility for the user’s own data analysis.
* The platform provides Data Access, Data Processing Services and PaaS (Platform as a Service).
* Data Access includes the possibility to perform catalogue queries.
* Data Processing Services enable users to process data available in the repository using a number of well know tools and to exploit the results.

The Enterprise Objects supporting the Platform implementation to support the GNSL EV_Objectives are identified in the Architecture diagrams as follows:

* **Portal**: the Platform's web presence entry point.
* **geoBrowser**: the Portal service for user interation with the Platform resources, including advanced search capabilities on the Platform's resources via e.g. "geospatial", "time", "data collections" and "EO-based productions" search facets.
* **processingServices**: the platform's resources dedicated to a "microservices" approach (in the current state, through Virtual Machines resources) for handling the inclusion on the platform of individual data processing units, per processor type (NEST, GAMMA, GMTSAR, ROI_PAC, ... including the proxying of existing G-POD services).
* **cloudControler**: the platform's engine for Cloud resources management. 
* **eoDataContext**: the geoBrowser's service for management of EO data sources, referenced from EO data providers catalogues, and including data access up to distributed EO data repositories (VA-4, ...).
* **eoProductsContext**: the geoBrowser's service for referencing processing jobs runs and results (final and intermediate), to allow users understand a processor, and its possible improvements

These Enterprise Objects are designed and implemented on the Platform to answer the identified GSNL objectives, in terms of scientific analysis, production and results sharing tasks.

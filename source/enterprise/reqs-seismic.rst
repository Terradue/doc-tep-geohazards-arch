Enterprise Viewpoint - Requirements - CEOS Pilot on Seismic Hazards
####################################################################

The CEOS Pilot on Seismic Hazards is driven by the CEOS Disaster Risk Management (DRM) Observation Strategy, 
and is delivered by CEOS as a response to a collection of observation requirements from the user community, 
to be implemented in 2014-2016.

The CEOS Pilot on Seismic Hazards aims at demonstrating: 

1. Added-value and uniqueness of increased CEOS coordination in this area; 
2. Benefits of closer ties to users and ease of access to data; 
3. Potential for increased roles of space agencies in Disasters Risk Management, for the 10-year period starting in 2015.

In support of this vision, the ESA Geohazards Exploitatin Platform, 
as a Cloud Platform contributing to community building in this Pilot area,
is aiming at supporting the Seismic Hazards community with the realization of three pragmatic objectives:

* **EV_Obj seismic1**: Support production of new observations of the seismic belts (around 15% of the land surface);
* **EV_Obj seismic2**: Contribute to improved understanding of seismic events;
* **EV_Obj seismic3**: Support Geoscience users to characterize, understand, and model seismic risk.

These objectives are contributing the present Geohazards Exploitation Platform architecture as part of the EV_Community_Contract aimed at supporting the CEOS Pilot.

They relate to several EV_Processes of the ESA Geohazards Exploitatin Platform, and enabled for users as EV_Interactions on the Platform in which Enterprise Objects participate (Cloud resources, Processing services, Web Portal, ...).

The corresponding system requirements for the implementation of the 3 identified objectives are as follows:

* The GEP is meant to allow users to easily exploit EO data resources by combining fast data access, processing facilities and flexibility for the user’s own data analysis.
* The platform provides Data Access, Data Processing Services and PaaS (Platform as a Service).
* Data Access includes the possibility to perform catalogue queries.
* Data Processing Services enable users to process data available in the repository using a number of well know tools and to exploit the results.
* The PaaS enables users to perform their data exploitation activities with large flexibility and autonomy by using one or several virtual hosts directly provided on the Cloud platform where the data resides.

The Enterprise Objects supporting the Platform implementation are identified in the Architecture diagrams as follows:

* **Portal**: the Platform's web presence entry point.
* **geoBrowser**: the Portal service for user interation with the Platform resources, including advanced search capabilities on the Platform's resources via e.g. "geospatial", "time", "data collections" and "EO-based productions" search facets.
* **oseCatalogue**: the EO data search hub for all the distributed EO data catalogues and partners resources registered on the Platform, leveraging the OGC OpenSearch extensions standard and ElasticSearch technology.
* **processingServices**: the platform's resources dedicated to a "microservices" approach (in the current state, through Virtual Machines resources) for handling the inclusion on the platform of individual data processing units, per processor type (NEST, GAMMA, GMTSAR, ROI_PAC, ... including the proxying of existing G-POD services).
* **cloudControler**: the platform's engine for Cloud resources management. 
* **eoDataContext**: the geoBrowser's service for management of EO data sources, referenced from EO data providers catalogues, and including data access up to distributed EO data repositories (VA-4, ...).
* **eoProductsContext**: the geoBrowser's service for referencing processing jobs runs and results (final and intermediate), to allow users understand a processor, and its possible improvements
* **eoPublicationsContext**: the geoBrowser's service for referencing scientific community curated results (scientific papers), and make them available for community building and to support users goals with EO data exploitation on the Platform.
* **eoCommunityContext**: the geoBrowser's service for referencing  web accessible content that labs, institutes or agencies are openly sharing on the web, and make them available for community building and to support users goals with EO data exploitation on the Platform.

These Enterprise Objects are designed and implemented on the Platform to answer the identified CEOS Seismic Pilot objectives, in terms of scientific analysis, production and results sharing tasks.

Enterprise Viewpoint - Scope of the system
##########################################

With the scope of the system, we describe the Platform expected behaviour, i.e., the way it is supposed to work and interact with its environment in the TEP context.

The targeted operational roles are:

* Data access
* Processor integration
* Data processing and Cloud bursting
* Data visualization and analysis
* Reproducible Science collaborations
* Capacity Building through Data Sharing 

Within RM-ODP, the scope of the system is modelled as the set of community objectives that are fulfilled by the provided roles and behaviours.

System Capabilities
===================

The platform is meant to allow users to easily exploit EO data resources by combining fast data access, processing facilities and flexibility for the user's own data analysis. 
The platform provides Data Access, Data Processing Services and PaaS (Platform as a Service). 

* Data Access includes the possibility to perform catalogue queries. 
* Data Processing Services enable users to process data available in the repository using a number of well know tools and to exploit the results. 
* The PaaS enables users to perform their data exploitation activities with large flexibility and autonomy by using one or several virtual hosts directly provided on the Cloud platform where the data resides. 

Users can therefore use their virtual hosts to efficiently access data and processing services, and immediately elaborate results by exploiting the analysis and visualization tools made available from the PaaS, or that they can directly install themselves in their virtual host. 
In addition, users can also open their own accounts on a commercial Cloud Provider, and directly provision their virtual hosts independently (through the Geohazards Platform Services).

Roles actions and interactions
==============================

Roles on the Platform are complying to a community policy, and are defined as a set of actions and interactions (EV_Behaviours), observable in the system through process steps involving three types of Enterprise Objects: Actors (e.g. a user), Resources (e.g. a data processor) and Artefacts (e.g. data processing results).

<< Enterprise_Spec >>
Community Roles

<< Enterprise_Spec >>
Community Policy

<< Enterprise_Spec >>
Community Processes

<< Enterprise_Spec >>
Enterprise Objects

<EV_Role> Data access
---------------------

* EV_Policy:
* EV_Process:
TBD

<EV_Role> Processor integration
-------------------------------

* EV_Policy:
* EV_Process:
* EV_Resource: vmDeveloperCloudSandbox
TBD

<EV_Role> Data processing and Cloud bursting
--------------------------------------------

Users can instantiate (on-demand) a processing service appliance, provision the appliance on a pre-configured Cloud Provider and invoke the processing via the OGC Web Processing Service interface.
Users define input data and select a results location (e.g. portal, cloud block storage, dropbox, google drive, ...)

* EV_Policy:
* EV_Process: runJob - On-demand cloud appliance

.. uml::

       title runJob - On-demand cloud appliance
       actor endUser
       ' Boundary (view in MVC) Objects that interface with system actors   
       boundary geoBrowser 
       ' Entity (model in MVC): Objects representing system data
       ' model descriptions are delegated to the Information viewpoint
       ' Control (controller in MVC): Objects that mediate between boundaries and entities
       control processingServices
       control eoDataContext
       control cloudControler

       endUser <-> geoBrowser: interact
       geoBrowser -> processingServices: selectProcessor
       activate processingServices
       geoBrowser <-- processingServices: selected 
       deactivate processingServices

       geoBrowser -> eoDataContext: selectDatasets
       activate eoDataContext
       geoBrowser <-- eoDataContext: selected
       deactivate eoDataContext

       endUser -> geoBrowser: Allocate selected input data
       endUser -> geoBrowser: runJob

       geoBrowser -> cloudControler: provision Cloud appliance with processor and input data
       activate cloudControler
       cloudControler->cloudControler: validate request against user quota
       ref over cloudControler: warning if quota exceeded
       cloudControler --> userCloudStorage: Deliver results
       geoBrowser <-- cloudControler: Reference to results
       deactivate cloudControler

       endUser -> userCloudStorage: access generated EO-based products
       endUser -> geoBrowser: share generated eO-based products
      
Users can run existing processing services (e.g. G-POD services) and and invoke the processing via the OGC Web Processing Service interface.
Users define input data and select a results location (e.g. portal, cloud block storage, dropbox, google drive, ...)

* EV_Policy:
* EV_Process: runJob - On-demand computing element

.. uml::

       title runJob - On-demand computing element
       actor endUser
       ' Boundary (view in MVC) Objects that interface with system actors   
       boundary geoBrowser 
       ' Entity (model in MVC): Objects representing system data
       ' model descriptions are delegated to the Information viewpoint
       ' Control (controller in MVC): Objects that mediate between boundaries and entities
       control processingServices
       control eoDataContext
       control cloudControler

       endUser <-> geoBrowser: interact
       geoBrowser -> processingServices: selectProcessor
       activate processingServices
       geoBrowser <-- processingServices: selected 
       deactivate processingServices

       geoBrowser -> eoDataContext: selectDatasets
       activate eoDataContext
       geoBrowser <-- eoDataContext: selected
       deactivate eoDataContext

       endUser -> geoBrowser: Allocate selected input data
       endUser -> geoBrowser: runJob

       geoBrowser -> cloudControler: provision grid computing element with input data parameter
       activate cloudControler
       cloudControler->cloudControler: validate request against user quota
       ref over cloudControler: warning if quota exceeded
       cloudControler --> userCloudStorage: Deliver results
       geoBrowser <-- cloudControler: Reference to results
       deactivate cloudControler

       endUser -> userCloudStorage: access generated EO-based products
       endUser -> geoBrowser: share generated EO-based products

<EV_Role> Data visualization and analysis
-----------------------------------------

* EV_Policy:
* EV_Process:
* EV_Resource: vmCloudToolbox

The platform is meant to allow users to perform data visualisation tasks:

* from processing software toolboxes hosted on their dedicated virtual machine: visualize and analyse EO-based products, e.g. to further apply data manipulation tools to them.
* from Web Portal Geobrowser: overlay EO data collections density maps, geohazards events layers (e.g. Disasters Charter activations)
* still from the Web Portal Geobrowser: combine EO data footprints and EO-based products to support data processing decision making (selection of processing input data, discovery and analysis of data processing results)

<EV_Role> Reproducible Science collaboration
--------------------------------------------

* EV_Policy:
* EV_Process:

The Geohazards Platform is investigating on different collaborative eScience scenarios made available to users:

* Job run sharing, allowing users to see a job processing parameters and results, and reuse a job definition as a baseline for further runs. 
* Collaborative work on algorithm integration, Virtual Machines accessing Git repositories, like offered by social coding platforms such as GitHub).
* Cloud bursting of Processing services to Commercial Clouds, in order to enable low-cost, massive data processing campaigns.

<EV_Role> Capacity Building through Data Sharing
------------------------------------------------

The Geohazards Web Portal is investigating on different work areas (or 'contexts') made available to users:

<EV_Behaviour> EO Data exploitation
+++++++++++++++++++++++++++++++++++

* EV_Policy:
* EV_Process:

* dedicated to EO data collections available as input data for processing tasks
* provides Portal links to automate the discovery allowing users to easily feed processing tasks

<EV_Behaviour> EO-based products exploitation
+++++++++++++++++++++++++++++++++++++++++++++

* EV_Policy:
* EV_Process:

* dedicated to GEP processors results (final and intermediate processing outputs) 
* provides Portal links to processing jobs runs, to allow users understand a processor, and its possible improvements 

<EV_Behaviour> Publication referencing
++++++++++++++++++++++++++++++++++++++

* EV_Policy:
* EV_Process:

* related to the scientific community curated results (scientific papers)
* provides Portal links to collateral resources (like in GEP, data and processors) that allow researchers to understand and reproduce an experiment or a production

<EV_Behaviour> Community sharing
++++++++++++++++++++++++++++++++

* EV_Policy:
* EV_Process:

* dedicated to geotag and reference web accessible content that labs, institutes, agencies, ... are openly sharing on the web (articles and blog posts, products images delivered in web-browser compatible formats, ...)
* provides a Portal integration mechanism based on the OGC standard "OWS Context" (http://www.opengeospatial.org/standards/owc)


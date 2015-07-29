Enterprise Viewpoint - Interactions between roles
#################################################

This section introduces the design contraints and the required interactions between roles.


Different services
------------------

The users of the platform are provided with several interaction points:

- a website, with pages for the general public and some entry points for the registered users

- a geobrowser, with a Shop Window for the general public, and other features for registered users

- a cloud dashboard for the monitoring of quotas consumption and cloud processing tasks for registered "end-users"

- a cloudSandbox environment for processor integration (or catalogue provisioning) activities for "expert" users

- a social media handle for registered users, with different levels of usage (within the website or towards third party social media platforms)

- a Control Panel for the administrators of the Platform's resources (Data collections, Data Packages, Groups, Users, WPS providers, Web Processing Services, News, Banners)

User profiles are defined to specialize the interactions between roles, in order to map the underlying processes with community objectives.

.. uml::

  left to right direction
  skinparam packageStyle rect
  actor Users
  rectangle Platform {
    Users -- (interact with websitePages)
    Users -- (interact with geoBrowser)
    Users -- (interact with cloudDashboard)
    Users -- (interact with cloudSandbox)
    Users -- (interact with socialwebHandle)
  }

Constraints on Data providers | Administrators interactions
------------------------------------------------------------

- Existing catalogues of EO Data Collections can be registered through a Catalogue Description Url, compliant with the OGC standard "OpenSearch Geo & Time extension". Collections are registered along with an identifier, a name and a description.

- Partner Data Admins are also provided with an organisational interface (handled through ESA RSS) which can setup a dedicated FTP resource (or access a provided one) and will migrate the uploaded data collections onto the Platforms storage, create the catalogue references, and make it registered on the Platform.

Constraints on Processor integrators | end-users interactions
--------------------------------------------------------------

Different integration options are supported by the Platform:

- Single machine integration: the user is provided with a Virtual Machine acting as a desktop machine, but with enhanced capacities to access the Platform's data collections. The user must access the VM through a VNC connexion, and has to use the resources made available from the Platform (GAMMA software, ESA toolboxes, ...).

- Hadoop Streaming API integration: the user is provided with a Developer Cloud Sandboc environment, offering APIs and tools to integrate an existing application code, and make it acknowledged by the Hadoop framework. Once integrated in the provided framework, the application can scale under the automatic management of the Hadoop framework (job distribution and task trackers over a compute cluster).

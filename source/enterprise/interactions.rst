Enterprise Viewpoint - Interactions between roles
#################################################

The design contraints and the required interactions between roles are...

Different services
------------------

.. uml::

       title webPortal entry point
       actor Users
       ' Boundary (view in MVC) Objects that interface with system actors   
       boundary websitePages
       boundary geoBrowser 
       boundary cloudDashboard
       boundary cloudSandbox
       boundary socialWebHandle
       ' Entity (model in MVC): Objects representing system data
       ' model descriptions are delegated to the Information viewpoint
       ' Control (controller in MVC): Objects that mediate between boundaries and entities

       Users <-> websitePages: interact
       Users <-> geoBrowser: interact
       Users <-> cloudDashboard: interact
       Users <-> cloudSandbox: interact

Data providers and Administrator users
--------------------------------------

TBD

Processor integrators and end-users
-----------------------------------

TBD

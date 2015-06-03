Enterprise Viewpoint - Interactions between roles
#################################################

The design contraints and the required interactions between roles are...


Different services
------------------

The users of the platform are provided with several interaction points:

- a website, with pages for the general public and some entry points for the registered users

- a geobrowser, with a Shop Window for the general public, and other features for registered users

- a cloud dashboard for the monitoring of quotas consumption and cloud processing tasks for registered "end-users"

- a cloudSandbox environment for processor integration (or catalogue provisioning) activities for "expert" users

- a social media handle for registered users, with different levels of usage (within the website or towards third party social media platforms)

User profiles are defined to specialize the interactions, in order to map the underlying processes with community objectives.

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

TBD

Constraints on Processor integrators | end-users interactions
--------------------------------------------------------------

TBD

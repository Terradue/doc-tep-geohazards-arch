Enterprise Viewpoint - Scope of the system
##########################################

With the scope, we describe the Platform expected behaviour, i.e., the way it is supposed to work and interact with its environment in the TEP context.

The targeted operational processes are:

* Data access
* Processor integration
* Data processing and Cloud bursting
* Visualization
* Reproducible Science
* Capacity Building through Data Sharing 

Within RM-ODP, the scope of the system is modelled as the set of roles it fulfils.

System Capabilities
-------------------

The platform is meant to allow users to easily exploit EO data resources by combining fast data access, processing facilities and flexibility for the user's own data analysis. 
The platform provides Data Access, Data Processing Services and PaaS (Platform as a Service). 
Data Access includes the possibility to perform catalogue queries. 
Data Processing Services enable users to process data available in the repository using a number of well know tools and to exploit the results. 
The PaaS enables users to perform their data exploitation activities with large flexibility and autonomy by using one or several virtual hosts directly provided on the Cloud platform where the data sits. 
Users can, therefore, use their virtual hosts to efficiently access data and processing services and immediately elaborate results using analysis and visualization tools available from the PaaS or directly installed in virtual hosts by themselves. 
In addition users can also open their own accounts on a commercial Cloud Provider and directly provision their virtual hosts independently (through the Geohazards Platform Services).

**Roles and Processes**

* EV_Role:
* EV_Behaviour:
* EV_Process:

<< Enterprise_Spec >>
Community Roles

<< Enterprise_Spec >>
Community Processes

.. uml::

       title Authentication Sequence
       Alice->Bob: Authentication Request
       note right of Bob: Bob thinks about it
       Bob->Alice: Authentication Response
       title Second Sequence
       Mike->Beth: Hello
       Mike<-Beth: Hi, how are you !
       
.. uml::

       actor Foo1
       boundary Foo2
       control Foo3
       entity Foo4
       database Foo5
       Foo1 -> Foo2 : To boundary
       Foo1 -> Foo3 : To control
       Foo1 -> Foo4 : To entity
       Foo1 -> Foo5 : To database
       
.. uml::

       participant User

       User -> A: DoWork
       activate A

       A -> B: << createRequest >>
       activate B

       B -> C: DoWork
       activate C
       C --> B: WorkDone
       destroy C

       B --> A: RequestCreated
       deactivate B

       A -> User: Done
       deactivate A


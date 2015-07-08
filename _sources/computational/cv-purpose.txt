Computational Viewpoint - Level of abstraction
##############################################

The computational viewpoint is defined within RM-ODP as the recipient for the functional decomposition of the system into a set of objects that interact at interfaces – enabling system distribution. It thus provides the basis for decisions on how to distribute the components to be handled by the system. It is unique to the system and therefore provides the reference model for ensuring consistency between different engineering and technology specifications (including programming languages and communication mechanisms). This is aiming at open interworking and portability of components in the resulting implementations. For example, the Computational specification is used as the baseline for the Engineering specification, the later defining the communications mechanisms supporting the behaviour at the interfaces of the system.

For these reasons, the configuration and degree of distribution of the infrastructure on which ODP applications are run can be altered, based on the documented environment contracts associated with interfaces, without having a major impact on the application software.

A computational component is defined as a way to model functional decomposition, has state and behaviour, and has interactions  achieved through interfaces. 
An Environment contract between a component and its environment can cover Quality of Service (QoS) constraints (delays, throughput, availability), usage constraints and component management constraints.







This section describes the design choices to cope with the usage constraints. I describes the computational model that manly consists of :
 
- the components (objects) participating to the real‐time behaviour, from which the system is constructed;
- the service model on which the system is executed and its associated mechanisms;
- the means of communication between components/objects (e.g. interfaces, format, parameters)

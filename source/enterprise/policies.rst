Enterprise Viewpoint - Policies governing the system design
###########################################################

The Policies governing the system design are defined in this Enterprise Viewpoint.
They are brought to the design activity by a user community to be supported on the system, and modelled as part of the EV_Community objects (definitin each user community) of the design.

**Policiy objects definition in RM-ODP**

* << EV_PolicyEnvelope >>: is a flexible way to gather the set of rules related to a purpose of the community on the system, basically either from the European contribution to GSNL, or from B2B goals. For a given policy envelope, only one policy value is in force at a point in time.
* << EV_PolicyValue >>: is a particular set of bahavioral rules related to some purpose that are applicable at some moment in time as a result of a business decision to apply them. These Policy value rules may comprise obligations, permissions, prohibitions, authorizations, accountable actions, delegation, commitment.

**List of Policies identified during the design activities**

There are mainly 3 areas of policies driving the system design.

<< EV_PolicyEnvelope >>: EO data access and sharing policies (visualization and download) 
* << EV_PolicyValue >>: ESA EO data access and sharing policy
* << EV_PolicyValue >>: Third-Party EO data provider data access and sharing policy (DLR, ASI, JAXA)
NOTE: policies implementation on download and processing quotas are delegated to the future evolutions of the platform

<< EV_PolicyEnvelope >>: EO data processor terms of use
* << EV_PolicyValue >>: a given Processor terms of use (Opensource, Commercial)

<< EV_PolicyEnvelope >>: Public Cloud Provider policies
* << EV_PolicyValue >>: a given Public Cloud Provider terms of use
* << EV_PolicyValue >>: a given Public Cloud Provider API capabilities



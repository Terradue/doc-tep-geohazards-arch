Engineering Viewpoint - Infrastructure Constraints
##################################################


The Infrastructure Constraints for the Thematic Exploitation Platform
captures the requirements for installation of the software element on its
base infrastructure. It specifies the basic installation requirements
for the component without consideration for its interaction
with other system components. Hence, satisfaction of the
Infrastructure Constraints specification does not imply proper
functional operation of the Tep Exploitation Platform.

The computing constraints are calculated on the basis of the number of users and
their insfrastructure needs for data and processing as described in :ref:`ev-userreq`.

General Operating System Constraints
------------------------------------

All system described hereafter are deployed on a similar baseline for the operating system
and the initial configuration:

- Centos 6 x86_64 arch


Web Portal Computing Constraints
--------------------------------

The minimum computing requirements of the system on which the Web Portal are:

- 8 core or thread CPUs at 2Ghz
- 16Gb RAM
- 250Gb HD
- Gigabit Network interface

Web Portal Security Constraints
-------------------------------

By default all ports of any protocol on every external network interface is closed for any inbound connection.
According to the type of deployment, The following exceptions must be defined in hte firewall system:

**Frontline Web Server**

- port 443 for HTTPS traffic on protocol TCP


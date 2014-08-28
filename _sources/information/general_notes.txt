.. _general_notes:

General Notes
#############

The Sandbox, short of *Terradue's Developer Cloud Sandbox*, is a Virtual Machine (VM) running the CentOS 6.5 Linux distribution. This VM has the complete set of tools of the CIOP framework (the 'ciop' command line tools). Furthermore it has CDH (Cloudera's Distribution of Apache Hadoop) installed in Pseudo-Distributed mode [#f1]_. 

Getting started
^^^^^^^^^^^^^^^^

* The Sandbox is set to automatically login as the user *<sandbox_user>*. Please refer to the section :doc:`Connect to your Sandbox <../start/sandbox>`.

Using the code examples
^^^^^^^^^^^^^^^^^^^^^^^^

* In some command-line steps in the exercises, you will see lines like this:

.. code-block:: console

 ciop-simjob -n my_node
 
The dollar sign ($) at the beginning of each line indicates the Linux shell prompt. The actual prompt will include additional information (e.g. *[user@sb-10-15-10-10.terradue.int]$* ) but it is omitted from these instructions for brevity. 

* If not otherwise specified, all the commands of these Hands-On refer to the $_CIOP_APPLICATION_PATH path:

.. code-block:: console

  echo $_CIOP_APPLICATION_PATH

.. code-block:: console-output

  /application

* Sometimes the Hands-On refer to the variable *$HOSTNAME*. To obtain its value type:

.. code-block:: console

  echo $HOSTNAME

The output will be similar to:

.. code-block:: console-output

  sb-xx-xx-xx-xx.lab.terradue.int

Install additional software
^^^^^^^^^^^^^^^^^^^^^^^^^^^

* You can install the software you need by using the *yum* command since the user *<sandbox_user>* has sudo privileges for *yum*:

.. code-block:: console

 sudo yum install <package name>
 
.. NOTE::
  As the exercises progress and you gain more familiarity with the CIOP framework, the Hadoop and the MapReduce, we provide fewer step by step instructions. You feel free to ask to us for explainations or doubts using our Support Site https://support.terradue.com. We'll be happy to help !

.. [#f1] Pseudo-distributed mode is a method of running Hadoop whereby all Hadoop daemons run on the same machine. It is a cluster consisting of a single machine. It works just like a larger cluster, the only key difference (apart from the speed, of course !) being that the block replication factor is set to 1 (normally in a Hadoop Cluster the blocks on HDFS have a replication factor of 3). 

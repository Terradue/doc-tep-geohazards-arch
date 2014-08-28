Processing nodes & parallelism
==============================

As introduced in the workflow section, the processing nodes are the edges of a Directed Acyclic Graph and they can be run in parallel.

This section explains what can be done within a processing node.

The processing node can be executed as several processing tasks or a single processing task.

While the single processing task doesn't change the understanding of the workflow where a node will process a single task, an example of a node breaking down into several processing tasks is show below.

Several processing tasks
************************

In the previous :doc:`workflow example <workflow>`: 

.. uml::

   !define DIAG_NAME Workflow example

   !include includes/skins.iuml

   skinparam backgroundColor #FFFFFF
   skinparam componentStyle uml2

  start

  :Node A;

  fork
    :Node B;
  fork again
    :Node C;
  end fork
    :Node D;

  stop

Let's say Node A and Node C break-down into several processing task.

Node A is executed as:

.. uml::

  !define DIAG_NAME Node A breakdown

  !include includes/skins.iuml

  skinparam backgroundColor #FFFFFF
  skinparam componentStyle uml2
   
  fork
    :Task A.1;
  fork again
    :Task A.2;
  fork again
    :...;
  fork again
    :Task A.n;
  end fork

The complete workflow is executed as:

.. uml::

  !define DIAG_NAME Workflow example

  !include includes/skins.iuml

  skinparam backgroundColor #FFFFFF
  skinparam componentStyle uml2

  start

  fork
    :Task A.1;
  fork again
    :Task A.2;
  fork again
    :...;
  fork again
    :Task A.n;
  end fork

  fork
    :Task B;
  fork again
    fork
      :Task C.1;
    fork again
      :Task C.2;
    fork again
      :...;
    fork again
      :Task C.n;
    end fork
  end fork
    :Task D;

  stop
    
.. tip::
   There two levels of parallelism:
      * The first is at workflow level where two nodes can run concurrently (fork and join)
      * The second is at node level where the execution can be split in several tasks, each processing a subset of the inputs 
      

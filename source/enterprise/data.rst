Data sources
============

A processing workflow is a data pipeline. How does the data reach the data pipeline? 

There are several approaches to provide data to the data pipeline:

* A local file containing the inputs as references to data or values (one per line)
* A list of comma-separated values containing the inputs as references to data or values
* A reference to a catalogue 

Local file 
**********

This approach is very useful during the early stages of the application development where you download a few files to your sandbox and use these data to run the first tests.

.. note:: 
  We do not recommend using this method beyond the early stages of the application development.

Comma-separated values 
**********************

On the one hand, this approach is very straigh-forward to test the application against a small number of values. 
On the other, during the exploitation phase with an application exposed as an OGC WPS service, the comma-separated values list is very well managed and allows clients to provide several values to the application.

Reference to a catalogue
************************

This approach allows tapping on large repositories of Earth Observation data exposing an OpenSearch catalogue. 
It is the preferred option to process large datasets and to expose catalogue queriable in the application Web Processing Service interface.


.. tip:: 
  For details on how to implement this, read :doc:`Application descriptor reference </reference/application/index>`

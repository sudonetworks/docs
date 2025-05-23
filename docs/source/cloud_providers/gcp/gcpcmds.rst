===================
Useful GCP Commands
===================

.. note::
   
   This is not an exhaustive complete list. This list as the name implies a list of commands I have found to be useful. 

   As my studies and use of GCP goes this list may grow as the my knowledge grows. Please use to create your own. 

.. glossary::
   
   gcloud
    This command is the root of all GCP CLI commands. command-line interface is the primary CLI tool to create and manage Google Cloud resources. You can use this tool to perform many common platform tasks either from the command line or in scripts and other automations.

   gsutil
    a python application that lets you acces Google Cloud Storage from command line.

.. code::
   
   To start an instance or multiple instances use the following:

   gcloud compute instances start <INSTANCE-NAME> <INSTANCE-NAME2>

   --async can be used to return immediately w/o waiting for operations to complete.
   --verbose adjusts logging output. 

.. code::

   To get a list of zones:

   gcloud compute zones list


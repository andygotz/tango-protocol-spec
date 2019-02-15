Tango Controls system
---------------------

:status:`draft`

Goal
----

Goal of this document is to describe top-level semantics and qualities of Tango Controls System

.. glossary::

   Tango Controls System

      Tango Controls system consists of set of
      * `device_servers`
      * `clients`

      Tango Controls System MUST:
      * be object oriented
      * be based on client-server architecture
      * allow for micro-services architecture


      .. code-block:: abnf

         tango_controls_system = *device_server *client [tango_database] [access_control]

         device_server = [admin_device] *device

         tango_database = device ;where device class

         access_control = ; where

         admin_device = device





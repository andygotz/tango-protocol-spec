Tango Controls system
---------------------

:status:`draft`

Goal
----

Goal of this document is to describe top-level semantics and qualities of Tango Controls System

.. glossary::

   Tango Controls System

      Tango Controls system consists of set of

      * Device Servers (`device_server`)
      * Clients (`client`)

      Tango Controls System:

      * MUST be object oriented
      * MUST be based on client-server architecture
      * MUST be based on concept of :term:`Device`
      * MAY be based on micro-services architecture

      Below is a formal definition of the Tango Controls System. The datai

      .. code-block:: abnf

         ; Tango Control System consists of set of device_servers and clients applications
         tango_controls_system = *device_server *client [tango_database] [access_control]

         ; Device Server instantiate admin_devcie and other devices
         device_server = admin_device *device

         tango_database = device ;where device is providing functionality of Tango Database

         access_control = device ;where device provides functionality to manage access to Tango Controls System

         admin_device = device ;where device provided functionality to manage a device_server it belongs to and devices instantiated by this device_server





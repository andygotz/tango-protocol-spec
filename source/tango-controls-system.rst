Tango Controls System
=====================

:status:`draft`

Goal
----

This document describes top-level semantics and qualities of Tango Controls System.

Definition
----------

.. glossary::

   Tango Controls System

      Tango Controls System SHALL allow to remotely control and monitor devices and systems by means of computer
      workstations, servers and network.
      It SHALL allow to read and write so-called process variables as well as monitor and influence
      state of devices and systems. It SHALL also provide monitoring and management of itself.

      Tango Controls system consists of sets of:

      * Device Servers (`device_server`)
      * Clients (`client`)

      Tango Controls System:

      * MUST be object-oriented
      * MUST implement the client-server architecture
      * MUST be based on concept of :term:`Device`
      * MAY be based on the micro-services architecture

      Below is a formal definition of the Tango Controls System.

      .. code-block:: abnf

         ; Tango Control System consists of set of device_servers and clients applications
         tango_controls_system = *device_server *client [tango_database] [access_control]

         ; Device Server instantiate admin_devcie and other devices
         device_server = admin_device *device

         tango_database = device ;where device provides functionality of Tango Database

         access_control = device ;where device provides functionality to manage access to Tango Controls System

         admin_device = device ;where device provides functionality to manage a device_server it belongs to and devices instantiated by this device_server



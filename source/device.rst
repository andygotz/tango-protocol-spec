Device
======

Goal
----

This document describes the core concept of Tango Controls which is `Device`.


Definition
----------

.. glossary::

   Device
       A Device is an object within the Tango Controls System. The Device SHALL be accessible locally and remotely through
       its interface.

       Before accessign the Device it SHALL be created by/within a :term:`Device Server`...

       The Device has `device_name`. `device_name` is a character string which SHALL uniquely identify the device within
       the system :term:`Tango Controls System`.

       .. todo::
          Extend the above (device cration, life, deletion), formal specification of device name as domain/subdomain/device, ...

       Device SHALL provide way to read its:

       * `device_name`
       * `description`
       * `device_info`



       Device SHALL implement an interface to interact with its:

       * :term:`Attributes <Attribute>` as `device_attributes_interface`
       * :term:`Pipes <Pipe>` as `device_pipes_interface`
       * :term:`Commands <Command>` as `device_commands_interface`
       * :term:`Properties <Properties>` as `device_properties_interface`
       * :term:`Polling system <Polling>` as `device_polling_interface`
       * :term:`Events system <Events>` as `device_events_interface`

       .. code-block:: abnf

          ; device object description
          device = device_name [device_description] device_class device_state device_status admin_device

                   device_ping_interface device_blackbox_interface device_info_interface

                   device_attributes_interface device_commands_interface device_pipes_interface device_properties_interface

                   device_polling_interface device_events_interface

       `device_attributes_interface` SHALL allow for the following operations:

       * `query_device_attributes_list`

         .. code-block:: abnf

            query_device_attributes_list = C:get_device_attributes_list (S:device_attributes_list | S: tango_exception)







   Attribute

        An attribute is a concept related to process variables. It provides real-time data value of specified datatype

        .. code-block:: abnf

           attribute = attribute_config attribute_value attribute_dim



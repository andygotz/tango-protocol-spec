
Device
======

Goal
----

Goal of this document is to describe Tango Controls terminology related to device concept.



.. glossary::

   Device
       A Device is an object within Tango Controls system. Device SHELL be accessible locally and remotely through
       its interface.

       The Device has `device_name`. `device_name` is a character string which SHELL uniquely identify the device within
       the system :term:`Tango Controls System`. TO-DO: peci

       Device SHELL provide way to read its:
       * `device_name`
       * `description`
       * `device_info`

       Device MUST provide information on its dev

       Device SHELL implement an interface to interact with its:

       * :term:`Attributes <Attribute>` as `attributes_interface`
       * :term:`Pipes <Pipe>` as `pipes_interface`
       * :term:`Commands <Command>` as `commands_interface`
       * :term:`Properties <Properties>` as `properties_interface`
       * :term:`Polling system <Polling>` as `polling_interface`
       * :term:`Events system <Events>` as `events_interface`

       .. code-block:: abnf

          ; device object description
          device = device_name [device_description] device_class device_state device_status admin_device

                   ping_interface blackbox_interface device_info_interface

                   attributes_interface commands_interface pipes_interface properties_interface

                   polling_interface events_interface


       `ping_interface` is


   Attribute
        .. code-block:: abnf

           attribute = attribute_config attribute_value attribute_dim

           attribute_interface
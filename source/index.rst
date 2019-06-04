.. Tango Controls Protocol Sepcification documentation master file, created by
   sphinx-quickstart on Thu Feb 14 15:40:00 2019.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to Tango Controls Protocol Specification's documentation!
=================================================================

:status:`draft, WIP`

Goal
----

This documentation aims to describe Tango Controls Protocol formally.

It SHALL provide a level of details which is enough to implement the Tango Controls Protocol on top of any suitable
transport layer.

To rich the goal, it SHALL describe semantic and behaviour of Tango Controls System's actors, objects
and concepts. The specification MUST define specific data structures as well.

The central concept of Tango Controls is :term:`Device` and the Tango Controls Protocol MUST provide marshalling
of :term:`Device` objects. However, it SHALL not specify data structures serialisation as this belongs to
a transport layer.

Preamble
--------

.. todo::

   Add references to RFCs

.. toctree::
   :maxdepth: 1
   :caption: Contents:

   tango-controls-system
   device
   device-server



Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

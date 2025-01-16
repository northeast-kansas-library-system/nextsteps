.. include:: /include.rst

Staff account types
===================

Koha staff account types
------------------------

There are 10 basic Koha account types in Next Search Catalog:

- :ref:`superlibrarian_permissions`
- :ref:`director_permissions`
- :ref:`director_limited`
- :ref:`tech_permissions`
- :ref:`tech_limited`
- :ref:`circ_permissions`
- :ref:`aide_permissions`
- :ref:`outreach_permissions`
- :ref:`sco_permission`
- :ref:`sci_permission`

You can find more information about staff permissions in the `permissions section of the Koha manual <https://koha-community.org/manual/latest/en/html/patrons.html#patron-permissions>`_

.. _superlibrarian_permissions:

Superlibrarian
--------------

- Superlibrarians have access to all system functions and are reserved for NEKLS staff

.. _director_permissions:

Director
--------

These accounts are assigned to library directors and give them the ability to change passwords for other library staff.

- Library directors have the ability to

  - log into the staff interface
  - check in and check out materials
  - manage borrower account restrictions
  - override blocked renewals
  - add, modify, and delete borrower accounts
  - view borrower information
  - place and modify requests for borrowers
  - create and edit bibliographic records
  - create and edit item records
  - manage borrower fees
  - manage borrower suggestions
  - export and import bibliographic records
  - use the item batch deletion and batch modification tools
  - create and print labels
  - manage borrower lists
  - manage rotating collections
  - upload files and cover images
  - access the inventory tools
  - moderate borrower comments
  - moderate borrower tags
  - execute reports
  - create and edit clubs
  - enroll borrowers in clubs
  - manage the library's calendar
  - set notice/status triggers
  - manage staff passwords

.. _director_limited:

Director (limited)
--------

These accounts are assigned to library directors and give them the ability to change passwords for other library staff.

Essentially these accounts are exactly like the regular director accounts, just without the ability to add or edit bibliographic records.  These accounts are usually given to new directors that have not yet had cataloging training.

- Library directors have the ability to

  - log into the staff interface
  - check in and check out materials
  - manage borrower account restrictions
  - override blocked renewals
  - add, modify, and delete borrower accounts
  - view borrower information
  - place and modify requests for borrowers
  - create and edit item records
  - manage borrower fees
  - manage borrower suggestions
  - export and import bibliographic records
  - use the item batch deletion and batch modification tools
  - create and print labels
  - manage borrower lists
  - manage rotating collections
  - upload files and cover images
  - access the inventory tools
  - moderate borrower comments
  - moderate borrower tags
  - execute reports
  - create and edit clubs
  - enroll borrowers in clubs
  - manage the library's calendar
  - set notice/status triggers
  - manage staff passwords

.. _tech_permissions:

Technical services (full permission)
------------------------------------

These accounts have the ability to catalog materials, add and edit item records, run reports, add and edit patron records, accept fee payments, and circulate materials.

- Technical services staff have the ability to:

  - log into the staff interface
  - check in and check out materials
  - manage borrower account restrictions
  - override blocked renewals
  - add, modify, and delete borrower accounts
  - view borrower information
  - place and modify requests for borrowers
  - create and edit bibliographic records
  - create and edit item records
  - manage borrower fees
  - manage borrower suggestions
  - export and import bibliographic records
  - use the item batch deletion and batch modification tools
  - create and print labels
  - manage borrower lists
  - manage rotating collections
  - upload files and cover images
  - access the inventory tools
  - moderate borrower comments
  - moderate borrower tags
  - execute reports
  - create and edit clubs
  - enroll borrowers in clubs

.. _tech_limited:

Technical services (limited permission)
------------------------------------

These accounts have the ability to add and edit item records, run reports, add and edit patron records, accept fee payments, and circulate materials.

These accounts are exactly like the "Technical services (full permission)," just without the ability to add or edit bibliographic records.  These accounts are usually given to new technical services staff that have not yet had cataloging training or staff that need the ability to add or edit items but are not given the ability to do more advanced cataloging work.

- Technical services staff have the ability to:

  - log into the staff interface
  - check in and check out materials
  - manage borrower account restrictions
  - override blocked renewals
  - add, modify, and delete borrower accounts
  - view borrower information
  - place and modify requests for borrowers
  - create and edit item records
  - manage borrower fees
  - manage borrower suggestions
  - export and import bibliographic records
  - use the item batch deletion and batch modification tools
  - create and print labels
  - manage borrower lists
  - manage rotating collections
  - upload files and cover images
  - access the inventory tools
  - moderate borrower comments
  - moderate borrower tags
  - execute reports
  - create and edit clubs
  - enroll borrowers in clubs

.. _circ_permissions:

Circulation
-----------

These accounts have the ability to run reports, add and edit patron records from any library, accept fee payments, sand circulate materials.

These accounts have the ability to accept fee payments; add and edit patron records; check out materials to library card holders from any library; check in materials; search the catalog; and place requests on materials for borrowers.

- Circulation staff have the ability to;

  - log into the staff interface
  - check in and check out materials
  - manage borrower account restrictions
  - override blocked renewals
  - add, modify, and delete borrower accounts
  - view borrower information
  - place and modify requests for borrowers
  - manage borrower fees
  - access the inventory tools
  - moderate borrower comments
  - moderate borrower tags
  - execute reports
  - enroll borrowers in clubs

.. _aide_permissions:

Aide
----

These accounts have the ability to check out materials to library card holders from any library; check in materials; search the catalog; and place requests on materials for borrowers.

- Aide accounts have the ability to

  - log into the staff interface
  - check in and check out materials
  - place requests for borrowers

.. _outreach_permissions:

Outreach
--------

Outreach accounts are created for allowing staff or volunteers to check materials in and out while working at locations outside of the library. 

These accounts have the ability to check out materials to library card holders whose home library matches the outreach account library; check in materials; search the catalog; and place requests on materials for borrowers.

- Outreach accounts have the ability to

  - log into the staff interface
  - check in and check out materials
  - place requests for borrowers

.. _sco_permission:

Self check-out
-------------

- Self check-out accounts have the ability to log into the self check-out module via the Koha OPAC

  - No other accounts have the ability to log into the self check-out module

  - NEKLS strongly recommends having 1 self check-out account per self check-out machine - this allows library staff to see circulation statistics for each separate self check-out machine

.. _sci_permission:

Self check-in
-------------

- Self check-in accounts have the ability to log into the self check-in module via the Koha OPAC

  - No other accounts have the ability to log into the self check-in module

  - NEKLS strongly recommends having 1 self check-in account per self checkin machine - this allows library staff to see circulation statistics for each separate self check-out machine
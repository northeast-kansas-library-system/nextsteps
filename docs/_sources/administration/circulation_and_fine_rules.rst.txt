.. include:: /include.rst

****************************************
Circulation, late fee, and request rules
****************************************

Circulation and late fee rules
==============================

Circulation and late fee rules are defined by these criteria:

1. The rules at **the library where the item is being checked out**
2. The borrower category of the account checking the materials out 
3. The item type of the item being checked out 

Collection codes, call numbers, shelving locations, etc. have no bearing on any lending, fee, or request policies.

Because Next Search Catalog has 54 library locations; 39 borrower categories; and 60 item types, this means that there are potentially 134200 circulation rules in our system.  Currently there are approximately 2250 active rules.

Rules are applied from most specific to less specific, using the first found in this order:

  ^ **same** library, **same** patron category, **same** item type
  - **same** library, **same** patron category, all item types
  - **same** library, all patron categories, **same** item type
  - **same** library, all patron categories, all item types
  - default (all libraries), **same** patron category, **same** item type
  - default (all libraries), **same** patron category, all item types
  - default (all libraries), all patron categories, **same** item type
  - default (all libraries), all patron categories, all item types

So if the circulation rules follows these examples:

+---------------+--------------+----------------+-----------------+
| Library       | Category     | Item type      | CKO Rule        |  
+===============+==============+================+=================+
| MY_LIBRARY    | ADULT        | VIDEO          | 3 day checkout  |  
+---------------+--------------+----------------+-----------------+
| MY_LIBRARY    | HOMEBOUND    | ALL            | 28 day checkout |  
+---------------+--------------+----------------+-----------------+
| MY_LIBRARY    | ALL          | GAME           | 7 day checkout  |  
+---------------+--------------+----------------+-----------------+
| MY_LIBRARY    | ALL          | ALL            | 21 day checkout |  
+---------------+--------------+----------------+-----------------+
| ALL_LIBRARIES | ADULT_OTHER  | MUSIC CD       | 12 day checkout |  
+---------------+--------------+----------------+-----------------+
| ALL_LIBRARIES | DIGITAL ONLY | ALL            | 0 day checkout  |  
+---------------+--------------+----------------+-----------------+
| ALL_LIBRARIES | ALL          | (Unclassified) | 0 day checkout  |  
+---------------+--------------+----------------+-----------------+
| ALL_LIBRARIES | ALL          | ALL            | 21 day checkout |  
+---------------+--------------+----------------+-----------------+

An ADULT at MY_LIBRARY checking out a VIDEO will follow the most specific rule at the top of the table because the Library, Category, and Item type all match.

A MINOR at MY_LIBRARY checking out a VIDEO will follow the "MY_LIBRARY, ALL, ALL" rule in the 4th row down (i.e the item will check out for 21 days) because there is no specific rule that matches MY_LIBRARY: MINOR : VIDEO. 

If a MY_LIBRARY : ALL : ALL rule is set for each library, the ALL_LIBRARIES only serve as backups in case of a software problem.

Request rules
=============

Request rules are defined by these criteria:

1. The rules at **the library that owns the item**
2. The borrower category of the account checking the materials out 
3. The item type of the item being checked out 

Request rules follow the same priority criteria as circulation and fee rules.

So if the request rules follows these examples:

+---------------+--------------+----------------+----------------+
| Library       | Category     | Item type      | Request        |
|               |              |                | Rules          |
+===============+==============+================+================+
| MY_LIBRARY    | ADULT        | LAPTOP         | LOCAL REQUEST  |
|               |              | COMPUTER       | ONLY           |
+---------------+--------------+----------------+----------------+
| MY_LIBRARY    | HOMEBOUND    | ALL            | Allowed        |
+---------------+--------------+----------------+----------------+
| MY_LIBRARY    | ALL          | SPECIAL        | NO REQUESTS    |
|               |              | COLLECTIONS    | ALLOWED        |
+---------------+--------------+----------------+----------------+
| MY_LIBRARY    | ALL          | ALL            | Allowed        |
+---------------+--------------+----------------+----------------+
| ALL_LIBRARIES | ADULT_OTHER  | MUSIC CD       | Allowed        |
+---------------+--------------+----------------+----------------+
| ALL_LIBRARIES | DIGITAL ONLY | ALL            | No requests    |
|               |              |                | allowed        |
+---------------+--------------+----------------+----------------+
| ALL_LIBRARIES | ALL          | (Unclassified) | Allowed        |
+---------------+--------------+----------------+----------------+
| ALL_LIBRARIES | ALL          | ALL            | Allowed        |
+---------------+--------------+----------------+----------------+

If an ADULT at YOUR_LIBRARY tries request a LAPTOP COMPUTER, to have it shipped to YOUR_LIBRARY they will not be able to request that item from MY_LIBRARY because the request rules for LAPTOPs at MY_LIBRARY only allow for those items to be picked up at MY_LIBRARY.

And no one can place a request on SPECIAL COLLECTIONS materials at MY_LIBRARY.

Circulation, late fee, request rules matrix
===========================================

General rules
-------------

.. include:: \administration\circulation_and_fine_rules\matrix_library.rst 





Item type
^^^^^^^^^


Note 
^^^^


Circulation rules
-----------------


Current checkouts allowed
^^^^^^^^^^^^^^^^^^^^^^^^^


Current on^site checkouts allowed
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^


Loan period
^^^^^^^^^^^


Days mode
^^^^^^^^^


Unit 
^^^^


Hard due date
^^^^^^^^^^^^^


Decreased loan period for high holds (day)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^


Late fee and suspension rules
-----------------------------


Fine amount
^^^^^^^^^^^


Fine charging interval
^^^^^^^^^^^^^^^^^^^^^^


When to charge
^^^^^^^^^^^^^^


Fine/suspension grace period
^^^^^^^^^^^^^^^^^^^^^^^^^^^^


Overdue fines cap (amount)
^^^^^^^^^^^^^^^^^^^^^^^^^^


Cap fine at replacement price
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Suspension in days (day)
^^^^^^^^^^^^^^^^^^^^^^^^


Max. suspension duration (day)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^


Suspension charging interval
^^^^^^^^^^^^^^^^^^^^^^^^^^^^


Renewal rules
-------------


Renewals allowed (count)
^^^^^^^^^^^^^^^^^^^^^^^^


Renewal period
^^^^^^^^^^^^^^


No renewal before
^^^^^^^^^^^^^^^^^


No automatic renewal before
^^^^^^^^^^^^^^^^^^^^^^^^^^^


Automatic renewal
^^^^^^^^^^^^^^^^^


No automatic renewal after
^^^^^^^^^^^^^^^^^^^^^^^^^^


No automatic renewal after (hard limit)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^


Request rules
-------------


Holds allowed (total)
^^^^^^^^^^^^^^^^^^^^^

Holds allowed (daily)
^^^^^^^^^^^^^^^^^^^^^


Holds per record (count)
^^^^^^^^^^^^^^^^^^^^^^^^


On shelf holds allowed
^^^^^^^^^^^^^^^^^^^^^^


OPAC item level holds
^^^^^^^^^^^^^^^^^^^^^


Holds pickup period (day)
^^^^^^^^^^^^^^^^^^^^^^^^^


Rental discount rules
---------------------


Rental discount (%)
^^^^^^^^^^^^^^^^^^^

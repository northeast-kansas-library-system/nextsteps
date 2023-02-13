.. include:: /include.rst

*Withdrawn* status
==================

Current withdrawn statuses
^^^^^^^^^^^^^^^^^^^^^^^^^^

There are several withdran statuses at the present time:

- Discard
- Withdrawn
- Lost - Not Returnable 

Depending on which library you are working at, you may not see all of these statuses.

Automatic deletion of "Withdrawn" items
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

13 month after setting an item to any of these statuses, the item will be automatically deleted from the catalog.

Seting a *withdrawn* status
^^^^^^^^^^^^^^^^^^^^^^^^^^^

|item_status_withdrawn_0010.png|

|item_status_withdrawn_0020.png|

Discard 
^^^^^^^

Used to mark a specific item as withdrawn - available to all libraries. (This status is being phased out because it has the exact same effect as "Withdrawn")

Withdrawn 
^^^^^^^^^

Used to mark a specific item as withdrawn - available to all libraries.


Lost - not returnable 
^^^^^^^^^^^^^^^^^^^^^

This is a special status used only by Ottawa Library.

What happens at check-in
^^^^^^^^^^^^^^^^^^^^^^^^

When you check in an item that has a "Withdrawn" status:

#. The item is not supposed to be chcked in (i.e. if it was checked out to a borrower when it was marked with a withdrawn status, the item should remain on the borrowers account - but there are some software bugs and this is sometimes an issue)
#. The withdrawn status **is not** removed
#. The item's shelving location is temporarily updated to "Recently returned" 
#. A check-in messages appears ths should be similar to this:

  |item_status_withdrawn_0030.png| 

Known bugs 
^^^^^^^^^^

There are some known bugs involved with checkin in items having a withdrawn status and the Koha community is working to resolve these issues.  Specifically, the item shelving location should not be updated to "Recently returned" and, if the item was withdrawn while checked out to a borrower, it should not be removed from the borrower's account.

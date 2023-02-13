.. include:: /include.rst

*In transit* status
===================

Current in transit statuses
^^^^^^^^^^^^^^^^^^^^^^^^

- In transit 
- In transit on hold

The only way to tell the difference is to read the message in the status column on the item record:

|item_status_in_transit_0010.png|

|item_status_in_transit_0020.png|

Seting an *in transit* status
^^^^^^^^^^^^^^^^^^^^^^^^^

The in transit process is automatic.  An item with a request for pickup at another library, or an item that needs to be shipped back to its owning library will automatically go into transit when you check it in.

What happens at check-in
^^^^^^^^^^^^^^^^^^^^^^^^

When you check in an item that has needs to be shipped to another library:

#. The item is checked in from the borrower's account (if it's checked out)
#. The items' last seen date is updated 
#. The item's shelving location is temporarily updated to "Recently returned"
#. A check-in message and a damaged message should appear that should be similar to this - if the item does not have any requests:

  |item_status_in_transit_0030.png| 

5. Or like this - if the item is being shipped to fill a requests:

  |item_status_in_transit_0040.png| 
.. include:: /include.rst

#############
21.11 Upgrade
#############

********
Overview
********

Koha 21.11 was released by the Koha Community in November of 2021.

The official release notes for this version are at `<https://koha-community.org/koha-21-11-released/>`_

There are very few changes in this upgrade that will affect Next Search Catalog staff.


**********************************
Clearing the cache on your browser
**********************************

.. toctree::
   :glob:
   :maxdepth: 2

   /upgrades/upgrade_clear_cache

*************************************************
Changes to "Check out" search and "Patron search"
*************************************************

The only significant change that staff will see in this verion of Koha is a change to the "Check out" search and the "Patron search."

The reason that this is a significant difference is because there is a bug that will prevent staff using an "Aide" account from doing a "Check out" search using the borrower's name insead of their card number.  I have written several work-arounds for this bug but it is possible that some staff using an "Aide" account might run into difficulties, so please contact nexthelp@nekls.org if you notice any problems searching for borrowers by name.

- In older versions of Koha, there is a difference between a "Check out" search and a "Search patrons" search.

|unified.search.0010|

|unified.search.0020|

|unified.search.0030|

In the new version of Koha, both search boxes execute the same search and the results will look more like the old "Patron search" with a few exceptions.

- The borrower's card number will provide a link to the borrower's "Check out" page
- The borrower's name will provide a link to the borrower's "Details" page
- If you are logged in at the borrower's home library, the borrower's home library in the results list will be highlighted

|unified.search.0040|

Significance of this change - possible bug issues
-------------------------------------------------

The reason that this is a significant difference is because there is a bug that will prevent staff using an "Aide" account from doing a "Check out" search using the borrower's name insead of their card number.  I have written several work-arounds for this bug but it is possible that some staff using an "Aide" account might run into difficulties, so please contact nexthelp@nekls.org if you notice any problems searching for borrowers by name.

*************
Other changes
*************

There are some other changes that are even more minor than this minor change.  There is also a feature that is not enabled yet that George will discuss at the August 30 Next Search Catalog meeting.

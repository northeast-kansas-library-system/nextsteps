.. include:: /include.rst

#############
22.05 Upgrade
#############

We will be upgrading to Koha 22.05 soon.  Here are the new features Next Search Catalog staff need to be aware of.

OPAC
====

Changes to the suggestion form
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Can search for title details in Google Books by entering ISBN 
2. Limit on itemtypes 
3. Fewer fields on the page 

Holds history in the OPAC 
^^^^^^^^^^^^^^^^^^^^^^^^^

1. Holds history is now available in the OPAC 
2. Patrons can delete their own holds history 
3. Holds history and reading history are both tied to patron privacy 
  - If a patron has their reading history set to "Previous 13 months" their reading **and holds** history will be kept for the previous 13 months 
  - If a patron has their reading history set to "Never" their reading **and holds** history will be deleted as soon as they return items they've checked out 

OPACMySummaryNote
^^^^^^^^^^^^^^^^^

HTML from this system preference currently appears on a patron's "My summary" page in the OPAC.  Beginning in 22.05, this will be moved to the library customizations area and it will be able to be modified on a library-by-library basis.  If you would like to have this message customized for your libary, please contact nexthelp@nekls.org.

OPAC and Staff interface
========================

Edit advanced searches 
^^^^^^^^^^^^^^^^^^^^^^

1. Go to advanced search 
2. Set some search parameters
2. From the results page click on "Edit search" (in the OPAC click on "Return to the last advanced search")
3. All of the options you selected in step 2 will remain set

Hold expiration dates vs hold pickup expiration 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This fixes a long standing problem.  When you place a request, Koha sets a "Hold expiration date" (called a "Not needed after" date in the OPAC).  When the item arrives and gets set on the hold shelf, this date is updated to reflect the date that the item's time on the hold shelf will expire.

The bugginess of this situation comes into play when a patron arrives to pick up a request and the item is not on the hold shelf where it's supposed to be.  If staff rever the request from "Waiting" to "Pending" the expiration date remains the date that was set when the item was placed on the hold shelf.

In the new version this one date field has been split into a "Hold expiration date" and a "Pickup expiration date."  This should solve this problem.

Hold start and end dates will be required 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Currently a hold's start date is automatically filled in when a request is placed.  An expiration date is not required.  We use custom code to set a hold expiration date when a request is placed.  However, if a staff member or a borrower deletes the expiration date, the request can still be placed.

In Koha 22.05, an expiration date will be required.



Staff interface
===============

Send "Password reset" and "Welcome" email directly from the staff client 

1. Go to a borrower's account 
2. Click on the "More" drop down button 
3. Select "Send welcome email" or "Send password reset" as needed 

Direct links built into some reports
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Some fields will be direct linked in Koha reports.  This means that the data will be linked to the record in the report results and fully downloadable if you export the data to Excel.

Changes in how patron "Notices" are rendered
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Unfortunately, many of our notices contain custom css inside of the notice, so the notices don't render well.  We're working on fixing this problem by building an external custom CSS sheet to style notices outside of the notice itself.

Automatic item modifications by age enhancement
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

We have several item modifications set up that run automatically.  Up until now all modifications happen based on the item's dateaccessioned.  After the upgrade, other date fields can be used to control modifications.

  - items.dateaccessioned
  - items.replacementpricedate
  - items.datelastborrowed
  - Items.datelastseen
  - items.damaged_on
  - items.itemlost_on
  - items.withdrawn_on

If you would like a modification to happen to items in your collection based on any of these dates, please ask for more information.




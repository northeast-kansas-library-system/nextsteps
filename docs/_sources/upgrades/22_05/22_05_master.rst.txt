.. include:: /include.rst

#############
22.05 Upgrade
#############

We will be upgrading to Koha 22.05 soon.  Here are the new features Next Search Catalog staff need to be aware of.

Staff interface
===============

Send "Password reset" and "Welcome" email directly from the staff client
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Go to a borrower's account
2. Click on the "More" drop down button
3. Select "Send welcome email" or "Send password reset" as needed

    |email_enhancement_0010|

Changes in how patron "Notices" are rendered
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

A borrower's sent messages will be displayed differently after the upgrade.

1. Go to a borrower's account
2. Click on the "Notices" tab
3. Click on the title of a notice

  - Before - message content appears inside of table

    |notices_enhancement_0010|

  - After - message content appears in pop-up

    |notices_enhancement_0020|

4. Note the position of the "Resend" button

  - Before - resend button appears inside of table

    |notices_enhancement_0030|

  - After - resend button appears in pop-up

    |notices_enhancement_0040|

5. Bug issue

  - By moving the message content into the pop-up, some of our older messages become invisible.  This is because we have many messages that have CSS inside of the message content.  We are working on putting the CSS into an external stylesheet so that the message content is always visible. We are also working on some jQuery to make the content on older notices visible whle we work on the CSS issue.

    |notices_enhancement_0050|

Direct links built into some reports
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The reports module has been enhanced to allow for built-in links to bibliographic, item, and borrower accounts.  This means that, in some reports, when you download the results as a .csv file, you will no longer see the raw URL data in the spreadsheet.

  - Before

    |reports_enhancement_0010|

  - After

    |reports_enhancement_0020|

    |reports_enhancement_0030|

    |reports_enhancement_0040|

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

One example of how this could be used would be to change the status of any item marked as "Damaged" to "Withrdawn" 90 days after the item is marked as "Damaged."  Another would be to automatically change the location of an item with a shelving location of "PAOLA Adult Display" back to "Adult" if the "datelastseen" is more than 60 days ago.  There are many possibilities.

If you would like a modification to happen to items in your collection based on any of these dates, please ask nexthelp@nekls.org for more information.

  - Before

    |age_enhancement_0010|

  - After

    |age_enhancement_0020|

OPAC and Staff interface
========================

Edit advanced searches
^^^^^^^^^^^^^^^^^^^^^^

1. Go to advanced search
2. Set some search parameters
2. From the results page click on "Edit search" (in the OPAC click on "Return to the last advanced search")
3. All of the options you selected in step 2 will remain set

  - Before

    |advanced_search_edit_0010|

  - After

    |advanced_search_edit_0020|

    |advanced_search_edit_0030|

Hold expiration dates vs hold pickup expiration
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This fixes a long standing problem.  When you place a request, Koha sets a "Hold expiration date" (called a "Not needed after" date in the OPAC).  When the item arrives and gets set on the hold shelf, this date is updated to reflect the date that the item's time on the hold shelf will expire.

The bugginess of this situation comes into play when a patron arrives to pick up a request and the item is not on the hold shelf where it's supposed to be.  If staff rever the request from "Waiting" to "Pending" the expiration date remains the date that was set when the item was placed on the hold shelf.

In the new version this one date field has been split into a "Hold expiration date" and a "Pickup expiration date."  This should solve this problem.

  - Before

    |hold_bug_0010|

    |hold_bug_0020|

    |hold_bug_0020|

  - After

    |hold_bug_0040|

    |hold_bug_0050|

    |hold_bug_0060|



Hold expiration dates will be required
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In Koha 22.05, an expiration date for new requests will be required.  The default expiration date is 1 year from the date the request is placed.

  - Before

    |hold_expiration_required_0010|

    |hold_expiration_required_0020|

  - after

    |hold_expiration_required_0030|



OPAC
====

Changes to the suggestion form
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Can search for title details in Google Books by entering ISBN
2. Limit on item types is improved
3. Fewer fields on the page

  - Before

    |suggestion_form_enhancement_0010|

  - After

    |suggestion_form_enhancement_0020|


Holds history in the OPAC
^^^^^^^^^^^^^^^^^^^^^^^^^

1. Holds history is now available in the OPAC
2. Patrons can delete their own holds history
3. Holds history and reading history are both tied to patron privacy
  - If a patron has their reading history set to "Previous 13 months" their reading **and holds** history will be kept for the previous 13 months
  - If a patron has their reading history set to "Never" their reading **and holds** history will be deleted as soon as they return items they've checked out

  - Before

    |holds_history_enhcancement_0010|

    |holds_history_enhcancement_0015|

  - After

    |holds_history_enhcancement_0020|

    |holds_history_enhcancement_0030|

    |holds_history_enhcancement_0040|

OPACMySummaryNote
^^^^^^^^^^^^^^^^^

HTML from this system preference currently appears on a patron's "My summary" page in the OPAC.  Beginning in 22.05, this will be moved to the library customizations area and it will be able to be modified on a library-by-library basis.  If you would like to have this message customized for your libary, please contact nexthelp@nekls.org.

  - After

    |summary_enhancement_0010|

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

- See `"Password reset" and "Welcome" email questions`_ below

Video on YouTube
^^^^^^^^^^^^^^^^

Watch **"Password reset" and "Welcome" email** on YouTube

.. only:: html

  .. raw:: html

        <div class="ytcontainer">
          <iframe class="responsive-iframe" src="https://www.youtube.com/embed/Hag1aoLTTQo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>

.. only:: latex

   https://youtu.be/Hag1aoLTTQo

|br|

Go directly to the video on YouTube `<https://youtu.be/Hag1aoLTTQo>`_

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

    |notices_enhancement_050|

Video on YouTube
^^^^^^^^^^^^^^^^

Watch **Notice rendering changes** on YouTube

.. only:: html

  .. raw:: html

        <div class="ytcontainer">
          <iframe class="responsive-iframe" src="https://www.youtube.com/embed/KopnRMjOo6M" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>

.. only:: latex

   https://youtu.be/KopnRMjOo6M

|br|

Go directly to the video on YouTube `<https://youtu.be/KopnRMjOo6M>`_

  
Direct links built into some reports
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The reports module has been enhanced to allow for built-in links to bibliographic, item, and borrower accounts.  This means that, in some reports, when you download the results as a .csv file, you will no longer see the raw URL data in the spreadsheet.

  - Before

    |reports_enhancement_0010|

  - After

    |reports_enhancement_0020|

    |reports_enhancement_0030|

    |reports_enhancement_0040|

Video on YouTube
^^^^^^^^^^^^^^^^

Watch **Direct links in reports** on YouTube

.. only:: html

  .. raw:: html

        <div class="ytcontainer">
          <iframe class="responsive-iframe" src="https://www.youtube.com/embed/dBOHk-r51no" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>

.. only:: latex

   https://youtu.be/dBOHk-r51no 

|br|

Go directly to the video on YouTube `<https://youtu.be/dBOHk-r51no >`_



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

Video on YouTube
^^^^^^^^^^^^^^^^

Watch **Automatic item modifications by age enhancement** on YouTube

.. only:: html

  .. raw:: html

        <div class="ytcontainer">
          <iframe class="responsive-iframe" src="https://www.youtube.com/embed/Y07lEcOob5A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>

.. only:: latex

   https://youtu.be/Y07lEcOob5A

|br|

Go directly to the video on YouTube `<https://youtu.be/Y07lEcOob5A>`_

OPAC and Staff interface
========================

Edit advanced searches
^^^^^^^^^^^^^^^^^^^^^^

1. Go to advanced search
2. Set some search parameters
3. From the results page click on "Edit search" (in the OPAC click on "Return to the last advanced search")
4. All of the options you selected in step 2 will remain set

  - Before

    |advanced_search_edit_0010|

  - After

    |advanced_search_edit_0020|

    |advanced_search_edit_0030|

Video on YouTube
^^^^^^^^^^^^^^^^

Watch **Edit advanced searches** on YouTube

.. only:: html

  .. raw:: html

        <div class="ytcontainer">
          <iframe class="responsive-iframe" src="https://www.youtube.com/embed/CD3bCW89OZs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>

.. only:: latex

   https://youtu.be/CD3bCW89OZs

|br|

Go directly to the video on YouTube `<https://youtu.be/CD3bCW89OZs>`_

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

- See `Hold expiration dates questions`_ below

Video on YouTube
^^^^^^^^^^^^^^^^

Watch **Hold expiration dates vs hold pickup expiration** on YouTube

.. only:: html

  .. raw:: html

        <div class="ytcontainer">
          <iframe class="responsive-iframe" src="https://www.youtube.com/embed/6bcra4lsaH0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>

.. only:: latex

   https://youtu.be/6bcra4lsaH0

|br|

Go directly to the video on YouTube `<https://youtu.be/6bcra4lsaH0>`_


Hold expiration dates will be required
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In Koha 22.05, an expiration date for new requests will be required.  The default expiration date is 1 year from the date the request is placed.

  - Before

    |hold_expiration_required_0010|

    |hold_expiration_required_0020|

  - after

    |hold_expiration_required_0030|

- See `Hold expiration dates questions`_ below

Video on YouTube
^^^^^^^^^^^^^^^^

Watch **Hold expiration dates will be required** on YouTube

.. only:: html

  .. raw:: html

        <div class="ytcontainer">
          <iframe class="responsive-iframe" src="https://www.youtube.com/embed/PUDEupNT52w" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>

.. only:: latex

   https://youtu.be/PUDEupNT52w

|br|

Go directly to the video on YouTube `<https://youtu.be/PUDEupNT52w>`_


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

Video on YouTube
^^^^^^^^^^^^^^^^

Watch **Changes to the suggestion form** on YouTube

.. only:: html

  .. raw:: html

        <div class="ytcontainer">
          <iframe class="responsive-iframe" src="https://www.youtube.com/embed/ta5O27-838Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>

.. only:: latex

   https://youtu.be/ta5O27-838Y

|br|

Go directly to the video on YouTube `<https://youtu.be/ta5O27-838Y>`_


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

- See `Hold history questions`_ below

Video on YouTube
^^^^^^^^^^^^^^^^

Watch **Holds history in the OPAC** on YouTube

.. only:: html

  .. raw:: html

        <div class="ytcontainer">
          <iframe class="responsive-iframe" src="https://www.youtube.com/embed/kx-E38Pd31s" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>

.. only:: latex

   https://youtu.be/kx-E38Pd31s

|br|

Go directly to the video on YouTube `<https://youtu.be/kx-E38Pd31s>`_

OPACMySummaryNote
^^^^^^^^^^^^^^^^^

After further testing this appears to have a bug and isn't working as expected.

|ss|
HTML from this system preference currently appears on a patron's "My summary" page in the OPAC.  Beginning in 22.05, this will be moved to the library customizations area and it will be able to be modified on a library-by-library basis.  If you would like to have this message customized for your libary, please contact nexthelp@nekls.org.
|se|

Questions from training sessions
================================

"Password reset" and "Welcome" email questions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Q: Can I edit the "Welcome" email for my library?

A: Yes, but you need to know HTML, CSS, and how to use Template Toolkit with Koha in order to really get any kind of result.  NEKLS staff can modify the "Welcome" email for your library if you would like not to have to deal with it.

-----

Q: What what does the "Welcome" email from my library say? 

A: NEKLS staff can send you a copy of the template being used by your library if you ask at nexthelp@nekls.org.

-----

Hold expiration dates questions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Q: Can you revert a hold when an item is "In transit"

A: No.  "In transit" is a special circumstance in Koha and, well, there are a lot of things you can't do to an item while it's in transit from one library to another.

-----

Hold history questions 
^^^^^^^^^^^^^^^^^^^^^^

Q: If a borrower deletes their holds history; or their checkout history; or sets their privacy rule to "Never," can staff still see their history?

A: No.  If a borrower deletes any of their history or sets their privacy rule to "Never," that data is removed from the staff interface and the OPAC.

-----

Q: What if a I have an item that was damaged by the last borrower but their history has been deleted?

A: No matter what else is done, the item record always remembers the last borrower.  "Borrower checkout history" and "Borrower hold history" are stored in one place in the database.  Separately in the item record, the item remembers the last borrower the item was checked out to.

-----

Q: What if the checkout history has been deleted and the item was damaged by a patron who had it 5 patrons ago.

A: The best practice is to check items to make sure all of the pieces have been returned and that there is no damage **before** you check the items in.  If you take care of damaged items and missing pieces before the item is checked in, you know exactly who the item was checked out to because it's still checked out to them.

-----

Mega-video on YouTube
=====================

Watch **See the full Koha 22.05 video (contains all other videos spliced together)** on YouTube

.. only:: html

  .. raw:: html

        <div class="ytcontainer">
          <iframe class="responsive-iframe" src="https://www.youtube.com/embed/c10IJhexDqE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>

.. only:: latex

   https://youtu.be/c10IJhexDqE

|br|

Go directly to the video on YouTube `<https://youtu.be/c10IJhexDqE>`_

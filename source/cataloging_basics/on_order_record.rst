.. include:: /include.rst

On order record cataloging
==========================

Some libraries add "On order" records to the catalog when they order new titles.  This allows borrowers to place requests on titles before they are published.

1. First search to see if the title has already been added as an "On order" record already 

    If a record already exists, go to step 4

    :doc:`See the searching best practices for help in searching for a bibliographic record </cataloging_basics/search_for_existing_record>`

2. If the title can not be found, find or create a bibliographic record for the title

3. Once you have a record in Next Search Catalog add "[On order]" or "(Street date mm/dd/yyyy)" to the end of the 245$a field.

    |on_order_record_0010|

4. Add an item record, but make the following changes to the item record:

  A. Change the "Not for loan" status of the item to "Ordered" (This step is required)

      "Ordered" is a priveledged status in Next Search Catalog.  It is the only "Not-for-loan" status that allows for requests.  Requests placed on an "Ordered" item will move across the holds queue like any other request, but "Ordered" items will not appear in the holds queue until the "Ordered" status has been removed.

  B. If you want to place item level requests on this item, you _must_ add a barcode number

      (see the note below)

  C. Add a public note to the item record indicating the publisher's release date (optional)

    |on_order_record_0020|

5. When you receive the item you need to make the following changes to the bibliographic record:

  A. Remove the "[On order]" or "(Street date mm/dd/yyyy)" notations from the 245$a field

  B. Update and make any other changes to the bibliographic record as needed

    |on_order_record_0030|

6. When you receive the item you need to make the following changes to the item records

  A. Remove the not for loan status

  B. If you added a barcode number, you can update that number if you wish

  C. Remove the public note indicating the release update

  D. Any other changes as necessary for cataloging the order_item

    |on_order_record_0040|

Note:

  If you create an item record and do not add a barcode number to the record **AND** someone puts an *item specific* request on the item with no barcode, the request will **never** be filled.  When an item level request is placed, the request is tied to the barcode number on the item.  If the item being requested doesn't have a barcode number, the barcode number in the request is recorded as an empty string - i.e. "".  If that happens, only barcode number "" can fill the request.  Since you can't check in "", the request will **never** be filled.
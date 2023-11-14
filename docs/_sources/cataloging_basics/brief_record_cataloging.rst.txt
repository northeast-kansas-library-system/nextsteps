.. include:: /include.rst

Brief record cataloging
=======================

If you can’t find a record already in Next Search Catalog, or a record via Z39.50, or a record in Shareit, or a record from another source, you may need to create an original catalog record.

A. Go to Cataloging 

    |brief_record_cataloging_0010|

B. Choose New Record --> Brief Records

    |brief_record_cataloging_0020|

C. Fill in the following fields accordingly, if applicable:

  - 000 -- Leader - click in this field and let it autofill (required)
  - 008 -- Fixed length data elements - click in this field and let it autofill (required)
  - 020 or 024

    - 020 -- ISBN number if the item has one (books)
    - 024 -- UPC code if the item doesn't have an ISBN (DVDs, Blu-ray discs, music CDs)

  - 100 -- Author (if applicable)
  - 245 -- Title (required)
  - 250 -- edition (if applicable)
  - 264 -- Publication information

    - a - place
    - b - publisher
    - c - year (most important piece of information here)

  - 300 -- physical description. Please at least record the number of pages, number of discs.
  - 490 -- series statement (if applicable)
    
    - a - series name
    - v - volume number
  
  - 500 – add note if applicable
  - 942 Koha elements 

    - e - shelving location (required)
    - c - item type (required)
    - h - collection code (required)

  |brief_record_cataloging_0030|

D. Once bibliographic records have been added, see :doc:`the instructions for adding items to records to continue </cataloging_basics/adding_item_to_record>`

  (Please note that if a bibliograhic record does not have an item added to it within 14 days, the bibliographic record will automatically be deleted)
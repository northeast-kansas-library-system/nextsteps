.. include:: /include.rst

ILL brief record cataloging 
===========================

Some libraries use brief ILL records to track inter-library-loans.

In this workflow, the library creates a new, temporary bibliographic record and item each time an item arrives from ShareIt or OCLC to fill an ILL request.

The advantage of this workflow is that the borrower has access to more information in their library account about the title they've borrowed.  

The disadvantage is that you need to create records and items for every item that you borrow through ILL.  Additionally, since these records are temporary, there is more work needed to remove the temporary records when the items are returned.

To create a brief temporary bibliographic record for an ILL item:

A. Go to Cataloging 

    |brief_record_cataloging_0010|

B. Choose New Record --> Fast add for ILL or temporary circulation

    |ill_brief_record_cataloging_0010|

C. Fill in the following fields accordingly, if applicable:

    - 100 -- Author (if applicable)
    - 245 -- Inter Library Loan
    - 942 Koha elements 
      - e - Location: Adult / Childrens / Young adult (you choose)
      - c - Item type: Borrowed from another library
      - h - Collection code: Interlibrary loan
      - n - Suppress in OPAC: Suppressed

    |ill_brief_record_cataloging_0020|

D. Once the bibliographic record is created, you need to add an item to the record

    |ill_brief_record_cataloging_0030|

E. Once the record and the item are created, you check them out to the borrower just like any normal item

F. When the item is returned, you need to delete the item and the bibliographic record



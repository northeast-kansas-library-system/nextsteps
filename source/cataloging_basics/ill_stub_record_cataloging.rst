.. include:: /include.rst

ILL stub record cataloging 
==========================

Some libraries use "Stub" records to track inter-library-loans.

In this workflow, the library creates 1 bibliographic record and adds multiple generic ILL items with individual barcode numbers to the record, then they create book-wraps with those generic numbers printed on them.  When the library needs to issue an ILL that they've received from ShareIt or OCLC to a borrower, they put the book-wrap on the exterior of the item and check out the item to the borrower using the barcode number on the book-wrap.

The advantage of this method is that you don't have to catalog anything in Next Search Catalog when ILL items arrive at the library.  All you have to do is put the book-wrap on the item and let the borrower know the item has arrived.  Then when they pick it up you check out the stub-record to the borrower.

The disadvantage is that you have to manually track which ShareIt or OCLC title goes with which book-wrap and the borrower will not be able to see the title of the ILL in the OPAC.  All they will see is a record called "Inter library loan item."

This is the process for creating an ILL record like this:

A. Go to Cataloging 

    |brief_record_cataloging_0010|

B. Choose New Record --> Brief Records

    |brief_record_cataloging_0020|

C. Fill in the following fields as shown below:

  - 000 -- click in this field and let it autofill
  - 008 -- click in this field and let it autofill
  - 245 -- Inter Library Loan
  - 942 Koha elements 
    - e - Location: Adult / Childrens / Young adult (you choose)
    - c - Item type: Borrowed from another library
    - h - Collection code: Unclassified
    - n - Suppress in OPAC: Suppressed

    |ill_stub_record_cataloging_0010|

D. Once the record is created, add as many items as you think you need to the bibliographic record.

    |ill_stub_record_cataloging_0020|
  
E. Create book-wraps for the stub-record items

    :download:`Microsoft Word template (requires barcode 3 of 9 font) </_files/ill_bookwrap_sample.docx>`

    :download:`PDF template </_files/ill_bookwrap_sample.pdf>`

    `Google Docs template (requires barcode 3 of 9 font) <https://docs.google.com/document/d/1gn4Bks7v4xPVt6uhSHWhPnbiAsQyKhe5w9vz3ZuCJUw/edit?usp=sharing>`_ 

F. When ILL items arrive from ShareIt or OCLC, wrap one of the ILL book-wraps around the item and check it out to the borrower using the barcode number on the book-wrap.  When items are returned, the barcode number on the book-wrap is ready to be used for another ILL.
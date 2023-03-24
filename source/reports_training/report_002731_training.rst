.. include:: /include.rst

********************
Report 2731 Training
********************

Purpose of report 2731
======================

The main purpose of report 2731 is to provide an easy-to-read shelf-list of every item in a library that meets the criteria you set.  It can be used for:

- Inventory 
- Weeding 
- Identifying items added in a specific date range
- Identifying items that have not checked out in a long time
- Identifying item that have never checked out 
- Identifying multiple copies of items at a library 
- Identifying all of the items in a library that start with the same call number digits 

Frequency for running report 2731
=================================

This report sould be run whenever you need its results.

Finding report 2731
===================

You can find report 214 following the instructions in :ref:`"Finding a report by number" <Finding a report by number>`

Report 2731 parameters and their defaults
=========================================

Reports 2731 has a large number of runtime parameters available.

- Item home library 

  - **Default** = Atchison Public Library
  - Includes "Doniphan County-ALL"
  - Includes "Prairie Hills Schools - ALL SCHOOLS"
  - We use a custom authorised values table called "ZBRAN" to include the "ALL" options |br| |br|

- Item permanent shelving location
   
  - **Default** = All shelving locations 
  - We use a custom authorised values table called "LLOC" to allow for flexibility in this dropdown |br| |br|

- Item type 

  - **Default** = All item types
  - We use a custom authorised values table called "LITYPES" to allow for flexibility in this dropdown |br| |br|

- Item collection code 

  - **Default** = All collection codes 
  - We use a custom authorised values table called "LCCODE" to allow for flexibility in this dropdown |br| |br|

- Enter first part of call number or a % symbol 

  - **Default** = %
  - We use custom code to add a "%" to all fields in the reports module where the label includes the phrase "or a % symbol" |br| |br|

- Not for loan status 

  - **Default** = All items 
  - We use a custom authorised values table called "LNOT_LOAN" to allow for flexibility in this dropdown |br| |br|

- Item added between date 1 
- and-date 2 

  - **Default** date 1 = 01/01/2000 
  - **Default** date 2 = today's date 
  - The SQL for the report is written in such a way that if there are items that were added before 01/01/2000 or if the items.dateaccessioned fieled is blank, the report reads their date as 01/01/2000 
  - The dates are populated by custom code that always sets report fields with a label ending in "date 1" to "01/01/2000" and always sets report fields with a label ending in "date 2" to today's date |br| |br|


- Item last borrowed between date 1 
- and--date 2 

  - **Default** date 1 = 01/01/2000 
  - **Default** date 2 = today's date  
  - "Last borrowed" = the last time an item was checked out
  - The SQL for the report is written in such a way that if there are items that were last borrowed before 01/01/2000 or if the items.lastborrowed fieled is blank, the report reads their date as 01/01/2000 
  - The dates are populated by custom code that always sets report fields with a label ending in "date 1" to "01/01/2000" and always sets report fields with a label ending in "date 2" to today's date |br| |br|

- Item last seen between date 1 
- and---date 2 

  - **Default** date 1 = 01/01/2000 
  - **Default** date 2 = today's date
  - "Last seen" = the last time an item was checked in
  - The SQL for the report is written in such a way that if there are items that were last seen before 01/01/2000 or if the items.lastseen fieled is blank, the report reads their date as 01/01/2000 
  - The dates are populated by custom code that always sets report fields with a label ending in "date 1" to "01/01/2000" and always sets report fields with a label ending in "date 2" to today's date |br| |br|

- With X or fewer checkouts 

  - **Default** = Any number - no limits
  - We use a custom authorised values table called "ZNUMBERS" to allow for flexibility in this dropdown |br| |br|

- Display checked out items 

  - **Default** = Show all
  - We use a custom authorised values table called "ZYES_NO" to allow for flexibility in this dropdown |br| |br|

- Display lost, missing, and withdrawn items 

  - **Default** = Show all
  - We use a custom authorised values table called "ZYES_NO" to allow for flexibility in this dropdown |br| |br|

- With X or more copies at this library 

  - **Default** = 000
  - We use a custom authorised values table called "YNUMBER" to allow for flexibility in this dropdown |br| |br|

- With X or more copies throughout the catalog 

  - **Default** = 000
  - We use a custom authorised values table called "YNUMBER" to allow for flexibility in this dropdown |br| |br|


Report 2731 - full shelf list for an entire library 
===================================================

To generate a shelf list of everything that is supposed to be at your library:

1. Find report 2731 and click on "Run" 
2. Set the runtime parameters as follow:

  - Item home library = Your library 
  - Leave **ALL** other parameters set to their defaults

For example: If you wanted a shelf list showing every items owned by NEKLS set these parameters:

  - Item home library = Northeast Kansas Library System 
  - Leave **ALL** other parameters set to their defaults

  |report_2731_0020|

Report 2731 - items added during a date range 
=============================================

To generate a shelf-list of everything added during a specific date range:

1. Find report 2731 and click on "Run" 
2. Set the runtime parameters as follow: 

  - Item home library = Your library 
  - Item added between date1 = First date of date range 
  - and-date2 = Last date of date range 
  - Leave **ALL** other parameters set to their defaults

For example: If you wanted a shelf list showing every item added at BERN during between May 1, 2020, and May 31, 2020, set these parameters:

  - Item home library = Bern Community Library
  - Item added between date1 = 05/01/2020 
  - and-date2 = 05/31/2020 
  - Leave **ALL** other parameters set to their defaults

  |report_2731_0030|

-----------

.. include:: /reports/report_002731.rst
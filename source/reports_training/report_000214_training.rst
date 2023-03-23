.. include:: /include.rst

*******************
Report 214 Training
*******************

Purpose of report 214
=====================

The purpose of this report is to identify items that have incomplete or problematic item record fields.  For example, if you chceck out an item that has no replacement price entered, if the item is never returned the lost item process will automatically bill the borrower $0.00 for the replacement because, as far as the system is concerned, the item has no price.  Similarly, if an item has a blank item type, the item will not check out for the proper length of time and borrowers may not be able to place requests on the item because an item type is crucial in the circulation rules matrix.

Frequency for running report 214
================================

Ideally, each library should run this report and try to resolve the issues with these items once a month.

Finding report 214
==================

You can find report 214 following the instructions in :ref:`"Finding a report by number" <Finding a report by number>`

Using report 214
================

When you run report 214 you'll be given options to choose a library and to choose a problem type.  The report is very flexible and allows you to view all items with problems, or just items with one or two specific problems.




.. include:: /reports/report_000214.rst
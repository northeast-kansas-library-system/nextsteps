.. include:: /include.rst

Expired borrowers processing
============================

Next Search Catalog policy is to delete borrower accounts that have been expired for more than 3 years unless:

- The borrower has a non-zero account balance
- The borrower is the guarantor to another account
- The borrower has unfilled requests on their account
- The borrower has any items checked out

The process has evolved in such a way that, when a person's account has been expired for more than 2 years, an extended attribute is added to the account marking it as "Account expired for 2+ years - will be deleted at 3+ years" or "Account expired for 2+ years - cannot be deleted due to fines/fees/ouverdues/etc."

Then when an account has been expired for more than 3 years the attribute is modified as "Account expired for 3+ years - will be auto-deleted on MM.15" or "Account expired for 3+ years - can't be auto-deleted due to problems with the account" or "Account expired for 3+ years - can't be auto-deleted due to problems with the account"

At any point in time library staff can run report 3091 to see which borrowers have any of these attributes on their accounts.
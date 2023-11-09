TEst 1      Test 2

+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
|          Rule           | Options                    |                                      Explanation                                  |br| |
+=========================+============================+========================================================================================+
|                                                               **General settings**                                                       |br| |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| Library            |br| | All libraries         |br| | Which library does the rule apply to                                              |br| |
|                         | - OR -                |br| |                                                                                        |
|                         | Specific library      |br| |                                                                                        |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| Borrower category  |br| | All borrowers         |br| | Which borrower category does the rule apply to                                    |br| |
|                         | - OR -                |br| |                                                                                        |
|                         | Specific category     |br| |                                                                                        |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| Item type          |br| | All item types        |br| | Usualy includes the Zen Desk ticket number to document request for change         |br| |
|                         | - OR -                |br| |                                                                                        |
|                         | Specific item type    |br| |                                                                                        |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| Note               |br| | Optional field        |br| | Usualy includes the Zen Desk ticket number to document request for change         |br| |
|                         | (32 characters max)   |br| |                                                                                        |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
|                                                                Checkout rules                                                            |br| |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| Current checkouts  |br| | Unlimited             |br| | Maximum total number of items of this item type that a borrower                   |br| |
| allowed            |br| | - OR -                |br| | can have checked out from this library at any given moment                        |br| |
|                         | a number between 1-999,999 |                                                                                        |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| Loan period        |br| | 1-999999              |br| | "Loan period" + "Unit" = how long an item checks out                              |br| |
+-------------------------+----------------------------|                                                                                        |
| Unit               |br| | Days/Hours            |br| | If "Loan period" = 21 and "Unit" = Days, items check out for 21 days              |br| |
|                         | - OR -                |br| | If "Loan period" = 36 and "Unit" = Hours, items check out for 36 hours            |br| |
|                         | Hours                 |br| |                                                                                        |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| Days mode          |br| | Default               |br| | Default = follow the system preference "useDaysMode"                              |br| |
|                         | - OR -                |br| |                                                                                        |
|                         | Skip closed days      |br| | Skip = circulation rules will skip days the library is closed when calculating    |br| |
|                         | - OR -                |br| | due dates                                                                         |br| |
|                         | Next open day         |br| | - i.e. if the circulation rules specify a 21 day check out and you are checking out    |
|                         | - OR -                |br| | an item to a borrower on Tuesday, August 1, the item will be due on Friday, August 25, |
|                         | Ignore the calendar   |br| | because this setting will not count the 3 Sundays between August 1 and August 25. |br| |
|                         | - OR -                |br| |                                                                                        |
|                         | Same week day         |br| | Next=If the calendar says the library is closed on a day an item would normally be|br| |
|                         |                            | due, push the due date to the next date the calendar says the library is open.    |br| |
|                         |                            |                                                                                        |
|                         |                            | Ignore=Ignore the calendar when calculating due dates                             |br| |
|                         |                            | - i.e. if an item being checked out would normally be due on a day the library    |br| |
|                         |                            | is closed, Koha will make the item due on that day no matter what.                |br| |
|                         |                            |                                                                                        |
|                         |                            | Same week day=If an item being checked out would normally be due on a day when    |br| |
|                         |                            | the calendar says the library is closed, push the due date to the next time the   |br| |
|                         |                            | calendar says the library is open on that same weekday                            |br| |
|                         |                            | - i.e. if an item would normally be due on a Thursday but the calendar has that   |br| |
|                         |                            | day listed as closed, push the due date to the next Thursday the                  |br| |
|                         |                            | calendar shows the library as open.                                               |br| |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| Hard due date      |br| | Before                |br| | Items must be returned Before/Exactly on/After                                    |br| |
|                         | - OR -                |br| | the due date specified in the preference                                          |br| |
|                         | Exactly on            |br| |                                                                                        |
|                         | - OR -                |br| | This is mostly used by schools - i.e. All items checked out are given a due date  |br| |
|                         | After                 |br| | BEFORE 2020-05-10.  This forces due   dates to fall before the end of the school year. |
|                         |                            |                                                                                        |
|                         | AND                   |br| |                                                                                        |
|                         | YYYY-MM-DD            |br| |                                                                                        |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| Decreased loan period   | Blank                 |br| | Works with decreaseLoanHighHolds, decreaseLoanHighHoldsDuration,                  |br| |
|                         | - OR -                |br| | decreaseLoanHighHoldsValue, decreaseLoanHighHoldsControl,                         |br| |
| for high hold      |br| | 1-999,999             |br| | and decreaseLoanHighHoldsIgnoreStatuses system preferences.                       |br| |
|                         |                            |                                                                                        |
| (day)              |br| |                            | Allows library to specify reduced loan period if the holds ratio exceeds parameters    |
|                         |                            | set in system preferences.                                                        |br| |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
|                                                                   Renewals                                                               |br| |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| Renewals allowed   |br| | Unlimited             |br| | How many times can an item of this type be renewed                                |br| |
|                         | - OR -                |br| |                                                                                        |
| (count)            |br| | 0-999,999             |br| |                                                                                        |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| Renewal period     |br| | 0-999,999             |br| | How many "Unit"s does it renew for                                                |br| |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| No renewal before  |br| | Blank                 |br| | Number of "Unit"s before the due date when the auto-renewal process will start    |br| |
|                         | - OR -                |br| |                                                                                        |
|                         | 0-999,999             |br| |                                                                                        |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| Automatic renewal  |br| | Yes                   |br| |                                                                                        |
|                         | - OR -                |br| |                                                                                        |
|                         | No                    |br| |                                                                                        |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| No automatic renewal    | Blank                 |br| | Number of "Unit"s after the issue date when the auto-renewal process will end     |br| |
|                         | - OR -                |br| |                                                                                        |
| renewal after      |br| | 1-999,999             |br| |                                                                                        |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| No automatic renewal    | Blank                 |br| | Specific date when the auto-renewal process will end                              |br| |
|                         | - OR -                |br| |                                                                                        |
| after (hard date limit) | YYYY-MM-DD            |br| |                                                                                        |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
|                                                                   Requests                                                               |br| |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| Requests allowed   |br| | Blank                 |br| | Maximum number of requests a borrower can have at any given moment                |br| |
| (total)            |br| | - OR -                |br| |                                                                                        |
|                         | 0-999,999             |br| |                                                                                        |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| Requests allowed   |br| | Blank                 |br| | Maximum number of requests a borrower can place on this item type in one single day    |
| (daily)            |br| | - OR -                |br| |                                                                                        |
|                         | 0-999,999             |br| |                                                                                        |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| Requests per record|br| | Blank                 |br| | Maximum number of requests a borrower can place on a single record                |br| |
| (count)            |br| | - OR -                |br| |                                                                                        |
|                         | 0-999,999             |br| |                                                                                        |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| On shelf requests  |br| | Yes                   |br| | If this is set to "No" a borrower cannot place requests on a bibliographic        |br| |
| allowed            |br| | - OR -                |br| | record if a copy of the item they want is currently checked in and available      |br| |
|                         | No                    |br| |                                                                                        |
|                         |                            |                                                                                        |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| Opac item level    |br| | Don't allow           |br| | Can a borrower place an item level request via the OPAC                           |br| |
| requests           |br| | - OR -                |br| |                                                                                        |
|                         | Allow                 |br| | Don't allow = no                                                                  |br| |
|                         | - OR -                |br| | Allow = yes                                                                       |br| |
|                         | Force                 |br| | Force = the borrower MUST choose a specific item                                  |br| |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
|                                                                   Late fees                                                              |br| |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| Late fee amount    |br| | 0.00-999,999.99       |br| | Cost of late fees                                                                 |br| |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| Fee interval       |br| | Blank                 |br| | per fee interval (in "Unit"s)                                                     |br| |
|                         | - OR -                |br| |                                                                                        |
|                         | 1-999,999             |br| |                                                                                        |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| When to charge     |br| | End of interval       |br| | charged at the (End of/Start of) the Fee interval                                 |br| |
|                         | - OR -                |br| |                                                                                        |
|                         | Start of interval     |br| |                                                                                        |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
|                         |                            | Late fees are set by a combination of "Late fee amount", "Fee interval", "Unit",  |br| |
|                         |                            | and "When to charge"                                                              |br| |
|                         |                            |                                                                                        |
|                         |                            | The late fee billed to a borrower =                                               |br| |
|                         |                            | ("Fee interval" x "Unit") x "Late fee amount"                                     |br| |
|                         | Late fee formula:     |br| |                                                                                        |
|                         |                            | So a library that wanted to charge a 1.00 per week late fee would have to have:   |br| |
|                         |                            |                                                                                        |
|                         |                            | "Fee interval" = 7; "Unit" = Days; "Late   fee" = $1.00                           |br| |
|                         |                            |                                                                                        |
|                         |                            | "When to charge" would then tell Koha whether to bill the borrower at the start of|br| |
|                         |                            | the week or the end of the week - i.e. charge the moment the item is overdue      |br| |
|                         |                            | or wait until it's been overdue a full 7 days.                                    |br| |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| Grace period       |br| | Blank                 |br| | "Grace period" follows the same "Unit" measurement as   loans and late fees       |br| |
|                         | - OR -                |br| |                                                                                        |
|                         | 1-999,999             |br| |                                                                                        |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| Late fee cap (amount)   | 0.00-999,999.99       |br| | What is the maximum late fee for this type of item                                |br| |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| Cap fee at         |br| | Checkbox              |br| | If "Late fee cap" is left blank and this checkbox is checked,   then the          |br| |
| replacement price  |br| |                            |                                                                                        |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
|                                                              Things we don't use                                                         |br| |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| Current on site    |br| | Unlimited             |br| | Suspension is not widely used in the USA.                                         |br| |
| checkouts allowed  |br| | - OR -                |br| | Suspension is a type of penalty system where, for example, if a borrower keeps    |br| |
|                         | 1-999,999             |br| | an item 4 days overdue, their account is suspended for borrowing for 4 days. If you    |
+-------------------------+----------------------------+ If a borrower keeps something overdue for 180 days, their account is suppended for|br| |
| Suspension in days |br| | Blank                 |br| | 180 days, etc.                                                                    |br| |
| (day)              |br| | - OR -                |br| |                                                                                        |
|                         | 1-999,999             |br| | These settings control the duration of the suspension.                            |br| |
+-------------------------+----------------------------+                                                                                        |
| Maximum suspension |br| | Blank                 |br| |                                                                                        |
| duration (day)     |br| | - OR -                |br| |                                                                                        |
|                         | 1-999,999             |br| |                                                                                        |
+-------------------------+----------------------------+                                                                                        |
| Suspension charging|br| | Blank                 |br| |                                                                                        |
| interval           |br| | - OR -                |br| |                                                                                        |
|                         | 1-999,999             |br| |                                                                                        |
|                         |                            |                                                                                        |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+
| Rental discount    |br| | Blank                 |br| | Rental discount is a feature Next Search Catalog does not currently use           |br| |
| (percentage)       |br| | - OR -                |br| |                                                                                        |
|                         | .01-100 (percentage)  |br| |                                                                                        |
+-------------------------+----------------------------+----------------------------------------------------------------------------------------+

.. |br| raw:: html

    <br />

.. |ss| raw:: html

    <strike>

.. |se| raw:: html

    </strike>
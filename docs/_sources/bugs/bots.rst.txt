.. include:: /include.rst

********************************************
March 2025 - Koha slowness caused by AI bots
********************************************

Currently we have had issues on several days in the last few weeks where Koha slows down.  This is not actually a Koha problem - it's an AI problem.

Generative AI systems like Chat GPT need to gather a massive amount of data from the internet in order to work.  They do this by what's called "data scraping" (https://en.wikipedia.org/wiki/Data_scraping).  Essentially generative AI systems use "bots"  (https://en.wikipedia.org/wiki/Internet_bot) to try to download all of the raw data from a website so they can add that data to their systems.

As far as this relates to the slowness in Koha goes, over the last several weeks there have been several times where the ByWater Solutions servers have been overrun with bots that are doing scraping for generative AI systems.  To remedy this problem ByWater Solutions is working to move all of their customer's data behind a more sophisticated firewall that can give them more information about which bots are trying to scrape our Koha site and automate processes to block them.

Cloudflare, an internet infrastructure company, estimates that about AI bots attempt to download pages from websites approximatly 50,000,000,000 times per day.  If just a 100,000 of those are aimed at one of our servers (about .0002% of that estimated number of downloads per day), that could certainly be the source of our problems with Koha running slowly.
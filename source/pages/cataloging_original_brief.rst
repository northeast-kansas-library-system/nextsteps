.. include:: /include.rst

##########################################################
Cataloging - create an original brief bibliographic record
##########################################################

If you can’t find a record already in Next Search Catalog; you can't find a record via Z39.50 or a record in Shareit; then you may need to create an original catalog record.

1. Click on "Cataloging"

|cataloging_original_brief_010|

2. Choose "Brief records" from the "+New record" drop-down menu 

|cataloging_original_brief_020|

3. Fill in the following fields accordingly, if applicable: 

  - 000 -- Leader - click in this field and let it autofill
  - 008 -- Fixed length data elements - click in this field and let it autofill 

    -  If the item is a book add the ISBN to the 020$a field 
    -  If the item is a magazine add the ISSN to the 022$a field
    -  If the item is another type (DVD, CD, cake pan, other), add the UPC code to the 024$a field 

  - 100$a -- Author (if applicable) 
  - 245$a -- Title (required) 
  - 250$a -- edition (if applicable)
  - 264 -- Fill in subfields as follow:

    - $a Place of publication (enter [Place of publication not identified] if it is not clear)
    - $b Name of publisher (enter [publisher not identified] if no publisher is indicated)
    - $c Year (most important piece of information - use current year if unsure) 

  - 300 -- Fill in subfields as follow:
  
    - $a Book = number of pages followed by a space and a colon - i.e. <454 pages :>
    - $a Video = number of discs followed by lenght in parantheses - i.e. <1 videodisc (1 hour, 51 minues) :>
    - $c Dimensions = height of book in centimeters or diameter of videodisc in inches - i.e. <21 cm.> or <4 1/2 in.>
  
  - 490 -- Series statement (if applicable)

    - $a Series name followed by a space and a semicolon (initial articles are omitted in this field) - i.e. <Harry Potter ;>
    - $v Volume number - i.e. <3> or <4> or <7> - it is not neccessary to use indicators like "number" or "v." or "vol." or "vololume"

  - 500$a -- Notes (optional) 
  - 942 -- You are required to fill in these fields:

    - $e Record level shelving location 
    - $c Record level item type 
    - $h Record level collection code 

|cataloging_original_brief_030|

4. Click on "Save"
# custom-koha-opac-xslt
Custom XSLT files for the results and detail views in Koha

These files represent edits to the default XSLT files in the Koha OPAC so that only the a and b subfields of $245, without ISBD or other erroneous punctuation (e.g. trailing slashes and periods), are should in the results and detail views.

Please note: when changing Koha XSLT files, it is advised to use duplicates of the originals rather than editing the originals directly.

## Before:
![Screenshot of results view before edits to the XSLT file](https://github.com/BI-Library/custom-koha-opac-xslt/blob/main/images/before.png "Notice that additional 245 subfields are included in the title display. For instance in the third result listed here, the 'state of responsibility' field (i.e. 245$c) is included.")

## After:
![Screenshot of results view after edits to the XSLT file](https://github.com/BI-Library/custom-koha-opac-xslt/blob/main/images/after.png "Here you can see that we have excluded additional subfields deemed to be redundant in an attempt to improve readability. We have also removed trailing punctuation which wasn't consistent throughout the bibliographic records; trailing slashes and periods for example.")
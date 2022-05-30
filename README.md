# About
Custom XSLT files for the results and detail views in Koha
## TL;DR
These files represent edits to the default XSLT files in the Koha OPAC so that only the a and b subfields of $245, without ISBD or other erroneous punctuation (e.g. trailing slashes and periods), are should in the results and detail views.

### Before:
![Screenshot of results view before edits to the XSLT file](https://github.com/BI-Library/custom-koha-opac-xslt/blob/main/images/before.png "Before Screenshot")
Notice that additional 245 subfields are included in the title display. For instance in the third result listed here, the 'state of responsibility' field (i.e. 245$c) is included.

### After:
![Screenshot of results view after edits to the XSLT file](https://github.com/BI-Library/custom-koha-opac-xslt/blob/main/images/after.png "After screenshot")
Here you can see that we have excluded additional subfields deemed to be redundant in an attempt to improve readability. We have also removed trailing punctuation which wasn't consistent throughout the bibliographic records; trailing slashes and periods for example.

## Installation

Please note: when changing Koha XSLT files, it is advised to use duplicates of the originals rather than editing the originals directly.

1. Locate XSLT files
In Debian package installations of Koha, these are located in your theme inside a folder named 'xslt' under the locale of the selected theme you are using, e.g. `/usr/share/koha/opac/htdocs/opac-tmpl/bootstrap/en/xslt/`.

2. Download the XSLT files included here.

3. Change their names, appending '-custom' for example.

4. Upload files to the xslt folder of your Koha instance.

5. Change Koha system preference **OPACXSLTResultsDisplay** from its original setting (i.e. “default”) to the path of our new file MARC21slim2OPACResults-custom.xsl. In this example that would be `/usr/share/koha/opac/htdocs/opac-tmpl/bootstrap/en/xslt/`. Likewise the other system preference OPACXSLTDetailsDisplay was changed to `/usr/share/koha/opac/htdocs/opac-tmpl/bootstrap/en/xslt/MARC21slim2OPACDetail-custom.xsl`.

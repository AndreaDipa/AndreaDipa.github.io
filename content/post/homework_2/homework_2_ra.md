+++
title = "Homework 2, research on application"
date = 2022-10-07T08:04:36+02:00
draft = false
author = "Andrea Di Paolo"
+++
Assignment:
<ul>
    <li> CSV protocol RFC 4180 (definition and rules) </li>
</ul>

<!--more-->
# <mark> Definiton </mark>
CSV is a simple format for representing a rectangular array (matrix) of numeric and textual values. It an example of a "flat file" format. It is a delimited data format that has fields/columns separated by the comma character %x2C (Hex 2C) and records/rows/lines separated by characters indicating a line break. RFC 4180 stipulates the use of CRLF pairs to denote line breaks, where CR is %x0D (Hex 0D) and LF is %x0A (Hex 0A). Each line should contain the same number of fields. Fields that contain a special character (comma, CR, LF, or double quote), must be "escaped" by enclosing them in double quotes (Hex 22). An optional header line may appear as the first line of the file with the same format as normal record lines. This header will contain names corresponding to the fields in the file and should contain the same number of fields as the records in the rest of the file. CSV commonly employs US-ASCII as character set, but other character sets are permitted.

# <mark> Rules <mark>
<ul>
    <li> Separate data fields with a delimiter, usually a comma, </li>
    <li> keep each record on a separate line, </li>
    <li> do not follow the last record in a file with a carriage return, </li>
    <li> in the first line of the file, include a header with a list of the column names in the file, </li>
    <li> make sure the header list is delimited in the same way as the rest of the file, </li>
    <li> remember that the enclosing character (typically double quotes) must be used when required. </li>
</ul>

# References 
[1] loc.gov, "CSV, Comma Separated Values (RFC 4180)", 2021, [URL](https://www.loc.gov/preservation/digital/formats/fdd/fdd000323.shtml),
[2] thoughtspot.com, "6 Rules for Creating Valid CSV Files", 2015, [URL](https://www.thoughtspot.com/blog/6-rules-creating-valid-csv-files).
# HEADER_RECORD
## Abstract
The header structure provides information about the entire transmission. The SOURce system name
identifies which system sent the data. The DESTination system name identifies the intended receiving
system. The reading program must read the &lt;<a href=Ged.VERSION_NUMBER.md>VERSION_NUMBER</a>&gt; and the &lt;<a href=Ged.GEDCOM_FORM.md>GEDCOM_FORM</a>&gt; values to insure proper readability.
The &lt;<a href=Ged.CHARACTER_SET.md>CHARACTER_SET</a>&gt; value is mandatory and must be read first to select the appropriate character set.


## GEDCOM syntax and proprietary extensions

**HEADER_RECORD**:=
<pre>
<b>n HEAD{1:1}</b>
<b>  +1 SOUR &lt;<a href=Ged.SYSTEM_ID.md>SYSTEM_ID</a>&gt;{1:1}</b>
    +2 VERS &lt;<a href=Ged.VERSION_NUMBER.md>VERSION_NUMBER</a>&gt;{0:1}
    +2 NAME &lt;<a href=Ged.NAME_OF_PRODUCT.md>NAME_OF_PRODUCT</a>&gt;{0:1}
    +2 CORP &lt;<a href=Ged.NAME_OF_BUSINESS.md>NAME_OF_BUSINESS</a>&gt;{0:1}
      +3 &lt;&lt;<a href=Ged.ADDRESS_STRUCTURE.md>ADDRESS_STRUCTURE</a>&gt;&gt;{0:1}
    +2 DATA &lt;<a href=Ged.NAME_OF_SOURCE_DATA.md>NAME_OF_SOURCE_DATA</a>&gt;{0:1}
      +3 DATE &lt;<a href=Ged.PUBLICATION_DATE.md>PUBLICATION_DATE</a>&gt;{0:1}
      +3 COPR &lt;<a href=Ged.COPYRIGHT_SOURCE_DATA.md>COPYRIGHT_SOURCE_DATA</a>&gt;{0:1}
        +4 [CONT|CONC] &lt;<a href=Ged.COPYRIGHT_SOURCE_DATA.md>COPYRIGHT_SOURCE_DATA</a>&gt;{0:M}
  +1 DEST &lt;<a href=Ged.RECEIVING_SYSTEM_NAME.md>RECEIVING_SYSTEM_NAME</a>&gt;{0:1} *
  +1 DATE &lt;<a href=Ged.CREATION_DATE.md>CREATION_DATE</a>&gt;{0:1}
    +2 TIME &lt;<a href=Ged.TIME_VALUE.md>TIME_VALUE</a>&gt;{0:1}
<b>  +1 SUBM @&lt;<a href=Ged.XREF_SUBM.md>XREF:SUBM</a>&gt;@{1:1}</b>
  +1 SUBN @&lt;<a href=Ged.XREF_SUBN.md>XREF:SUBN</a>&gt;@{0:1}
  +1 FILE &lt;<a href=Ged.FILE_NAME.md>FILE_NAME</a>&gt;{0:1}
  +1 COPR &lt;<a href=Ged.COPYRIGHT_GEDCOM_FILE.md>COPYRIGHT_GEDCOM_FILE</a>&gt;{0:1}
<b>  +1 GEDC{1:1}</b>
<b>    +2 VERS &lt;<a href=Ged.VERSION_NUMBER.md>VERSION_NUMBER</a>&gt;{1:1}</b>
<b>    +2 FORM &lt;<a href=Ged.GEDCOM_FORM.md>GEDCOM_FORM</a>&gt;{1:1}</b>
<b>  +1 CHAR &lt;<a href=Ged.CHARACTER_SET.md>CHARACTER_SET</a>&gt;{1:1}</b>
    +2 VERS &lt;<a href=Ged.VERSION_NUMBER.md>VERSION_NUMBER</a>&gt;{0:1}
  +1 LANG &lt;<a href=Ged.LANGUAGE_OF_TEXT.md>LANGUAGE_OF_TEXT</a>&gt;{0:1}
  +1 PLAC{0:1}
<b>    +2 FORM &lt;<a href=Ged.PLACE_HIERARCHY.md>PLACE_HIERARCHY</a>&gt;{1:1}</b>
  +1 NOTE &lt;<a href=Ged.GEDCOM_CONTENT_DESCRIPTION.md>GEDCOM_CONTENT_DESCRIPTION</a>&gt;{0:1}
    +2 [CONC|CONT] &lt;<a href=Ged.GEDCOM_CONTENT_DESCRIPTION.md>GEDCOM_CONTENT_DESCRIPTION</a>&gt;{0:M}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />


NOTE:
Submissions to the Family History Department for Ancestral File submission or for clearing temple ordinances  must use a
DESTination of ANSTFILE or TempleReady, respectively.

## Geneweb behavior

level tag  | Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#head>HEAD</a> |  | yes | yes | 
+1 <a href=Ged.GLOSSARY.md#sour>SOUR</a> | char{1:20} | record SYSTEM_ID | yes | export with SYSTEM_ID=Geneweb
+2 <a href=Ged.GLOSSARY.md#vers>VERS</a> | char{1:15} | ignore &#x26A0; | yes | export geneweb version
+2 <a href=Ged.GLOSSARY.md#name>NAME</a> | char{1:90} | ignore | yes | export name gwb2ged
+2 <a href=Ged.GLOSSARY.md#corp>CORP</a> | char{1:90} | ignore | yes &#x2753; | export INRIA name; "geneweb team" would be better &#x1F4CD;
+3  | &lt;<a href=Ged.ADDRESS_STRUCTURE.md>ADDRESS_STRUCTURE</a>&gt; | ignore | partial &#x26A0; | url http://www.geneweb.org export in postal address (ADDR tag). Shall be corrected with WWW tag.
+2 <a href=Ged.GLOSSARY.md#data>DATA</a> | char{1:90} | ignore | yes | export name of gw database
+3 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_EXACT.md>DATE_EXACT</a>&gt; | ignore | no | 
+3 <a href=Ged.GLOSSARY.md#copr>COPR</a> | char{1:90} | ignore | no | 
+4 <a href=Ged.GLOSSARY.md#cont>CONT</a>\|<a href=Ged.GLOSSARY.md#conc>CONC</a> | char{1:90} | ignore | no | 
+1 <a href=Ged.GLOSSARY.md#dest>DEST</a> | char{1:20} | ignore | no | 
+1 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_EXACT.md>DATE_EXACT</a>&gt; | ignore | yes | Creation date
+2 <a href=Ged.GLOSSARY.md#time>TIME</a> |  hh:mm:ss.fs  | ignore | yes | Creation time
+1 <a href=Ged.GLOSSARY.md#subm>SUBM</a> | @XREF{1:22}@ | ignore | missing &#x26A0; | export SUBM tag to add
+1 <a href=Ged.GLOSSARY.md#subn>SUBN</a> | @XREF{1:22}@ | ignore | no | 
+1 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:90} | ignore | yes | name of gedcom file maked
+1 <a href=Ged.GLOSSARY.md#copr>COPR</a> | char{1:90} | ignore | no | 
+1 <a href=Ged.GLOSSARY.md#gedc>GEDC</a> |  | ignore &#x1F4CD; | yes | import should check GEDC.VERS and GEDC.Form
+2 <a href=Ged.GLOSSARY.md#vers>VERS</a> | char{1:15} | not checked &#x26A0; | 5.5 if non UTF8 and 5.5.1. if UTF8 &#x26A0; | always 5.5.1 must be assumed (some tag 5.5.1)
+2 <a href=Ged.GLOSSARY.md#form>FORM</a> |  LINEAGE-LINKED  | not checked &#x26A0; | yes | 
+1 <a href=Ged.GLOSSARY.md#char>CHAR</a> |  ANSEL \| &#x25B6; UTF-8 \| UNICODE \| &#x1F5D1; ASCII \| &#x23E9; ANSI \| &#x23E9; MACINTOSH  | plus MSDOS charset | ANSI missing &#x26A0; | ANSI and MACINTOSH charset missing &#x26A0; - <a href=https://github.com/geneweb/geneweb/issues/627>Issue #627</a>
+2 <a href=Ged.GLOSSARY.md#vers>VERS</a> | char{1:15} | ignore | no | 
+1 <a href=Ged.GLOSSARY.md#lang>LANG</a> | &lt;<a href=Ged.LANGUAGE_ID.md>LANGUAGE_ID</a>&gt; | ignore | no | 
+1 <a href=Ged.GLOSSARY.md#plac>PLAC</a> |  | ignore | no | &#x1F4CD; must be used for correct import of subdivision field (lieux dits)
+2 <a href=Ged.GLOSSARY.md#form>FORM</a> | char{1:120} | ignore | no &#x1F4CD; | can be used to detect subdivision position in place.
+1 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248} | record | optional (-nn gwb2ged option) | only the first page of chronicles/notes. &#x1F4CD; export all pages would be better.
+2 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | record | optional (-nn gwb2ged option) | 




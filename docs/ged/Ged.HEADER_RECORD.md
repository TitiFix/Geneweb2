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

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#head>HEAD</a> |  | | |
+1 <a href=Ged.GLOSSARY.md#sour>SOUR</a> | char{1:20} | | |
+2 <a href=Ged.GLOSSARY.md#vers>VERS</a> | char{1:15} | | |
+2 <a href=Ged.GLOSSARY.md#name>NAME</a> | char{1:90} | | |
+2 <a href=Ged.GLOSSARY.md#corp>CORP</a> | char{1:90} | | |
+3 <a href=Ged.GLOSSARY.md#addr>ADDR</a> | char{1:60} | | |
+4 <a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:60} | | |
+4 <a href=Ged.GLOSSARY.md#adr1>ADR1</a> | char{1:60} | | |
+4 <a href=Ged.GLOSSARY.md#adr2>ADR2</a> | char{1:60} | | |
+4 <a href=Ged.GLOSSARY.md#adr3>ADR3</a> | char{1:60} | | |
+4 <a href=Ged.GLOSSARY.md#city>CITY</a> | char{1:60} | | |
+4 <a href=Ged.GLOSSARY.md#stae>STAE</a> | char{1:60} | | |
+4 <a href=Ged.GLOSSARY.md#post>POST</a> | char{1:10} | | |
+4 <a href=Ged.GLOSSARY.md#ctry>CTRY</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#phon>PHON</a> | char{1:25} | | |
+3 <a href=Ged.GLOSSARY.md#email>EMAIL</a> | char{5:120} | | |
+3 <a href=Ged.GLOSSARY.md#fax>FAX</a> | char{5:60} | | |
+3 <a href=Ged.GLOSSARY.md#www>WWW</a> | char{5:120} | | |
+2 <a href=Ged.GLOSSARY.md#data>DATA</a> | char{1:90} | | |
+3 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_EXACT.md>DATE_EXACT</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#copr>COPR</a> | char{1:90} | | |
+4 <a href=Ged.GLOSSARY.md#cont>CONT</a>\|<a href=Ged.GLOSSARY.md#conc>CONC</a> | char{1:90} | | |
+1 <a href=Ged.GLOSSARY.md#dest>DEST</a> | char{1:20} | | |
+1 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_EXACT.md>DATE_EXACT</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#time>TIME</a> |  hh:mm:ss.fs  | | |
+1 <a href=Ged.GLOSSARY.md#subm>SUBM</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#subn>SUBN</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:90} | | |
+1 <a href=Ged.GLOSSARY.md#copr>COPR</a> | char{1:90} | | |
+1 <a href=Ged.GLOSSARY.md#gedc>GEDC</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#vers>VERS</a> | char{1:15} | | |
+2 <a href=Ged.GLOSSARY.md#form>FORM</a> |  LINEAGE-LINKED  | | |
+1 <a href=Ged.GLOSSARY.md#char>CHAR</a> |  ANSEL \| :play: UTF-8 \| UNICODE \| :wastebasket: ASCII \| :ff: ANSI \| :ff: MACINTOSH  | | |
+2 <a href=Ged.GLOSSARY.md#vers>VERS</a> | char{1:15} | | |
+1 <a href=Ged.GLOSSARY.md#lang>LANG</a> | &lt;<a href=Ged.LANGUAGE_ID.md>LANGUAGE_ID</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#plac>PLAC</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#form>FORM</a> | char{1:120} | | |
+1 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |

:warning: to be continued/checked


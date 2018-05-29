# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**HEADER_RECORD**:=
<pre>
<b>n HEAD{1:1}</b>
<b>  +1 SOUR &lt;<a href=Ged.APPROVED_SYSTEM_ID>APPROVED_SYSTEM_ID</a>&gt;{1:1}</b>
    +2 VERS &lt;<a href=Ged.VERSION_NUMBER>VERSION_NUMBER</a>&gt;{0:1}
    +2 NAME &lt;<a href=Ged.NAME_OF_PRODUCT>NAME_OF_PRODUCT</a>&gt;{0:1}
    +2 CORP &lt;<a href=Ged.NAME_OF_BUSINESS>NAME_OF_BUSINESS</a>&gt;{0:1}
      +3 &lt;&lt;<a href=Ged.ADDRESS_STRUCTURE>ADDRESS_STRUCTURE</a>&gt;&gt;{0:1}
    +2 DATA &lt;<a href=Ged.NAME_OF_SOURCE_DATA>NAME_OF_SOURCE_DATA</a>&gt;{0:1}
      +3 DATE &lt;<a href=Ged.PUBLICATION_DATE>PUBLICATION_DATE</a>&gt;{0:1}
      +3 COPR &lt;<a href=Ged.COPYRIGHT_SOURCE_DATA>COPYRIGHT_SOURCE_DATA</a>&gt;{0:1}
        +4 [CONT|CONC] &lt;<a href=Ged.COPYRIGHT_SOURCE_DATA>COPYRIGHT_SOURCE_DATA</a>&gt;{0:M}
  +1 DEST &lt;<a href=Ged.RECEIVING_SYSTEM_NAME>RECEIVING_SYSTEM_NAME</a>&gt;{0:1} *
  +1 DATE &lt;<a href=Ged.TRANSMISSION_DATE>TRANSMISSION_DATE</a>&gt;{0:1}
    +2 TIME &lt;<a href=Ged.TIME_VALUE>TIME_VALUE</a>&gt;{0:1}
<b>  +1 SUBM @&lt;<a href=Ged.XREF_SUBM>XREF:SUBM</a>&gt;@{1:1}</b>
  +1 SUBN @&lt;<a href=Ged.XREF_SUBN>XREF:SUBN</a>&gt;@{0:1}
  +1 FILE &lt;<a href=Ged.FILE_NAME>FILE_NAME</a>&gt;{0:1}
  +1 COPR &lt;<a href=Ged.COPYRIGHT_GEDCOM_FILE>COPYRIGHT_GEDCOM_FILE</a>&gt;{0:1}
<b>  +1 GEDC{1:1}</b>
<b>    +2 VERS &lt;<a href=Ged.VERSION_NUMBER>VERSION_NUMBER</a>&gt;{1:1}</b>
<b>    +2 FORM &lt;<a href=Ged.GEDCOM_FORM>GEDCOM_FORM</a>&gt;{1:1}</b>
<b>  +1 CHAR &lt;<a href=Ged.CHARACTER_SET>CHARACTER_SET</a>&gt;{1:1}</b>
    +2 VERS &lt;<a href=Ged.VERSION_NUMBER>VERSION_NUMBER</a>&gt;{0:1}
  +1 LANG &lt;<a href=Ged.LANGUAGE_OF_TEXT>LANGUAGE_OF_TEXT</a>&gt;{0:1}
  +1 PLAC{0:1}
<b>    +2 FORM &lt;<a href=Ged.PLACE_HIERARCHY>PLACE_HIERARCHY</a>&gt;{1:1}</b>
  +1 NOTE &lt;<a href=Ged.GEDCOM_CONTENT_DESCRIPTION>GEDCOM_CONTENT_DESCRIPTION</a>&gt;{0:1}
    +2 [CONC|CONT] &lt;<a href=Ged.GEDCOM_CONTENT_DESCRIPTION>GEDCOM_CONTENT_DESCRIPTION</a>&gt;{0:M}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE>LINEAGE_LINKED_STRUCTURE</a><br />


* NOTE:
Submissions to the Family History Department for Ancestral File submission or for clearing temple ordinances  must use a
DESTination of ANSTFILE or TempleReady, respectively.
# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+1 SOUR | APPROVED_SYSTEM_ID | | |
+2 VERS | VERSION_NUMBER | | |
+2 NAME | NAME_OF_PRODUCT | | |
+2 CORP | NAME_OF_BUSINESS | | |
+3 | ADDRESS_STRUCTURE | | |
+2 DATA | NAME_OF_SOURCE_DATA | | |
+3 DATE | PUBLICATION_DATE | | |
+3 COPR | COPYRIGHT_SOURCE_DATA | | |
+4 CONC/CONT | COPYRIGHT_SOURCE_DATA | | |
+1 DEST | RECEIVING_SYSTEM_NAME | | |
+1 DATE | TRANSMISSION_DATE | | |
+2 TIME | TIME_VALUE | | |
+1 SUBM | @ | | |
+1 SUBN | @ | | |
+1 FILE | FILE_NAME | | |
+1 COPR | COPYRIGHT_GEDCOM_FILE | | |
+2 VERS | VERSION_NUMBER | | |
+2 FORM | GEDCOM_FORM | | |
+1 CHAR | CHARACTER_SET | | |
+2 VERS | VERSION_NUMBER | | |
+1 LANG | LANGUAGE_OF_TEXT | | |
+2 FORM | PLACE_HIERARCHY | | |
+1 NOTE | GEDCOM_CONTENT_DESCRIPTION | | |
+2 CONC/CONT | GEDCOM_CONTENT_DESCRIPTION | | |

:warning: to be continued/checked


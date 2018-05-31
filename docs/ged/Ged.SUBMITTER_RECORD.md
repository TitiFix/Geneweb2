# SUBMITTER_RECORD
## Abstract
The submitter record identifies an individual or organization that contributed information contained
in the GEDCOM transmission. All records in the file are assumed to be submitted by the SUBMITTER referenced in the HEADer, unless a SUBMitter reference inside a specific record points at a different SUBMITTER record.


## GEDCOM syntax and proprietary extensions

**SUBMITTER_RECORD**:=
<pre>
<b>n @&lt;<a href=Ged.XREF_SUBM.md>XREF:SUBM</a>&gt;@ SUBM{1:1}</b>
<b>  +1 NAME &lt;<a href=Ged.SUBMITTER_NAME.md>SUBMITTER_NAME</a>&gt;{1:1}</b>
  +1 &lt;&lt;<a href=Ged.ADDRESS_STRUCTURE.md>ADDRESS_STRUCTURE</a>&gt;&gt;{0:1} *
  +1 &lt;&lt;<a href=Ged.MULTIMEDIA_LINK.md>MULTIMEDIA_LINK</a>&gt;&gt;{0:M}
  +1 LANG &lt;<a href=Ged.LANGUAGE_PREFERENCE.md>LANGUAGE_PREFERENCE</a>&gt;{0:3}
  +1 RFN &lt;<a href=Ged.SUBMITTER_REGISTERED_RFN.md>SUBMITTER_REGISTERED_RFN</a>&gt;{0:1}
  +1 RIN &lt;<a href=Ged.AUTOMATED_RECORD_ID.md>AUTOMATED_RECORD_ID</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.CHANGE_STRUCTURE.md>CHANGE_STRUCTURE</a>&gt;&gt;{0:1}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />


NOTE: submissions to the ancestral file require the name and address of the submitter.

## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#subm>SUBM</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#name>NAME</a> | char{1:60} | | |
+1 <a href=Ged.GLOSSARY.md#addr>ADDR</a> | char{1:60} | | |
+2 <a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:60} | | |
+2 <a href=Ged.GLOSSARY.md#adr1>ADR1</a> | char{1:60} | | |
+2 <a href=Ged.GLOSSARY.md#adr2>ADR2</a> | char{1:60} | | |
+2 <a href=Ged.GLOSSARY.md#adr3>ADR3</a> | char{1:60} | | |
+2 <a href=Ged.GLOSSARY.md#city>CITY</a> | char{1:60} | | |
+2 <a href=Ged.GLOSSARY.md#stae>STAE</a> | char{1:60} | | |
+2 <a href=Ged.GLOSSARY.md#post>POST</a> | char{1:10} | | |
+2 <a href=Ged.GLOSSARY.md#ctry>CTRY</a> | char{1:60} | | |
+1 <a href=Ged.GLOSSARY.md#phon>PHON</a> | char{1:25} | | |
+1 <a href=Ged.GLOSSARY.md#email>EMAIL</a> | char{5:120} | | |
+1 <a href=Ged.GLOSSARY.md#fax>FAX</a> | char{5:60} | | |
+1 <a href=Ged.GLOSSARY.md#www>WWW</a> | char{5:120} | | |
+1 <a href=Ged.GLOSSARY.md#obje>OBJE</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+3 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+2 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+4 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+1 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+2 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+3 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+1 <a href=Ged.GLOSSARY.md#lang>LANG</a> | &lt;<a href=Ged.LANGUAGE_ID.md>LANGUAGE_ID</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#rfn>RFN</a> | char{1:30} | | |
+1 <a href=Ged.GLOSSARY.md#rin>RIN</a> | char{1:12} | | |
+1 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+2 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+1 <a href=Ged.GLOSSARY.md#chan>CHAN</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_EXACT.md>DATE_EXACT</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#time>TIME</a> |  hh:mm:ss.fs  | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+3 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |

:warning: to be continued/checked


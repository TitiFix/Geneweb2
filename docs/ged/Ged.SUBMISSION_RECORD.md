﻿# SUBMISSION_RECORD
## Abstract
The sending system uses a submission record to send instructions and information to the receiving
system. TempleReady processes submission records to determine which temple the cleared records
should be directed to. The submission record is also used for communication between Ancestral File
download requests and TempleReady. Each GEDCOM file should have only one
submission record. Multiple submissions are handled by creating separate GEDCOM transmission
files.


## GEDCOM syntax and proprietary extensions

**SUBMISSION_RECORD**:=
<pre>
<b>n @&lt;<a href=Ged.XREF_SUBN.md>XREF:SUBN</a>&gt;@ SUBN{1:1}</b>
  +1 SUBM @&lt;<a href=Ged.XREF_SUBM.md>XREF:SUBM</a>&gt;@{0:1}
  +1 FAMF &lt;<a href=Ged.NAME_OF_FAMILY_FILE.md>NAME_OF_FAMILY_FILE</a>&gt;{0:1}
  +1 TEMP &lt;<a href=Ged.TEMPLE_CODE.md>TEMPLE_CODE</a>&gt;{0:1}
  +1 ANCE &lt;<a href=Ged.GENERATIONS_OF_ANCESTORS.md>GENERATIONS_OF_ANCESTORS</a>&gt;{0:1}
  +1 DESC &lt;<a href=Ged.GENERATIONS_OF_DESCENDANTS.md>GENERATIONS_OF_DESCENDANTS</a>&gt;{0:1}
  +1 ORDI &lt;<a href=Ged.ORDINANCE_PROCESS_FLAG.md>ORDINANCE_PROCESS_FLAG</a>&gt;{0:1}
  +1 RIN &lt;<a href=Ged.AUTOMATED_RECORD_ID.md>AUTOMATED_RECORD_ID</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.CHANGE_STRUCTURE.md>CHANGE_STRUCTURE</a>&gt;&gt;{0:1}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />


NOTE: :wastebasket: Since the discontinuation of the GEDCOM standard by familysearch, this record is no longer useful.

## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#subn>SUBN</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#subm>SUBM</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#famf>FAMF</a> | char{1:120} | | |
+1 <a href=Ged.GLOSSARY.md#temp>TEMP</a> | char{4:5} | | |
+1 <a href=Ged.GLOSSARY.md#ance>ANCE</a> | char{1:4} | | |
+1 <a href=Ged.GLOSSARY.md#desc>DESC</a> | char{1:4} | | |
+1 <a href=Ged.GLOSSARY.md#ordi>ORDI</a> |  yes \| no  | | |
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

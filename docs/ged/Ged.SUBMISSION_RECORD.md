# SUBMISSION_RECORD 🗑 (Deprecated record)
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


NOTE: &#x1F5D1; Since the discontinuation of the GEDCOM standard by familysearch, this record is no longer useful.

## Geneweb behavior

level tag  | Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#subn>SUBN</a> | @XREF{1:22}@ | ignore | no | not used by geneweb
+1 <a href=Ged.GLOSSARY.md#subm>SUBM</a> | @XREF{1:22}@ | ignore | no | 
+1 <a href=Ged.GLOSSARY.md#famf>FAMF</a> | char{1:120} | ignore | no | 
+1 <a href=Ged.GLOSSARY.md#temp>TEMP</a> | char{4:5} | ignore | no | 
+1 <a href=Ged.GLOSSARY.md#ance>ANCE</a> | 🗑 deprecated | ignore | no | 
+1 <a href=Ged.GLOSSARY.md#desc>DESC</a> | 🗑 deprecated | ignore | no | 
+1 <a href=Ged.GLOSSARY.md#ordi>ORDI</a> |  yes \| no  | ignore | no | 
+1 <a href=Ged.GLOSSARY.md#rin>RIN</a> | char{1:12} | ignore | no | 
+1  | &lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt; | ignore | no | 
+1  | &lt;<a href=Ged.CHANGE_STRUCTURE.md>CHANGE_STRUCTURE</a>&gt; | ignore | no | 




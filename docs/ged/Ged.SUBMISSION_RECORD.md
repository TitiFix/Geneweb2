# SUBMISSION_RECORD
## Abstract
The sending system uses a submission record to send instructions and information to the receiving
system. TempleReady processes submission records to determine which temple the cleared records
should be directed to. The submission record is also used for communication between Ancestral File
download requests and TempleReady. Each GEDCOM transmission file should have only one
submission record. Multiple submissions are handled by creating separate GEDCOM transmission
files.


## GEDCOM syntax and proprietary extensions
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**SUBMISSION_RECORD**:=
<pre>
<b>n @&lt;<a href=Ged.XREF_SUBN.md>XREF:SUBN</a>&gt;@ SUBN{1:1}</b>
  +1 SUBM @XREF:SUBM@{0:1}
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
+0 <a href=Ged.GLOSSARY.md#SUBN>SUBN</a> | @XREF:SUBN@ | | |
+1 <a href=Ged.GLOSSARY.md#SUBM>SUBM</a> | @XREF:SUBM@ | | |
+1 <a href=Ged.GLOSSARY.md#FAMF>FAMF</a> | NAME_OF_FAMILY_FILE | | |
+1 <a href=Ged.GLOSSARY.md#TEMP>TEMP</a> | TEMPLE_CODE | | |
+1 <a href=Ged.GLOSSARY.md#ANCE>ANCE</a> | GENERATIONS_OF_ANCESTORS | | |
+1 <a href=Ged.GLOSSARY.md#DESC>DESC</a> | GENERATIONS_OF_DESCENDANTS | | |
+1 <a href=Ged.GLOSSARY.md#ORDI>ORDI</a> | ORDINANCE_PROCESS_FLAG | | |
+1 <a href=Ged.GLOSSARY.md#RIN>RIN</a> | AUTOMATED_RECORD_ID | | |
+1  | NOTE_STRUCTURE | | |
+1  | CHANGE_STRUCTURE | | |

:warning: to be continued/checked


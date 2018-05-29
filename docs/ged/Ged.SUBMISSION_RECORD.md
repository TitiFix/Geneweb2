# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**SUBMISSION_RECORD**:=
<pre>
<b>n @&lt;<a href=Ged.XREF_SUBN>XREF:SUBN</a>&gt;@ SUBN{1:1}</b>
  +1 SUBM @XREF:SUBM@{0:1}
  +1 FAMF &lt;<a href=Ged.NAME_OF_FAMILY_FILE>NAME_OF_FAMILY_FILE</a>&gt;{0:1}
  +1 TEMP &lt;<a href=Ged.TEMPLE_CODE>TEMPLE_CODE</a>&gt;{0:1}
  +1 ANCE &lt;<a href=Ged.GENERATIONS_OF_ANCESTORS>GENERATIONS_OF_ANCESTORS</a>&gt;{0:1}
  +1 DESC &lt;<a href=Ged.GENERATIONS_OF_DESCENDANTS>GENERATIONS_OF_DESCENDANTS</a>&gt;{0:1}
  +1 ORDI &lt;<a href=Ged.ORDINANCE_PROCESS_FLAG>ORDINANCE_PROCESS_FLAG</a>&gt;{0:1}
  +1 RIN &lt;<a href=Ged.AUTOMATED_RECORD_ID>AUTOMATED_RECORD_ID</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.CHANGE_STRUCTURE>CHANGE_STRUCTURE</a>&gt;&gt;{0:1}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE>LINEAGE_LINKED_STRUCTURE</a><br />

# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
n@ | XREF:SUBN | | |
+1 FAMF | NAME_OF_FAMILY_FILE | | |
+1 TEMP | TEMPLE_CODE | | |
+1 ANCE | GENERATIONS_OF_ANCESTORS | | |
+1 DESC | GENERATIONS_OF_DESCENDANTS | | |
+1 ORDI | ORDINANCE_PROCESS_FLAG | | |
+1 RIN | AUTOMATED_RECORD_ID | | |
+1 | NOTE_STRUCTURE | | |
+1 | CHANGE_STRUCTURE | | |

:warning: to be continued/checked


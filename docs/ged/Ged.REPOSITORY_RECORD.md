# REPOSITORY_RECORD
## Abstract


## GEDCOM syntax and proprietary extensions
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**REPOSITORY_RECORD**:=
<pre>
<b>n @&lt;<a href=Ged.XREF_REPO.md>XREF:REPO</a>&gt;@ REPO{1:1}</b>
<b>  +1 NAME &lt;<a href=Ged.NAME_OF_REPOSITORY.md>NAME_OF_REPOSITORY</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.ADDRESS_STRUCTURE.md>ADDRESS_STRUCTURE</a>&gt;&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 REFN &lt;<a href=Ged.USER_REFERENCE_NUMBER.md>USER_REFERENCE_NUMBER</a>&gt;{0:M}
    +2 TYPE &lt;<a href=Ged.USER_REFERENCE_TYPE.md>USER_REFERENCE_TYPE</a>&gt;{0:1}
  +1 RIN &lt;<a href=Ged.AUTOMATED_RECORD_ID.md>AUTOMATED_RECORD_ID</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.CHANGE_STRUCTURE.md>CHANGE_STRUCTURE</a>&gt;&gt;{0:1}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#repo>REPO</a> | @XREF:REPO@ | | |
+1 <a href=Ged.GLOSSARY.md#name>NAME</a> | NAME_OF_REPOSITORY | | |
+1  | ADDRESS_STRUCTURE | | |
+1  | NOTE_STRUCTURE | | |
+1 <a href=Ged.GLOSSARY.md#refn>REFN</a> | USER_REFERENCE_NUMBER | | |
+2 <a href=Ged.GLOSSARY.md#type>TYPE</a> | USER_REFERENCE_TYPE | | |
+1 <a href=Ged.GLOSSARY.md#rin>RIN</a> | AUTOMATED_RECORD_ID | | |
+1  | CHANGE_STRUCTURE | | |

:warning: to be continued/checked


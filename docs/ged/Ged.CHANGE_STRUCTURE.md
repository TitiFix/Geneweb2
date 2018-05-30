# CHANGE_STRUCTURE
## Abstract
The change date is intended to only record the last change to a record.  Some systems may want to
manage the change process with more detail, but it is sufficient for GEDCOM purposes to indicate
the last time that a record was modified.


## GEDCOM syntax and proprietary extensions
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**CHANGE_STRUCTURE**:=
<pre>
<b>n CHAN{1:1}</b>
<b>  +1 DATE &lt;<a href=Ged.CHANGE_DATE.md>CHANGE_DATE</a>&gt;{1:1}</b>
    +2 TIME &lt;<a href=Ged.TIME_VALUE.md>TIME_VALUE</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#chan>CHAN</a> |  | | |
+1 <a href=Ged.GLOSSARY.md#date>DATE</a> | CHANGE_DATE | | |
+2 <a href=Ged.GLOSSARY.md#time>TIME</a> | TIME_VALUE | | |
+1  | NOTE_STRUCTURE | | |

:warning: to be continued/checked


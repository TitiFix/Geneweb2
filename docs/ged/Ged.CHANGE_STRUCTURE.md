# CHANGE_STRUCTURE
## Abstract
The change date is intended to only record the last change to a record.  Some systems may want to
manage the change process with more detail, but it is sufficient for GEDCOM purposes to indicate
the last time that a record was modified.


## GEDCOM syntax and proprietary extensions

**CHANGE_STRUCTURE**:=
<pre>
<b>n CHAN{1:1}</b>
<b>  +1 DATE &lt;<a href=Ged.CHANGE_DATE.md>CHANGE_DATE</a>&gt;{1:1}</b>
    +2 TIME &lt;<a href=Ged.TIME_VALUE.md>TIME_VALUE</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
</pre>
Used in <a href=Ged.FAM_RECORD.md>FAM_RECORD</a>, <a href=Ged.INDIVIDUAL_RECORD.md>INDIVIDUAL_RECORD</a>, <a href=Ged.MULTIMEDIA_RECORD.md>MULTIMEDIA_RECORD</a>, <a href=Ged.NOTE_RECORD.md>NOTE_RECORD</a>, <a href=Ged.REPOSITORY_RECORD.md>REPOSITORY_RECORD</a>, <a href=Ged.SOURCE_RECORD.md>SOURCE_RECORD</a>, <a href=Ged.SUBMISSION_RECORD.md>SUBMISSION_RECORD</a>, <a href=Ged.SUBMITTER_RECORD.md>SUBMITTER_RECORD</a><br />


## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#chan>CHAN</a> |  | | |
+1 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_EXACT.md>DATE_EXACT</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#time>TIME</a> |  hh:mm:ss.fs  | | |
+1 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+2 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |

:warning: to be continued/checked


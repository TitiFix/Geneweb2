# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**CHANGE_STRUCTURE**:=
<pre>
<b>n CHAN{1:1}</b>
<b>  +1 DATE &lt;<a href=Ged.CHANGE_DATE>CHANGE_DATE</a>&gt;{1:1}</b>
    +2 TIME &lt;<a href=Ged.TIME_VALUE>TIME_VALUE</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
</pre>
Used in <a href=Ged.FAM_RECORD>FAM_RECORD</a>, <a href=Ged.INDIVIDUAL_RECORD>INDIVIDUAL_RECORD</a>, <a href=Ged.MULTIMEDIA_RECORD>MULTIMEDIA_RECORD</a>, <a href=Ged.NOTE_RECORD>NOTE_RECORD</a>, <a href=Ged.REPOSITORY_RECORD>REPOSITORY_RECORD</a>, <a href=Ged.SOURCE_RECORD>SOURCE_RECORD</a>, <a href=Ged.SUBMISSION_RECORD>SUBMISSION_RECORD</a>, <a href=Ged.SUBMITTER_RECORD>SUBMITTER_RECORD</a><br />

# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+1 DATE | CHANGE_DATE | | |
+2 TIME | TIME_VALUE | | |
+1 | NOTE_STRUCTURE | | |

:warning: to be continued/checked


# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**NOTE_STRUCTURE**:=
<pre>
[
<b>n NOTE @&lt;<a href=Ged.XREF_NOTE>XREF:NOTE</a>&gt;@ {1:1}</b>
|
<b>n NOTE [&lt;<a href=Ged.SUBMITTER_TEXT>SUBMITTER_TEXT</a>&gt; | &lt;<a href=Ged.NULL>NULL</a>&gt;] {1:1}</b>
  +1 [CONC|CONT] &lt;<a href=Ged.SUBMITTER_TEXT>SUBMITTER_TEXT</a>&gt; {0:M}
]
</pre>
Used in <a href=Ged.FAM_RECORD>FAM_RECORD</a>, <a href=Ged.INDIVIDUAL_RECORD>INDIVIDUAL_RECORD</a>, <a href=Ged.MULTIMEDIA_RECORD>MULTIMEDIA_RECORD</a>, <a href=Ged.REPOSITORY_RECORD>REPOSITORY_RECORD</a>, <a href=Ged.SOURCE_RECORD>SOURCE_RECORD</a>, <a href=Ged.SUBMISSION_RECORD>SUBMISSION_RECORD</a>, <a href=Ged.SUBMITTER_RECORD>SUBMITTER_RECORD</a>, <a href=Ged.ASSOCIATION_STRUCTURE>ASSOCIATION_STRUCTURE</a>, <a href=Ged.CHANGE_STRUCTURE>CHANGE_STRUCTURE</a>, <a href=Ged.CHILD_TO_FAMILY_LINK>CHILD_TO_FAMILY_LINK</a>, <a href=Ged.EVENT_DETAIL>EVENT_DETAIL</a>, <a href=Ged.LDS_INDIVIDUAL_ORDINANCE>LDS_INDIVIDUAL_ORDINANCE</a>, <a href=Ged.LDS_SPOUSE_SEALING>LDS_SPOUSE_SEALING</a>, <a href=Ged.PERSONAL_NAME_PIECES>PERSONAL_NAME_PIECES</a>, <a href=Ged.PLACE_STRUCTURE>PLACE_STRUCTURE</a>, <a href=Ged.SOURCE_CITATION>SOURCE_CITATION</a>, <a href=Ged.SOURCE_REPOSITORY_CITATION>SOURCE_REPOSITORY_CITATION</a>, <a href=Ged.SPOUSE_TO_FAMILY_LINK>SPOUSE_TO_FAMILY_LINK</a><br />


* NOTE : There are special considerations required when using the CONC tag. The usage is to provide a
n ote string that can be concatenated together so that the display program can do its own word
wrapping according to its display window size. The requirement for usage is to either break the text
line in the middle of a word, or if at the end of a word, to add a space to the first of the next CONC
line. Otherwise most operating systems will strip off the trailing space and the space is lost in the
reconstitution of the note.
# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
nNOTE @ | XREF:NOTE | | |
nNOTE [ | SUBMITTER_TEXT | | |
nNOTE [<SUBMITTER_TEXT> | | | | |
+1 CONC/CONT | SUBMITTER_TEXT | | |

:warning: to be continued/checked


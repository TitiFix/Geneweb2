# NOTE_STRUCTURE
## Abstract

## GEDCOM syntax and proprietary extensions

**NOTE_STRUCTURE**:=
<pre>
[
<b>n NOTE @&lt;<a href=Ged.XREF_NOTE.md>XREF:NOTE</a>&gt;@ {1:1}</b>
|
<b>n NOTE [&lt;<a href=Ged.SUBMITTER_TEXT.md>SUBMITTER_TEXT</a>&gt; | &lt;<a href=Ged.NULL.md>NULL</a>&gt;] {1:1}</b>
  +1 [CONC|CONT] &lt;<a href=Ged.SUBMITTER_TEXT.md>SUBMITTER_TEXT</a>&gt; {0:M}
]
</pre>
Used in <a href=Ged.FAMILY_RECORD.md>FAMILY_RECORD</a>, <a href=Ged.INDIVIDUAL_RECORD.md>INDIVIDUAL_RECORD</a>, <a href=Ged.MULTIMEDIA_RECORD.md>MULTIMEDIA_RECORD</a>, <a href=Ged.REPOSITORY_RECORD.md>REPOSITORY_RECORD</a>, <a href=Ged.SOURCE_RECORD.md>SOURCE_RECORD</a>, <a href=Ged.SUBMISSION_RECORD.md>SUBMISSION_RECORD</a>, <a href=Ged.SUBMITTER_RECORD.md>SUBMITTER_RECORD</a>, <a href=Ged.ASSOCIATION_STRUCTURE.md>ASSOCIATION_STRUCTURE</a>, <a href=Ged.CHANGE_STRUCTURE.md>CHANGE_STRUCTURE</a>, <a href=Ged.CHILD_TO_FAMILY_LINK.md>CHILD_TO_FAMILY_LINK</a>, <a href=Ged.FAMILY_EVENT_DETAIL.md>FAMILY_EVENT_DETAIL</a>, <a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>, <a href=Ged.LDS_INDIVIDUAL_ORDINANCE.md>LDS_INDIVIDUAL_ORDINANCE</a>, <a href=Ged.LDS_SPOUSE_SEALING.md>LDS_SPOUSE_SEALING</a>, <a href=Ged.PERSONAL_NAME_PIECES.md>PERSONAL_NAME_PIECES</a>, <a href=Ged.PLACE_STRUCTURE.md>PLACE_STRUCTURE</a>, <a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>, <a href=Ged.SOURCE_REPOSITORY_CITATION.md>SOURCE_REPOSITORY_CITATION</a>, <a href=Ged.SPOUSE_TO_FAMILY_LINK.md>SPOUSE_TO_FAMILY_LINK</a><br />


NOTE: There are special considerations required when using the CONC tag. The usage is to provide a
n ote string that can be concatenated together so that the display program can do its own word
wrapping according to its display window size. The requirement for usage is to either break the text
line in the middle of a word, or if at the end of a word, to add a space to the first of the next CONC
line. Otherwise most operating systems will strip off the trailing space and the space is lost in the
reconstitution of the note.

## Geneweb behavior

level tag  | Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | ? | no | 
+0 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | yes | yes | export with text cut to 78 characters each CONC tag needed.
+1 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | yes | yes | 

You must refer to the calling structure to see if this structure is used or not by Geneweb. If used, the behavior is as described above. if there are several notes for the same structure. These notes are concatenated.



<!-- licence GPL V2, cf https://github.com/TitiFix/geneweb -->
# NOTE_STRUCTURE
## Abstract
Additional information provided by the submitter for understanding the enclosing data.


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


NOTE: see special considerations required when using the &lt;<a href=Ged.GLOSSARY.md#conc>CONC</a>&gt; tag.

## Geneweb behavior



level tag  | Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | yes | no &#x1F4CD; | It's must be useful to separate multi notes by &lt;hr&gt; tag separate note durant export.
+0 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | yes | yes | export with text cut to 78 characters each CONC tag needed.
+1 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | yes | yes | 

You must refer to the calling structure to see if this structure is used or not by Geneweb. If used, the behavior is as described above. If there are several notes for the same structure. In this case notes are concatenated by Geneweb with &lt;br&gt; HTML tag ( one database per event ). Export generate only one note (each notes ends with CONT tag)



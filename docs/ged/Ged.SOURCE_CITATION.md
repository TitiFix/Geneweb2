# SOURCE_CITATION
## Abstract
The data provided in the &lt;&lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt;&gt; structure is source-related information specific to the data being cited. Systems that do not use a (SOURCE_RECORD)  must use the non-preferred second SOURce citation structure option.


## GEDCOM syntax and proprietary extensions

**SOURCE_CITATION**:=
<pre>
[ (* pointer to source record (preferred)*)
<b>n SOUR @&lt;<a href=Ged.XREF_SOUR.md>XREF:SOUR</a>&gt;@   {1:1}</b>
  +1 PAGE &lt;<a href=Ged.WHERE_WITHIN_SOURCE.md>WHERE_WITHIN_SOURCE</a>&gt;{0:1}
  +1 EVEN &lt;<a href=Ged.EVENT_TYPE_CITED_FROM.md>EVENT_TYPE_CITED_FROM</a>&gt;{0:1}
    +2 ROLE &lt;<a href=Ged.ROLE_IN_EVENT.md>ROLE_IN_EVENT</a>&gt;{0:1}
  +1 DATA{0:1}
    +2 DATE &lt;<a href=Ged.ENTRY_RECORDING_DATE.md>ENTRY_RECORDING_DATE</a>&gt;{0:1}
    +2 TEXT &lt;<a href=Ged.TEXT_FROM_SOURCE.md>TEXT_FROM_SOURCE</a>&gt;{0:M}
      +3 [CONC|CONT] &lt;<a href=Ged.TEXT_FROM_SOURCE.md>TEXT_FROM_SOURCE</a>&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.MULTIMEDIA_LINK.md>MULTIMEDIA_LINK</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 QUAY &lt;<a href=Ged.CERTAINTY_ASSESSMENT.md>CERTAINTY_ASSESSMENT</a>&gt;{0:1}
|(* Systems not using source records *)
<b>n SOUR &lt;<a href=Ged.SOURCE_DESCRIPTION.md>SOURCE_DESCRIPTION</a>&gt;{1:1}</b>
  +1 [CONC|CONT] &lt;<a href=Ged.SOURCE_DESCRIPTION.md>SOURCE_DESCRIPTION</a>&gt;{0:M}
  +1 TEXT &lt;<a href=Ged.TEXT_FROM_SOURCE.md>TEXT_FROM_SOURCE</a>&gt;{0:M}
    +2 [CONC|CONT] &lt;<a href=Ged.TEXT_FROM_SOURCE.md>TEXT_FROM_SOURCE</a>&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.MULTIMEDIA_LINK.md>MULTIMEDIA_LINK</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 QUAY &lt;<a href=Ged.CERTAINTY_ASSESSMENT.md>CERTAINTY_ASSESSMENT</a>&gt;{0:1}
]
</pre>
Used in <a href=Ged.FAMILY_RECORD.md>FAMILY_RECORD</a>, <a href=Ged.INDIVIDUAL_RECORD.md>INDIVIDUAL_RECORD</a>, <a href=Ged.MULTIMEDIA_RECORD.md>MULTIMEDIA_RECORD</a>, <a href=Ged.NOTE_RECORD.md>NOTE_RECORD</a>, <a href=Ged.ASSOCIATION_STRUCTURE.md>ASSOCIATION_STRUCTURE</a>, <a href=Ged.EVENT_DETAIL.md>EVENT_DETAIL</a>, <a href=Ged.LDS_INDIVIDUAL_ORDINANCE.md>LDS_INDIVIDUAL_ORDINANCE</a>, <a href=Ged.LDS_SPOUSE_SEALING.md>LDS_SPOUSE_SEALING</a>, <a href=Ged.PERSONAL_NAME_PIECES.md>PERSONAL_NAME_PIECES</a>, <a href=Ged.PLACE_STRUCTURE.md>PLACE_STRUCTURE</a><br />


NOTE: When systems that support the zero level source record format encounters a source citation that does not
contain pointers to source records, then that system needs to create a SOURCE_RECORD format
and store the source description information found in the non-structured source citation in the title
area for the new source record.
The information intended to be placed in the citation structure includes:
!The pointer to the SOURCE_RECORD, which contains a more general description of the source
used for the fact being cited.
!Information, such as a page number, to help the user find the cited data within the referenced
source. This is stored in the “.SOUR.PAGE” tag context.
!Actual text from the source that was used in making assertions, for example a date phrase as
actually recorded in the source, or significant notes written by the recorder, or an applicable
sentence from a letter. This is stored in the “.SOUR.DATA.TEXT” tag context.
!Data that allows an assessment of the relative value of one source over another for making the
recorded assertions (primary or secondary source, etc.).  Data needed for this assessment is data
that would help determine  how much time from the date of the asserted fact and when the source
was actually recorded, what type of event was cited, and what type of role did this person have in
the cited source.
-Date when the entry was recorded in source document is stored in the
".SOUR.DATA.DATE" tag context.
-The type of event that initiated the recording is stored in the “SOUR.EVEN” tag context. The
value used is the event code taken from the table of choices shown in the EVENT_TYPE_CITED_FROM primitive
-The role of this person in the event is stored in the ".SOUR.EVEN.ROLE" context.

## Geneweb behavior

level tag  | Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#sour>SOUR</a> | @XREF{1:22}@ | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#page>PAGE</a> | char{1:248} | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#even>EVEN</a> | &lt;<a href=Ged.EVENT_TYPE_CITED_FROM.md>EVENT_TYPE_CITED_FROM</a>&gt; | ? | ? | 
+2 <a href=Ged.GLOSSARY.md#role>ROLE</a> | &lt;<a href=Ged.ROLE_IN_EVENT.md>ROLE_IN_EVENT</a>&gt; | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#data>DATA</a> |  | ? | ? | 
+2 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | ? | ? | 
+2 <a href=Ged.GLOSSARY.md#text>TEXT</a> | char{1:248} | ? | ? | 
+3 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | ? | ? | 
+1  | &lt;<a href=Ged.MULTIMEDIA_LINK.md>MULTIMEDIA_LINK</a>&gt; | ? | ? | 
+1  | &lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt; | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#quay>QUAY</a> |  0 \| 1 \| 2 \| 3  | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#sour>SOUR</a> | char{1:248} | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#text>TEXT</a> | char{1:248} | ? | ? | 
+2 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | ? | ? | 
+1  | &lt;<a href=Ged.MULTIMEDIA_LINK.md>MULTIMEDIA_LINK</a>&gt; | ? | ? | 
+1  | &lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt; | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#quay>QUAY</a> |  0 \| 1 \| 2 \| 3  | ? | ? | 

🚧 to be continued/checked


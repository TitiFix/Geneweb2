# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**SOURCE_CITATION**:=
<pre>
[/* pointer to source record (preferred)*/
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
|/* Systems not using source records */
<b>n SOUR &lt;<a href=Ged.SOURCE_DESCRIPTION.md>SOURCE_DESCRIPTION</a>&gt;{1:1}</b>
  +1 [CONC|CONT] &lt;<a href=Ged.SOURCE_DESCRIPTION.md>SOURCE_DESCRIPTION</a>&gt;{0:M}
  +1 TEXT &lt;<a href=Ged.TEXT_FROM_SOURCE.md>TEXT_FROM_SOURCE</a>&gt;{0:M}
    +2 [CONC|CONT] &lt;<a href=Ged.TEXT_FROM_SOURCE.md>TEXT_FROM_SOURCE</a>&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.MULTIMEDIA_LINK.md>MULTIMEDIA_LINK</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 QUAY &lt;<a href=Ged.CERTAINTY_ASSESSMENT.md>CERTAINTY_ASSESSMENT</a>&gt;{0:1}
]
</pre>
Used in <a href=Ged.FAM_RECORD.md>FAM_RECORD</a>, <a href=Ged.INDIVIDUAL_RECORD.md>INDIVIDUAL_RECORD</a>, <a href=Ged.MULTIMEDIA_RECORD.md>MULTIMEDIA_RECORD</a>, <a href=Ged.NOTE_RECORD.md>NOTE_RECORD</a>, <a href=Ged.ASSOCIATION_STRUCTURE.md>ASSOCIATION_STRUCTURE</a>, <a href=Ged.EVENT_DETAIL.md>EVENT_DETAIL</a>, <a href=Ged.LDS_INDIVIDUAL_ORDINANCE.md>LDS_INDIVIDUAL_ORDINANCE</a>, <a href=Ged.LDS_SPOUSE_SEALING.md>LDS_SPOUSE_SEALING</a>, <a href=Ged.PERSONAL_NAME_PIECES.md>PERSONAL_NAME_PIECES</a><br />

# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
nSOUR @ | XREF:SOUR | | |
+1 PAGE | WHERE_WITHIN_SOURCE | | |
+1 EVEN | EVENT_TYPE_CITED_FROM | | |
+2 ROLE | ROLE_IN_EVENT | | |
+2 DATE | ENTRY_RECORDING_DATE | | |
+2 TEXT | TEXT_FROM_SOURCE | | |
+3 CONC/CONT | TEXT_FROM_SOURCE | | |
+1 | MULTIMEDIA_LINK | | |
+1 | NOTE_STRUCTURE | | |
+1 QUAY | CERTAINTY_ASSESSMENT | | |
nSOUR | SOURCE_DESCRIPTION | | |
+1 CONC/CONT | SOURCE_DESCRIPTION | | |
+1 TEXT | TEXT_FROM_SOURCE | | |
+2 CONC/CONT | TEXT_FROM_SOURCE | | |
+1 | MULTIMEDIA_LINK | | |
+1 | NOTE_STRUCTURE | | |
+1 QUAY | CERTAINTY_ASSESSMENT | | |

:warning: to be continued/checked


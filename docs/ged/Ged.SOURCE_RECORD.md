# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**SOURCE_RECORD**:=
<pre>
<b>n @&lt;<a href=Ged.XREF_SOUR>XREF:SOUR</a>&gt;@ SOUR{1:1}</b>
  +1 DATA{0:1}
    +2 EVEN &lt;<a href=Ged.EVENTS_RECORDED>EVENTS_RECORDED</a>&gt;{0:M}
      +3 DATE &lt;<a href=Ged.DATE_PERIOD>DATE_PERIOD</a>&gt;{0:1}
      +3 PLAC &lt;<a href=Ged.SOURCE_JURISDICTION_PLACE>SOURCE_JURISDICTION_PLACE</a>&gt;{0:1}
    +2 AGNC &lt;<a href=Ged.RESPONSIBLE_AGENCY>RESPONSIBLE_AGENCY</a>&gt;{0:1}
    +2 &lt;&lt;<a href=Ged.NOTE_STRUCTURE>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 AUTH &lt;<a href=Ged.SOURCE_ORIGINATOR>SOURCE_ORIGINATOR</a>&gt;{0:1}
    +2 [CONC|CONT] &lt;<a href=Ged.SOURCE_ORIGINATOR>SOURCE_ORIGINATOR</a>&gt;{0:M}
  +1 TITL &lt;<a href=Ged.SOURCE_DESCRIPTIVE_TITLE>SOURCE_DESCRIPTIVE_TITLE</a>&gt;{0:1}
    +2 [CONC|CONT] &lt;<a href=Ged.SOURCE_DESCRIPTIVE_TITLE>SOURCE_DESCRIPTIVE_TITLE</a>&gt;{0:M}
  +1 ABBR &lt;<a href=Ged.SOURCE_FILED_BY_ENTRY>SOURCE_FILED_BY_ENTRY</a>&gt;{0:1}
  +1 PUBL &lt;<a href=Ged.SOURCE_PUBLICATION_FACTS>SOURCE_PUBLICATION_FACTS</a>&gt;{0:1}
    +2 [CONC|CONT] &lt;<a href=Ged.SOURCE_PUBLICATION_FACTS>SOURCE_PUBLICATION_FACTS</a>&gt;{0:M}
  +1 TEXT &lt;<a href=Ged.TEXT_FROM_SOURCE>TEXT_FROM_SOURCE</a>&gt;{0:1}
    +2 [CONC|CONT] &lt;<a href=Ged.TEXT_FROM_SOURCE>TEXT_FROM_SOURCE</a>&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.SOURCE_REPOSITORY_CITATION>SOURCE_REPOSITORY_CITATION</a>&gt;&gt;{0:M}
  +1 REFN &lt;<a href=Ged.USER_REFERENCE_NUMBER>USER_REFERENCE_NUMBER</a>&gt;{0:M}
    +2 TYPE &lt;<a href=Ged.USER_REFERENCE_TYPE>USER_REFERENCE_TYPE</a>&gt;{0:1}
  +1 RIN &lt;<a href=Ged.AUTOMATED_RECORD_ID>AUTOMATED_RECORD_ID</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.CHANGE_STRUCTURE>CHANGE_STRUCTURE</a>&gt;&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.MULTIMEDIA_LINK>MULTIMEDIA_LINK</a>&gt;&gt;{0:M}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE>LINEAGE_LINKED_STRUCTURE</a><br />

# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
n@ | XREF:SOUR | | |
+2 EVEN | EVENTS_RECORDED | | |
+3 DATE | DATE_PERIOD | | |
+3 PLAC | SOURCE_JURISDICTION_PLACE | | |
+2 AGNC | RESPONSIBLE_AGENCY | | |
+2 | NOTE_STRUCTURE | | |
+1 AUTH | SOURCE_ORIGINATOR | | |
+2 CONC/CONT | SOURCE_ORIGINATOR | | |
+1 TITL | SOURCE_DESCRIPTIVE_TITLE | | |
+2 CONC/CONT | SOURCE_DESCRIPTIVE_TITLE | | |
+1 ABBR | SOURCE_FILED_BY_ENTRY | | |
+1 PUBL | SOURCE_PUBLICATION_FACTS | | |
+2 CONC/CONT | SOURCE_PUBLICATION_FACTS | | |
+1 TEXT | TEXT_FROM_SOURCE | | |
+2 CONC/CONT | TEXT_FROM_SOURCE | | |
+1 | SOURCE_REPOSITORY_CITATION | | |
+1 REFN | USER_REFERENCE_NUMBER | | |
+2 TYPE | USER_REFERENCE_TYPE | | |
+1 RIN | AUTOMATED_RECORD_ID | | |
+1 | CHANGE_STRUCTURE | | |
+1 | NOTE_STRUCTURE | | |
+1 | MULTIMEDIA_LINK | | |

:warning: to be continued/checked


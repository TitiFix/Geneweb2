# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**LDS_INDIVIDUAL_ORDINANCE**:=
<pre>
[
<b>n [ BAPL | CONL ]{1:1}</b>
  +1 DATE &lt;<a href=Ged.DATE_LDS_ORD>DATE_LDS_ORD</a>&gt;{0:1}
  +1 TEMP &lt;<a href=Ged.TEMPLE_CODE>TEMPLE_CODE</a>&gt;{0:1}
  +1 PLAC &lt;<a href=Ged.PLACE_LIVING_ORDINANCE>PLACE_LIVING_ORDINANCE</a>&gt;{0:1}
  +1 STAT &lt;<a href=Ged.LDS_BAPTISM_DATE_STATUS>LDS_BAPTISM_DATE_STATUS</a>&gt;{0:1}
<b>    +2 DATE &lt;<a href=Ged.CHANGE_DATE>CHANGE_DATE</a>&gt;{1:1}</b>
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.SOURCE_CITATION>SOURCE_CITATION</a>&gt;&gt;{0:M}
|
<b>n ENDL{1:1}</b>
  +1 DATE &lt;<a href=Ged.DATE_LDS_ORD>DATE_LDS_ORD</a>&gt;{0:1}
  +1 TEMP &lt;<a href=Ged.TEMPLE_CODE>TEMPLE_CODE</a>&gt;{0:1}
  +1 PLAC &lt;<a href=Ged.PLACE_LIVING_ORDINANCE>PLACE_LIVING_ORDINANCE</a>&gt;{0:1}
  +1 STAT &lt;<a href=Ged.LDS_ENDOWMENT_DATE_STATUS>LDS_ENDOWMENT_DATE_STATUS</a>&gt;{0:1}
<b>    +2 DATE &lt;<a href=Ged.CHANGE_DATE>CHANGE_DATE</a>&gt;{1:1}</b>
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.SOURCE_CITATION>SOURCE_CITATION</a>&gt;&gt;{0:M}
|
<b>n SLGC{1:1}</b>
  +1 DATE &lt;<a href=Ged.DATE_LDS_ORD>DATE_LDS_ORD</a>&gt;{0:1}
  +1 TEMP &lt;<a href=Ged.TEMPLE_CODE>TEMPLE_CODE</a>&gt;{0:1}
  +1 PLAC &lt;<a href=Ged.PLACE_LIVING_ORDINANCE>PLACE_LIVING_ORDINANCE</a>&gt;{0:1}
<b>  +1 FAMC @&lt;<a href=Ged.XREF_FAM>XREF:FAM</a>&gt;@{1:1}</b>
  +1 STAT &lt;<a href=Ged.LDS_CHILD_SEALING_DATE_STATUS>LDS_CHILD_SEALING_DATE_STATUS</a>&gt;{0:1}
<b>    +2 DATE &lt;<a href=Ged.CHANGE_DATE>CHANGE_DATE</a>&gt;{1:1}</b>
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.SOURCE_CITATION>SOURCE_CITATION</a>&gt;&gt;{0:M}
]
</pre>
Used in <a href=Ged.INDIVIDUAL_RECORD>INDIVIDUAL_RECORD</a><br />

# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+1 DATE | DATE_LDS_ORD | | |
+1 TEMP | TEMPLE_CODE | | |
+1 PLAC | PLACE_LIVING_ORDINANCE | | |
+1 STAT | LDS_BAPTISM_DATE_STATUS | | |
+2 DATE | CHANGE_DATE | | |
+1 | NOTE_STRUCTURE | | |
+1 | SOURCE_CITATION | | |
+1 DATE | DATE_LDS_ORD | | |
+1 TEMP | TEMPLE_CODE | | |
+1 PLAC | PLACE_LIVING_ORDINANCE | | |
+1 STAT | LDS_ENDOWMENT_DATE_STATUS | | |
+2 DATE | CHANGE_DATE | | |
+1 | NOTE_STRUCTURE | | |
+1 | SOURCE_CITATION | | |
+1 DATE | DATE_LDS_ORD | | |
+1 TEMP | TEMPLE_CODE | | |
+1 PLAC | PLACE_LIVING_ORDINANCE | | |
+1 FAMC | @ | | |
+1 STAT | LDS_CHILD_SEALING_DATE_STATUS | | |
+2 DATE | CHANGE_DATE | | |
+1 | NOTE_STRUCTURE | | |
+1 | SOURCE_CITATION | | |

:warning: to be continued/checked


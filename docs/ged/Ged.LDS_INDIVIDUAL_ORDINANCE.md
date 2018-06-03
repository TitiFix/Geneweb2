<!-- licence GPL V2, cf https://github.com/TitiFix/geneweb -->
# LDS_INDIVIDUAL_ORDINANCE
## Abstract

## GEDCOM syntax and proprietary extensions

**LDS_INDIVIDUAL_ORDINANCE**:=
<pre>
[
<b>n [ BAPL | CONL ]{1:1}</b>
  +1 DATE &lt;<a href=Ged.DATE_LDS_ORD.md>DATE_LDS_ORD</a>&gt;{0:1}
  +1 TEMP &lt;<a href=Ged.TEMPLE_CODE.md>TEMPLE_CODE</a>&gt;{0:1}
  +1 PLAC &lt;<a href=Ged.PLACE_LIVING_ORDINANCE.md>PLACE_LIVING_ORDINANCE</a>&gt;{0:1}
  +1 STAT &lt;<a href=Ged.LDS_BAPTISM_DATE_STATUS.md>LDS_BAPTISM_DATE_STATUS</a>&gt;{0:1}
<b>    +2 DATE &lt;<a href=Ged.CHANGE_DATE.md>CHANGE_DATE</a>&gt;{1:1}</b>
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt;&gt;{0:M}
|
<b>n ENDL{1:1}</b>
  +1 DATE &lt;<a href=Ged.DATE_LDS_ORD.md>DATE_LDS_ORD</a>&gt;{0:1}
  +1 TEMP &lt;<a href=Ged.TEMPLE_CODE.md>TEMPLE_CODE</a>&gt;{0:1}
  +1 PLAC &lt;<a href=Ged.PLACE_LIVING_ORDINANCE.md>PLACE_LIVING_ORDINANCE</a>&gt;{0:1}
  +1 STAT &lt;<a href=Ged.LDS_ENDOWMENT_DATE_STATUS.md>LDS_ENDOWMENT_DATE_STATUS</a>&gt;{0:1}
<b>    +2 DATE &lt;<a href=Ged.CHANGE_DATE.md>CHANGE_DATE</a>&gt;{1:1}</b>
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt;&gt;{0:M}
|
<b>n SLGC{1:1}</b>
  +1 DATE &lt;<a href=Ged.DATE_LDS_ORD.md>DATE_LDS_ORD</a>&gt;{0:1}
  +1 TEMP &lt;<a href=Ged.TEMPLE_CODE.md>TEMPLE_CODE</a>&gt;{0:1}
  +1 PLAC &lt;<a href=Ged.PLACE_LIVING_ORDINANCE.md>PLACE_LIVING_ORDINANCE</a>&gt;{0:1}
<b>  +1 FAMC @&lt;<a href=Ged.XREF_FAM.md>XREF:FAM</a>&gt;@{1:1}</b>
  +1 STAT &lt;<a href=Ged.LDS_CHILD_SEALING_DATE_STATUS.md>LDS_CHILD_SEALING_DATE_STATUS</a>&gt;{0:1}
<b>    +2 DATE &lt;<a href=Ged.CHANGE_DATE.md>CHANGE_DATE</a>&gt;{1:1}</b>
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt;&gt;{0:M}
]
</pre>
Used in <a href=Ged.INDIVIDUAL_RECORD.md>INDIVIDUAL_RECORD</a><br />


## Geneweb behavior


🚧 UNDER CONSTRUCTION : to be continued/checked 🚧 



level tag  | Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#bapl>BAPL</a>\|<a href=Ged.GLOSSARY.md#conl>CONL</a> |  | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#temp>TEMP</a> | char{4:5} | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#plac>PLAC</a> | &lt;<a href=Ged.PLACE_NAME.md>PLACE_NAME</a>&gt; | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#stat>STAT</a> |  CHILD \| COMPLETED \| EXCLUDED \| PRE-1970 \| STILLBORN \| SUBMITTED \| UNCLEARED  | ? | ? | 
+2 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_EXACT.md>DATE_EXACT</a>&gt; | ? | ? | 
+1  | &lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt; | ? | ? | 
+1  | &lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#endl>ENDL</a> |  | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#temp>TEMP</a> | char{4:5} | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#plac>PLAC</a> | &lt;<a href=Ged.PLACE_NAME.md>PLACE_NAME</a>&gt; | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#stat>STAT</a> |  CHILD \| COMPLETED \| EXCLUDED \| PRE-1970 \|  STILLBORN \| SUBMITTED \| UNCLEARED  | ? | ? | 
+2 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_EXACT.md>DATE_EXACT</a>&gt; | ? | ? | 
+1  | &lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt; | ? | ? | 
+1  | &lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#slgc>SLGC</a> |  | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#temp>TEMP</a> | char{4:5} | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#plac>PLAC</a> | &lt;<a href=Ged.PLACE_NAME.md>PLACE_NAME</a>&gt; | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#famc>FAMC</a> | @XREF{1:22}@ | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#stat>STAT</a> |  BIC \| COMPLETED \| EXCLUDED \| DNS \| PRE-1970 \| STILLBORN \| SUBMITTED \| UNCLEARED  | ? | ? | 
+2 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_EXACT.md>DATE_EXACT</a>&gt; | ? | ? | 
+1  | &lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt; | ? | ? | 
+1  | &lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt; | ? | ? | 

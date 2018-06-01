# LDS_SPOUSE_SEALING
## Abstract
A religious event pertaining to the sealing of a husband and wife in an LDS temple ceremony.

## GEDCOM syntax and proprietary extensions

**LDS_SPOUSE_SEALING**:=
<pre>
<b>n SLGS{1:1}</b>
  +1 DATE &lt;<a href=Ged.DATE_LDS_ORD.md>DATE_LDS_ORD</a>&gt;{0:1}
  +1 TEMP &lt;<a href=Ged.TEMPLE_CODE.md>TEMPLE_CODE</a>&gt;{0:1}
  +1 PLAC &lt;<a href=Ged.PLACE_LIVING_ORDINANCE.md>PLACE_LIVING_ORDINANCE</a>&gt;{0:1}
  +1 STAT &lt;<a href=Ged.LDS_SPOUSE_SEALING_DATE_STATUS.md>LDS_SPOUSE_SEALING_DATE_STATUS</a>&gt; {0:1}
<b>    +2 DATE &lt;<a href=Ged.CHANGE_DATE.md>CHANGE_DATE</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt; {0:M}
  +1 &lt;&lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt;&gt; {0:M}
</pre>
Used in <a href=Ged.FAMILY_RECORD.md>FAMILY_RECORD</a><br />


## Geneweb behavior

level tag  | Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#slgs>SLGS</a> |  | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#temp>TEMP</a> | char{4:5} | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#plac>PLAC</a> | &lt;<a href=Ged.PLACE_NAME.md>PLACE_NAME</a>&gt; | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#stat>STAT</a> |  CANCELED \| COMPLETED \| DNS \| EXCLUDED \| DNS/CAN \| PRE-1970 \| SUBMITTED \| UNCLEARED  | ? | ? | 
+2 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_EXACT.md>DATE_EXACT</a>&gt; | ? | ? | 
+1  | &lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt; | ? | ? | 
+1  | &lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt; | ? | ? | 

🚧 to be continued/checked


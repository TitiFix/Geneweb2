# LDS_SPOUSE_SEALING
## Abstract


## GEDCOM syntax and proprietary extensions
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

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
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#slgs>SLGS</a> |  | | |
+1 <a href=Ged.GLOSSARY.md#date>DATE</a> | DATE_LDS_ORD | | |
+1 <a href=Ged.GLOSSARY.md#temp>TEMP</a> | TEMPLE_CODE | | |
+1 <a href=Ged.GLOSSARY.md#plac>PLAC</a> | PLACE_LIVING_ORDINANCE | | |
+1 <a href=Ged.GLOSSARY.md#stat>STAT</a> | LDS_SPOUSE_SEALING_DATE_STATUS | | |
+2 <a href=Ged.GLOSSARY.md#date>DATE</a> | CHANGE_DATE | | |
+1  | NOTE_STRUCTURE | | |
+1  | SOURCE_CITATION | | |

:warning: to be continued/checked


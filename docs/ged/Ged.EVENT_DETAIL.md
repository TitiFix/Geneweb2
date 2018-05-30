# EVENT_DETAIL
## Abstract


## GEDCOM syntax and proprietary extensions
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**EVENT_DETAIL**:=
<pre>
n TYPE &lt;<a href=Ged.EVENT_OR_FACT_CLASSIFICATION.md>EVENT_OR_FACT_CLASSIFICATION</a>&gt;{0:1}
n DATE &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt;{0:1}
n &lt;&lt;<a href=Ged.PLACE_STRUCTURE.md>PLACE_STRUCTURE</a>&gt;&gt;{0:1}
n &lt;&lt;<a href=Ged.ADDRESS_STRUCTURE.md>ADDRESS_STRUCTURE</a>&gt;&gt;{0:1}
n AGNC &lt;<a href=Ged.RESPONSIBLE_AGENCY.md>RESPONSIBLE_AGENCY</a>&gt;{0:1}
n RELI &lt;<a href=Ged.RELIGIOUS_AFFILIATION.md>RELIGIOUS_AFFILIATION</a>&gt;{0:1}
n CAUS &lt;<a href=Ged.CAUSE_OF_EVENT.md>CAUSE_OF_EVENT</a>&gt;{0:1}
n RESN &lt;<a href=Ged.RESTRICTION_NOTICE.md>RESTRICTION_NOTICE</a>&gt;{0:1}
n &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
n &lt;&lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt;&gt;{0:M}
n &lt;&lt;<a href=Ged.MULTIMEDIA_LINK.md>MULTIMEDIA_LINK</a>&gt;&gt;{0:M}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#TYPE>TYPE</a> | EVENT_OR_FACT_CLASSIFICATION | | |
+0 <a href=Ged.GLOSSARY.md#DATE>DATE</a> | DATE_VALUE | | |
+0  | PLACE_STRUCTURE | | |
+0  | ADDRESS_STRUCTURE | | |
+0 <a href=Ged.GLOSSARY.md#AGNC>AGNC</a> | RESPONSIBLE_AGENCY | | |
+0 <a href=Ged.GLOSSARY.md#RELI>RELI</a> | RELIGIOUS_AFFILIATION | | |
+0 <a href=Ged.GLOSSARY.md#CAUS>CAUS</a> | CAUSE_OF_EVENT | | |
+0 <a href=Ged.GLOSSARY.md#RESN>RESN</a> | RESTRICTION_NOTICE | | |
+0  | NOTE_STRUCTURE | | |
+0  | SOURCE_CITATION | | |
+0  | MULTIMEDIA_LINK | | |

:warning: to be continued/checked


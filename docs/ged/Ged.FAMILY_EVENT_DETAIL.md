# FAMILY_EVENT_DETAIL
## Abstract
A further qualification to the meaning of the associated superior tag. The value does not have any
computer processing reliability. It is more in the form of a short one or two word note that should be
displayed any time the associated data is displayed.

## GEDCOM syntax and proprietary extensions

**FAMILY_EVENT_DETAIL**:=
<pre>
n TYPE &lt;<a href=Ged.EVENT_OR_FACT_CLASSIFICATION.md>EVENT_OR_FACT_CLASSIFICATION</a>&gt;{0:1} &#x25B6; (* modified value *)
n DATE &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt;{0:1}
n &lt;&lt;<a href=Ged.PLACE_STRUCTURE.md>PLACE_STRUCTURE</a>&gt;&gt;{0:1}
n &lt;&lt;<a href=Ged.ADDRESS_STRUCTURE.md>ADDRESS_STRUCTURE</a>&gt;&gt;{0:1}
n AGNC &lt;<a href=Ged.RESPONSIBLE_AGENCY.md>RESPONSIBLE_AGENCY</a>&gt;{0:1}
n RELI &lt;<a href=Ged.RELIGIOUS_AFFILIATION.md>RELIGIOUS_AFFILIATION</a>&gt;{0:1} &#x25B6;
n CAUS &lt;<a href=Ged.CAUSE_OF_EVENT.md>CAUSE_OF_EVENT</a>&gt;{0:1}
n RESN &lt;<a href=Ged.RESTRICTION_NOTICE.md>RESTRICTION_NOTICE</a>&gt;{0:1} &#x25B6;
n &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
n &lt;&lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt;&gt;{0:M}
n &lt;&lt;<a href=Ged.MULTIMEDIA_LINK.md>MULTIMEDIA_LINK</a>&gt;&gt;{0:M}
n HUSB{0:1} &#x25B6;
<b>  +1 AGE &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt;{1:1} &#x25B6;</b>
n WIFE{0:1} &#x25B6;
<b>  +1 AGE &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt;{1:1} &#x25B6;</b>
</pre>
Used in <a href=Ged.FAMILY_EVENT_STRUCTURE.md>FAMILY_EVENT_STRUCTURE</a><br />


## Geneweb behavior

level tag  | Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#type>TYPE</a> | char{1:90} | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | ? | ? | 
+0  | &lt;<a href=Ged.PLACE_STRUCTURE.md>PLACE_STRUCTURE</a>&gt; | ? | ? | 
+0  | &lt;<a href=Ged.ADDRESS_STRUCTURE.md>ADDRESS_STRUCTURE</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#agnc>AGNC</a> | char{1:120} | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#reli>RELI</a> | char{1:90} | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#caus>CAUS</a> | char{1:90} | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#resn>RESN</a> | confidential \| locked \| privacy  | ? | ? | 
+0  | &lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt; | ? | ? | 
+0  | &lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt; | ? | ? | 
+0  | &lt;<a href=Ged.MULTIMEDIA_LINK.md>MULTIMEDIA_LINK</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#husb>HUSB</a> |  | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#wife>WIFE</a> |  | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | ? | ? | 

🚧 to be continued/checked


<!-- licence GPL V2, cf https://github.com/TitiFix/geneweb -->
# INDIVIDUAL_EVENT_DETAIL
## Abstract
In 5.5.1,  a generic FACT tag was added to the individual attribute structure. Previously, the generic EVEN
tag was used. The FACT was added to give a semantic difference between generic events and
generic facts or characteristics.


## GEDCOM syntax and proprietary extensions

**INDIVIDUAL_EVENT_DETAIL**:=
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
n AGE &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt;{0:1} &#x25B6;
</pre>
Used in <a href=Ged.INDIVIDUAL_ATTRIBUTE_STRUCTURE.md>INDIVIDUAL_ATTRIBUTE_STRUCTURE</a>, <a href=Ged.INDIVIDUAL_EVENT_STRUCTURE.md>INDIVIDUAL_EVENT_STRUCTURE</a><br />


## Geneweb behavior


🚧 UNDER CONSTRUCTION : to be continued/checked 🚧 



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
+0 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | ? | ? | 

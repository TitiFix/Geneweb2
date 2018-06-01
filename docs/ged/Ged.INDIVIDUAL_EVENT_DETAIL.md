# INDIVIDUAL_EVENT_DETAIL
## Abstract
In 5.5.1, added a generic FACT tag to the individual attribute structure. Previously, the generic EVEN
tag was used. The FACT was added to give a semantic difference between generic events and
generic facts or characteristics.


## GEDCOM syntax and proprietary extensions

**INDIVIDUAL_EVENT_DETAIL**:=
<pre>
<b>n &lt;&lt;<a href=Ged.EVENT_DETAIL.md>EVENT_DETAIL</a>&gt;&gt;{1:1}</b>
n AGE &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt;{0:1}
</pre>
Used in <a href=Ged.INDIVIDUAL_ATTRIBUTE_STRUCTURE.md>INDIVIDUAL_ATTRIBUTE_STRUCTURE</a>, <a href=Ged.INDIVIDUAL_EVENT_STRUCTURE.md>INDIVIDUAL_EVENT_STRUCTURE</a><br />


## Geneweb behavior

level tag  | Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0  | &lt;<a href=Ged.EVENT_DETAIL.md>EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | ? | ? | 

🚧 to be continued/checked


# FAMILY_EVENT_DETAIL
## Abstract

## GEDCOM syntax and proprietary extensions

**FAMILY_EVENT_DETAIL**:=
<pre>
n HUSB{0:1}
<b>  +1 AGE &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt;{1:1}</b>
n WIFE{0:1}
<b>  +1 AGE &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt;{1:1}</b>
n &lt;&lt;<a href=Ged.EVENT_DETAIL.md>EVENT_DETAIL</a>&gt;&gt;{0:1}
</pre>
Used in <a href=Ged.FAMILY_EVENT_STRUCTURE.md>FAMILY_EVENT_STRUCTURE</a><br />


## Geneweb behavior

level tag  | Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#husb>HUSB</a> |  | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#wife>WIFE</a> |  | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | ? | ? | 
+0  | &lt;<a href=Ged.EVENT_DETAIL.md>EVENT_DETAIL</a>&gt; | ? | ? | 

🚧 to be continued/checked


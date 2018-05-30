# INDIVIDUAL_EVENT_DETAIL
## Abstract


## GEDCOM syntax and proprietary extensions
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**INDIVIDUAL_EVENT_DETAIL**:=
<pre>
<b>n &lt;&lt;<a href=Ged.EVENT_DETAIL.md>EVENT_DETAIL</a>&gt;&gt;{1:1}</b>
n AGE &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt;{0:1}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0  | EVENT_DETAIL | | |
+0 <a href=Ged.GLOSSARY.md#age>AGE</a> | AGE_AT_EVENT | | |

:warning: to be continued/checked


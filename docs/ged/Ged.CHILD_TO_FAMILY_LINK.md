# CHILD_TO_FAMILY_LINK
## Abstract

## GEDCOM syntax and proprietary extensions

**CHILD_TO_FAMILY_LINK**:=
<pre>
<b>n FAMC @&lt;<a href=Ged.XREF_FAM.md>XREF:FAM</a>&gt;@{1:1}</b>
  +1 PEDI &lt;<a href=Ged.PEDIGREE_LINKAGE_TYPE.md>PEDIGREE_LINKAGE_TYPE</a>&gt;{0:1}
  +1 STAT &lt;<a href=Ged.CHILD_LINKAGE_STATUS.md>CHILD_LINKAGE_STATUS</a>&gt;{0:1} &#x25B6;
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
</pre>
Used in <a href=Ged.INDIVIDUAL_RECORD.md>INDIVIDUAL_RECORD</a><br />


## Geneweb behavior

level tag  | Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#famc>FAMC</a> | @XREF{1:22}@ | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#pedi>PEDI</a> |  adopted \| birth \| foster \| sealing  | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#stat>STAT</a> | challenged \| disproven \| proven | ? | ? | 
+1  | &lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt; | ? | ? | 

🚧 to be continued/checked


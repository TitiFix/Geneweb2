# CHILD_TO_FAMILY_LINK
## Abstract


## GEDCOM syntax and proprietary extensions
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**CHILD_TO_FAMILY_LINK**:=
<pre>
<b>n FAMC @&lt;<a href=Ged.XREF_FAM.md>XREF:FAM</a>&gt;@{1:1}</b>
  +1 PEDI &lt;<a href=Ged.PEDIGREE_LINKAGE_TYPE.md>PEDIGREE_LINKAGE_TYPE</a>&gt;{0:1}
  +1 STAT &lt;<a href=Ged.CHILD_LINKAGE_STATUS.md>CHILD_LINKAGE_STATUS</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#famc>FAMC</a> | @XREF:FAM@ | | |
+1 <a href=Ged.GLOSSARY.md#pedi>PEDI</a> | PEDIGREE_LINKAGE_TYPE | | |
+1 <a href=Ged.GLOSSARY.md#stat>STAT</a> | CHILD_LINKAGE_STATUS | | |
+1  | NOTE_STRUCTURE | | |

:warning: to be continued/checked


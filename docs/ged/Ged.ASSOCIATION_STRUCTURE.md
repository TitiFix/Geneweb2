# ASSOCIATION_STRUCTURE
## Abstract
The association pointer only associates INDIvidual records to INDIvidual records.


## GEDCOM syntax and proprietary extensions
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**ASSOCIATION_STRUCTURE**:=
<pre>
<b>n ASSO @&lt;<a href=Ged.XREF_INDI.md>XREF:INDI</a>&gt;@{1:1}</b>
<b>  +1 RELA &lt;<a href=Ged.RELATION_IS_DESCRIPTOR.md>RELATION_IS_DESCRIPTOR</a>&gt;{1:1}</b>
  +1 &lt;&lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#asso>ASSO</a> | @XREF:INDI@ | | |
+1 <a href=Ged.GLOSSARY.md#rela>RELA</a> | RELATION_IS_DESCRIPTOR | | |
+1  | SOURCE_CITATION | | |
+1  | NOTE_STRUCTURE | | |

:warning: to be continued/checked


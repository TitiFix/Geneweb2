# ASSOCIATION_STRUCTURE
## Abstract
The association pointer only associates INDIvidual records to INDIvidual records. These structure may not be used for familial connections already expressed by the family tree (RELA value is not a father, mother, etc...)


## GEDCOM syntax and proprietary extensions

**ASSOCIATION_STRUCTURE**:=
<pre>
<b>n ASSO @&lt;<a href=Ged.XREF_INDI.md>XREF:INDI</a>&gt;@{1:1}</b>
<b>  +1 TYPE &lt;<a href=Ged.RECORD_TYPE.md>RECORD_TYPE</a>&gt; {1:1} (* &#x25B6; remove in 5.5.1, do not used (5.0 error) &#x1F6AB; *)</b>
<b>  +1 RELA &lt;<a href=Ged.RELATION_IS_DESCRIPTOR.md>RELATION_IS_DESCRIPTOR</a>&gt;{1:1}</b>
  +1 &lt;&lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
</pre>
Used in <a href=Ged.INDIVIDUAL_RECORD.md>INDIVIDUAL_RECORD</a><br />


## Geneweb behavior

level tag  | Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#asso>ASSO</a> | @XREF{1:22}@ | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#type>TYPE</a> |  FAM \| INDI \| NOTE \| OBJE \| REPO \| SOUR \| SUBM \| SUBN  | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#rela>RELA</a> | 0 INDI | ? | ? | 
+1  | &lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt; | ? | ? | 
+1  | &lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt; | ? | ? | 

🚧 to be continued/checked


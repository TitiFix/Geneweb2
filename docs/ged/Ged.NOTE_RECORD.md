<!-- licence GPL V2, cf https://github.com/TitiFix/geneweb -->
# NOTE_RECORD
## Abstract
Additional information provided by the submitter for understanding the enclosing data.


## GEDCOM syntax and proprietary extensions

**NOTE_RECORD**:=
<pre>
<b>n @&lt;<a href=Ged.XREF_NOTE.md>XREF:NOTE</a>&gt;@ NOTE &lt;<a href=Ged.SUBMITTER_TEXT.md>SUBMITTER_TEXT</a>&gt;{1:1}</b>
  +1 [CONC|CONT] &lt;<a href=Ged.SUBMITTER_TEXT.md>SUBMITTER_TEXT</a>&gt;{0:M}
  +1 REFN &lt;<a href=Ged.USER_REFERENCE_NUMBER.md>USER_REFERENCE_NUMBER</a>&gt;{0:M} &#x1F5D1;
    +2 TYPE &lt;<a href=Ged.USER_REFERENCE_TYPE.md>USER_REFERENCE_TYPE</a>&gt;{0:1} &#x1F5D1;
  +1 RIN &lt;<a href=Ged.AUTOMATED_RECORD_ID.md>AUTOMATED_RECORD_ID</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.CHANGE_STRUCTURE.md>CHANGE_STRUCTURE</a>&gt;&gt;{0:1}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />


## Geneweb behavior


🚧 UNDER CONSTRUCTION : to be continued/checked 🚧 



level tag  | Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#refn>REFN</a> | 🗑 deprecated | ? | ? | 
+2 <a href=Ged.GLOSSARY.md#type>TYPE</a> | 🗑 deprecated | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#rin>RIN</a> | char{1:12} | ? | ? | 
+1  | &lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt; | ? | ? | 
+1  | &lt;<a href=Ged.CHANGE_STRUCTURE.md>CHANGE_STRUCTURE</a>&gt; | ? | ? | 

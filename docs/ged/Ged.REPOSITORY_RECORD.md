<!-- licence GPL V2, cf https://github.com/TitiFix/geneweb -->
# REPOSITORY_RECORD
## Abstract
An institution or person that has the specified item as part of their collection(s).


## GEDCOM syntax and proprietary extensions

**REPOSITORY_RECORD**:=
<pre>
<b>n @&lt;<a href=Ged.XREF_REPO.md>XREF:REPO</a>&gt;@ REPO{1:1}</b>
<b>  +1 NAME &lt;<a href=Ged.NAME_OF_REPOSITORY.md>NAME_OF_REPOSITORY</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.ADDRESS_STRUCTURE.md>ADDRESS_STRUCTURE</a>&gt;&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 REFN &lt;<a href=Ged.USER_REFERENCE_NUMBER.md>USER_REFERENCE_NUMBER</a>&gt;{0:M} &#x1F5D1;
    +2 TYPE &lt;<a href=Ged.USER_REFERENCE_TYPE.md>USER_REFERENCE_TYPE</a>&gt;{0:1} &#x1F5D1;
  +1 RIN &lt;<a href=Ged.AUTOMATED_RECORD_ID.md>AUTOMATED_RECORD_ID</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.CHANGE_STRUCTURE.md>CHANGE_STRUCTURE</a>&gt;&gt;{0:1}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />


## Geneweb behavior


🚧 UNDER CONSTRUCTION : to be continued/checked 🚧 



level tag  | Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#repo>REPO</a> | @XREF{1:22}@ | ignore | no | not used by Geneweb
+1 <a href=Ged.GLOSSARY.md#name>NAME</a> | char{1:90} | ? | ? | 
+1  | &lt;<a href=Ged.ADDRESS_STRUCTURE.md>ADDRESS_STRUCTURE</a>&gt; | ? | ? | 
+1  | &lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt; | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#refn>REFN</a> | 🗑 deprecated | ? | ? | 
+2 <a href=Ged.GLOSSARY.md#type>TYPE</a> | 🗑 deprecated | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#rin>RIN</a> | char{1:12} | ? | ? | 
+1  | &lt;<a href=Ged.CHANGE_STRUCTURE.md>CHANGE_STRUCTURE</a>&gt; | ? | ? | 




# REPOSITORY_RECORD
## Abstract

## GEDCOM syntax and proprietary extensions

**REPOSITORY_RECORD**:=
<pre>
<b>n @&lt;<a href=Ged.XREF_REPO.md>XREF:REPO</a>&gt;@ REPO{1:1}</b>
<b>  +1 NAME &lt;<a href=Ged.NAME_OF_REPOSITORY.md>NAME_OF_REPOSITORY</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.ADDRESS_STRUCTURE.md>ADDRESS_STRUCTURE</a>&gt;&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 REFN &lt;<a href=Ged.USER_REFERENCE_NUMBER.md>USER_REFERENCE_NUMBER</a>&gt;{0:M}
    +2 TYPE &lt;<a href=Ged.USER_REFERENCE_TYPE.md>USER_REFERENCE_TYPE</a>&gt;{0:1}
  +1 RIN &lt;<a href=Ged.AUTOMATED_RECORD_ID.md>AUTOMATED_RECORD_ID</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.CHANGE_STRUCTURE.md>CHANGE_STRUCTURE</a>&gt;&gt;{0:1}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />


## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#repo>REPO</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#name>NAME</a> | char{1:90} | | |
+1 <a href=Ged.GLOSSARY.md#addr>ADDR</a> | char{1:60} | | |
+2 <a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:60} | | |
+2 <a href=Ged.GLOSSARY.md#adr1>ADR1</a> | char{1:60} | | |
+2 <a href=Ged.GLOSSARY.md#adr2>ADR2</a> | char{1:60} | | |
+2 <a href=Ged.GLOSSARY.md#adr3>ADR3</a> | char{1:60} | | |
+2 <a href=Ged.GLOSSARY.md#city>CITY</a> | char{1:60} | | |
+2 <a href=Ged.GLOSSARY.md#stae>STAE</a> | char{1:60} | | |
+2 <a href=Ged.GLOSSARY.md#post>POST</a> | char{1:10} | | |
+2 <a href=Ged.GLOSSARY.md#ctry>CTRY</a> | char{1:60} | | |
+1 <a href=Ged.GLOSSARY.md#phon>PHON</a> | char{1:25} | | |
+1 <a href=Ged.GLOSSARY.md#email>EMAIL</a> | char{5:120} | | |
+1 <a href=Ged.GLOSSARY.md#fax>FAX</a> | char{5:60} | | |
+1 <a href=Ged.GLOSSARY.md#www>WWW</a> | char{5:120} | | |
+1 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+2 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+1 <a href=Ged.GLOSSARY.md#refn>REFN</a> | char{1:20} | | |
+2 <a href=Ged.GLOSSARY.md#type>TYPE</a> | char{1:40} | | |
+1 <a href=Ged.GLOSSARY.md#rin>RIN</a> | char{1:12} | | |
+1 <a href=Ged.GLOSSARY.md#chan>CHAN</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_EXACT.md>DATE_EXACT</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#time>TIME</a> |  hh:mm:ss.fs  | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+3 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |

:warning: to be continued/checked


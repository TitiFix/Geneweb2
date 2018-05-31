﻿# SOURCE_REPOSITORY_CITATION
## Abstract
This structure is used within a source record to point to a name and address record of the holder of the
source document.  Formal and informal repository name and addresses are stored in the
REPOSITORY_RECORD.  Informal repositories include owner's of an unpublished work or of a rare
published source, or a keeper of personal collections. An example would be the owner of a family Bible
containing unpublished family genealogical entries. More formal repositories, such as the Family History
Library, should show a call number of the source at that repository. The call number of that source
should be recorded using a subordinate CALN tag.  Systems which do not use repository name and
address record, should describe where the information cited is stored in the &lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;>
of the REPOsitory source citation structure.


## GEDCOM syntax and proprietary extensions

**SOURCE_REPOSITORY_CITATION**:=
<pre>
<b>n REPO [ @XREF:REPO@ | &lt;<a href=Ged.NULL.md>NULL</a>&gt;]{1:1}</b>
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 CALN &lt;<a href=Ged.SOURCE_CALL_NUMBER.md>SOURCE_CALL_NUMBER</a>&gt;{0:M}
    +2 MEDI &lt;<a href=Ged.SOURCE_MEDIA_TYPE.md>SOURCE_MEDIA_TYPE</a>&gt;{0:1}
</pre>
Used in <a href=Ged.SOURCE_RECORD.md>SOURCE_RECORD</a><br />


## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#repo>REPO</a> | [@XREF:REPO@\|NULL] | | |
+1 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+2 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+1 <a href=Ged.GLOSSARY.md#caln>CALN</a> | char{1:120} | | |
+2 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |

:warning: to be continued/checked

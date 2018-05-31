# PERSONAL_NAME_PIECES
## Abstract

## GEDCOM syntax and proprietary extensions

**PERSONAL_NAME_PIECES**:=
<pre>
n NPFX &lt;<a href=Ged.NAME_PIECE_PREFIX.md>NAME_PIECE_PREFIX</a>&gt; {0:1}
n GIVN &lt;<a href=Ged.NAME_PIECE_GIVEN.md>NAME_PIECE_GIVEN</a>&gt; {0:1}
n NICK &lt;<a href=Ged.NAME_PIECE_NICKNAME.md>NAME_PIECE_NICKNAME</a>&gt; {0:1}
n SPFX &lt;<a href=Ged.NAME_PIECE_SURNAME_PREFIX.md>NAME_PIECE_SURNAME_PREFIX</a>&gt; {0:1}
n SURN &lt;<a href=Ged.NAME_PIECE_SURNAME.md>NAME_PIECE_SURNAME</a>&gt; {0:1}
n NSFX &lt;<a href=Ged.NAME_PIECE_SUFFIX.md>NAME_PIECE_SUFFIX</a>&gt; {0:1}
n &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt; {0:M}
n &lt;&lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt;&gt; {0:M}
</pre>
Used in <a href=Ged.PERSONAL_NAME_STRUCTURE.md>PERSONAL_NAME_STRUCTURE</a><br />


## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#npfx>NPFX</a> | &lt;<a href=Ged.NAME_PIECE_PREFIX.md>NAME_PIECE_PREFIX</a>&gt; | | |
+0 <a href=Ged.GLOSSARY.md#givn>GIVN</a> | &lt;<a href=Ged.NAME_PIECE_GIVEN.md>NAME_PIECE_GIVEN</a>&gt; | | |
+0 <a href=Ged.GLOSSARY.md#nick>NICK</a> | &lt;<a href=Ged.NAME_PIECE_NICKNAME.md>NAME_PIECE_NICKNAME</a>&gt; | | |
+0 <a href=Ged.GLOSSARY.md#spfx>SPFX</a> | &lt;<a href=Ged.NAME_PIECE_SURNAME_PREFIX.md>NAME_PIECE_SURNAME_PREFIX</a>&gt; | | |
+0 <a href=Ged.GLOSSARY.md#surn>SURN</a> | &lt;<a href=Ged.NAME_PIECE_SURNAME.md>NAME_PIECE_SURNAME</a>&gt; | | |
+0 <a href=Ged.GLOSSARY.md#nsfx>NSFX</a> | &lt;<a href=Ged.NAME_PIECE_SUFFIX.md>NAME_PIECE_SUFFIX</a>&gt; | | |
+0 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+0 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+1 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+0 <a href=Ged.GLOSSARY.md#sour>SOUR</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#page>PAGE</a> | char{1:248} | | |
+1 <a href=Ged.GLOSSARY.md#even>EVEN</a> | &lt;<a href=Ged.EVENT_TYPE_CITED_FROM.md>EVENT_TYPE_CITED_FROM</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#role>ROLE</a> | &lt;<a href=Ged.ROLE_IN_EVENT.md>ROLE_IN_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#data>DATA</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#text>TEXT</a> | char{1:248} | | |
+3 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+1 <a href=Ged.GLOSSARY.md#obje>OBJE</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+3 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+2 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+4 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+1 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+2 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+3 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+1 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+2 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+1 <a href=Ged.GLOSSARY.md#quay>QUAY</a> |  0 \| 1 \| 2 \| 3  | | |
+0 <a href=Ged.GLOSSARY.md#sour>SOUR</a> | char{1:248} | | |
+1 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+1 <a href=Ged.GLOSSARY.md#text>TEXT</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+1 <a href=Ged.GLOSSARY.md#obje>OBJE</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+3 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+2 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+4 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+1 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+2 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+3 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+1 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+2 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+1 <a href=Ged.GLOSSARY.md#quay>QUAY</a> |  0 \| 1 \| 2 \| 3  | | |

:warning: to be continued/checked


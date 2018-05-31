# PERSONAL_NAME_STRUCTURE
## Abstract
The name value is formed in the manner the name is normally spoken, with the given name and family
n ame (surname) separated by slashes (/). (See &lt;<a href=Ged.NAME_PERSONAL.md>NAME_PERSONAL</a>&gt;) Based on the
dynamic nature or unknown compositions of naming conventions, it is difficult to provide more
detailed name piece structure to handle every case. The NPFX, GIVN, NICK, SPFX, SURN, and
NSFX tags are provided optionally for systems that cannot operate effectively with less structured
information.


## GEDCOM syntax and proprietary extensions

**PERSONAL_NAME_STRUCTURE**:=
<pre>
<b>n NAME &lt;<a href=Ged.NAME_PERSONAL.md>NAME_PERSONAL</a>&gt; {1:1}</b>
  +1 TYPE &lt;<a href=Ged.NAME_TYPE.md>NAME_TYPE</a>&gt; {0:1}
  +1 &lt;&lt;<a href=Ged.PERSONAL_NAME_PIECES.md>PERSONAL_NAME_PIECES</a>&gt;&gt; {0:1}
  +1 FONE &lt;<a href=Ged.NAME_PHONETIC_VARIATION.md>NAME_PHONETIC_VARIATION</a>&gt; {0:M}
<b>    +2 TYPE &lt;<a href=Ged.PHONETIC_TYPE.md>PHONETIC_TYPE</a>&gt; {1:1}</b>
    +2 &lt;&lt;<a href=Ged.PERSONAL_NAME_PIECES.md>PERSONAL_NAME_PIECES</a>&gt;&gt; {0:1}
  +1 ROMN &lt;<a href=Ged.NAME_ROMANIZED_VARIATION.md>NAME_ROMANIZED_VARIATION</a>&gt; {0:M}
<b>    +2 TYPE &lt;<a href=Ged.ROMANIZED_TYPE.md>ROMANIZED_TYPE</a>&gt; {1:1}</b>
    +2 &lt;&lt;<a href=Ged.PERSONAL_NAME_PIECES.md>PERSONAL_NAME_PIECES</a>&gt;&gt; {0:1}
</pre>
Used in <a href=Ged.INDIVIDUAL_RECORD.md>INDIVIDUAL_RECORD</a><br />


NOTE:
- For current future compatibility, all systems must construct their names based on the &lt;<a href=Ged.NAME_PERSONAL.md>NAME_PERSONAL</a>&gt; structure. Those using the optional name pieces should assume that few systems will process them, and most will not provide the name pieces.
- A &lt;<a href=Ged.NAME_TYPE.md>NAME_TYPE</a>&gt; is used to specify the particular variation that this name is.  For example; if the name type is subordinate to the &lt;<a href=Ged.NAME_PERSONAL.md>NAME_PERSONAL</a>&gt; it could indicate that this name is a name taken at immigration or that it could be an ‘also known as’ name.
- The structure allows name pieces to be specifically identified as subordinate parts of the name line. Most products will not use subordinate name pieces. A nickname can  be included on the name line by enclosing it in double quotation marks (changed in 5.5.)
- Systems using the subordinate name parts must still provide the name structure formed in the same way specified for &lt;<a href=Ged.NAME_PERSONAL.md>NAME_PERSONAL</a>&gt;.

## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#name>NAME</a> | &lt;<a href=Ged.NAME_PERSONAL.md>NAME_PERSONAL</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#type>TYPE</a> |  aka \| birth \| immigrant \| maiden \| married \| user_defined  | | |
+1 <a href=Ged.GLOSSARY.md#npfx>NPFX</a> | &lt;<a href=Ged.NAME_PIECE_PREFIX.md>NAME_PIECE_PREFIX</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#givn>GIVN</a> | &lt;<a href=Ged.NAME_PIECE_GIVEN.md>NAME_PIECE_GIVEN</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#nick>NICK</a> | &lt;<a href=Ged.NAME_PIECE_NICKNAME.md>NAME_PIECE_NICKNAME</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#spfx>SPFX</a> | &lt;<a href=Ged.NAME_PIECE_SURNAME_PREFIX.md>NAME_PIECE_SURNAME_PREFIX</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#surn>SURN</a> | &lt;<a href=Ged.NAME_PIECE_SURNAME.md>NAME_PIECE_SURNAME</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#nsfx>NSFX</a> | &lt;<a href=Ged.NAME_PIECE_SUFFIX.md>NAME_PIECE_SUFFIX</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+2 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+1 <a href=Ged.GLOSSARY.md#sour>SOUR</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#page>PAGE</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#even>EVEN</a> | &lt;<a href=Ged.EVENT_TYPE_CITED_FROM.md>EVENT_TYPE_CITED_FROM</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#role>ROLE</a> | &lt;<a href=Ged.ROLE_IN_EVENT.md>ROLE_IN_EVENT</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#data>DATA</a> |  | | |
+3 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#text>TEXT</a> | char{1:248} | | |
+4 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#obje>OBJE</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+3 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+4 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+3 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+5 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+2 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+3 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+3 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+3 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+4 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+3 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#quay>QUAY</a> |  0 \| 1 \| 2 \| 3  | | |
+1 <a href=Ged.GLOSSARY.md#sour>SOUR</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#text>TEXT</a> | char{1:248} | | |
+3 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#obje>OBJE</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+3 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+4 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+3 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+5 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+2 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+3 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+3 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+3 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+4 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+3 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#quay>QUAY</a> |  0 \| 1 \| 2 \| 3  | | |
+1 <a href=Ged.GLOSSARY.md#fone>FONE</a> | char{1:120} | | |
+2 <a href=Ged.GLOSSARY.md#type>TYPE</a> |  user_defined \| hangul \| kana | | |
+2 <a href=Ged.GLOSSARY.md#npfx>NPFX</a> | &lt;<a href=Ged.NAME_PIECE_PREFIX.md>NAME_PIECE_PREFIX</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#givn>GIVN</a> | &lt;<a href=Ged.NAME_PIECE_GIVEN.md>NAME_PIECE_GIVEN</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#nick>NICK</a> | &lt;<a href=Ged.NAME_PIECE_NICKNAME.md>NAME_PIECE_NICKNAME</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#spfx>SPFX</a> | &lt;<a href=Ged.NAME_PIECE_SURNAME_PREFIX.md>NAME_PIECE_SURNAME_PREFIX</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#surn>SURN</a> | &lt;<a href=Ged.NAME_PIECE_SURNAME.md>NAME_PIECE_SURNAME</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#nsfx>NSFX</a> | &lt;<a href=Ged.NAME_PIECE_SUFFIX.md>NAME_PIECE_SUFFIX</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+3 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#sour>SOUR</a> | @XREF{1:22}@ | | |
+3 <a href=Ged.GLOSSARY.md#page>PAGE</a> | char{1:248} | | |
+3 <a href=Ged.GLOSSARY.md#even>EVEN</a> | &lt;<a href=Ged.EVENT_TYPE_CITED_FROM.md>EVENT_TYPE_CITED_FROM</a>&gt; | | |
+4 <a href=Ged.GLOSSARY.md#role>ROLE</a> | &lt;<a href=Ged.ROLE_IN_EVENT.md>ROLE_IN_EVENT</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#data>DATA</a> |  | | |
+4 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | | |
+4 <a href=Ged.GLOSSARY.md#text>TEXT</a> | char{1:248} | | |
+5 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+3 <a href=Ged.GLOSSARY.md#obje>OBJE</a> | @XREF{1:22}@ | | |
+3 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+4 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+5 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+4 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+6 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+3 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+4 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+4 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+4 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+5 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+4 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+3 <a href=Ged.GLOSSARY.md#quay>QUAY</a> |  0 \| 1 \| 2 \| 3  | | |
+2 <a href=Ged.GLOSSARY.md#sour>SOUR</a> | char{1:248} | | |
+3 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+3 <a href=Ged.GLOSSARY.md#text>TEXT</a> | char{1:248} | | |
+4 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+3 <a href=Ged.GLOSSARY.md#obje>OBJE</a> | @XREF{1:22}@ | | |
+3 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+4 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+5 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+4 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+6 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+3 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+4 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+4 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+4 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+5 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+4 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+3 <a href=Ged.GLOSSARY.md#quay>QUAY</a> |  0 \| 1 \| 2 \| 3  | | |
+1 <a href=Ged.GLOSSARY.md#romn>ROMN</a> | char{1:120} | | |
+2 <a href=Ged.GLOSSARY.md#type>TYPE</a> | &lt;<a href=Ged.ROMANIZED_TYPE.md>ROMANIZED_TYPE</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#npfx>NPFX</a> | &lt;<a href=Ged.NAME_PIECE_PREFIX.md>NAME_PIECE_PREFIX</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#givn>GIVN</a> | &lt;<a href=Ged.NAME_PIECE_GIVEN.md>NAME_PIECE_GIVEN</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#nick>NICK</a> | &lt;<a href=Ged.NAME_PIECE_NICKNAME.md>NAME_PIECE_NICKNAME</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#spfx>SPFX</a> | &lt;<a href=Ged.NAME_PIECE_SURNAME_PREFIX.md>NAME_PIECE_SURNAME_PREFIX</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#surn>SURN</a> | &lt;<a href=Ged.NAME_PIECE_SURNAME.md>NAME_PIECE_SURNAME</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#nsfx>NSFX</a> | &lt;<a href=Ged.NAME_PIECE_SUFFIX.md>NAME_PIECE_SUFFIX</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+3 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#sour>SOUR</a> | @XREF{1:22}@ | | |
+3 <a href=Ged.GLOSSARY.md#page>PAGE</a> | char{1:248} | | |
+3 <a href=Ged.GLOSSARY.md#even>EVEN</a> | &lt;<a href=Ged.EVENT_TYPE_CITED_FROM.md>EVENT_TYPE_CITED_FROM</a>&gt; | | |
+4 <a href=Ged.GLOSSARY.md#role>ROLE</a> | &lt;<a href=Ged.ROLE_IN_EVENT.md>ROLE_IN_EVENT</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#data>DATA</a> |  | | |
+4 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | | |
+4 <a href=Ged.GLOSSARY.md#text>TEXT</a> | char{1:248} | | |
+5 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+3 <a href=Ged.GLOSSARY.md#obje>OBJE</a> | @XREF{1:22}@ | | |
+3 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+4 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+5 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+4 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+6 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+3 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+4 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+4 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+4 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+5 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+4 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+3 <a href=Ged.GLOSSARY.md#quay>QUAY</a> |  0 \| 1 \| 2 \| 3  | | |
+2 <a href=Ged.GLOSSARY.md#sour>SOUR</a> | char{1:248} | | |
+3 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+3 <a href=Ged.GLOSSARY.md#text>TEXT</a> | char{1:248} | | |
+4 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+3 <a href=Ged.GLOSSARY.md#obje>OBJE</a> | @XREF{1:22}@ | | |
+3 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+4 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+5 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+4 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+6 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+3 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+4 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+4 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+4 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+5 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+4 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+3 <a href=Ged.GLOSSARY.md#quay>QUAY</a> |  0 \| 1 \| 2 \| 3  | | |

:warning: to be continued/checked


# FAMILY_EVENT_STRUCTURE
## Abstract

## GEDCOM syntax and proprietary extensions

**FAMILY_EVENT_STRUCTURE**:=
<pre>
[
n [ ANUL | CENS | DIV | DIVF ] {0:1}
  +1 &lt;&lt;<a href=Ged.FAMILY_EVENT_DETAIL.md>FAMILY_EVENT_DETAIL</a>&gt;&gt;{0:1}
|
n [ ENGA | MARB | MARC ]{0:1}
  +1 &lt;&lt;<a href=Ged.FAMILY_EVENT_DETAIL.md>FAMILY_EVENT_DETAIL</a>&gt;&gt;{0:1}
|
<b>n MARR  [Y|&lt;<a href=Ged.NULL.md>NULL</a>&gt;]{1:1}</b>
  +1 &lt;&lt;<a href=Ged.FAMILY_EVENT_DETAIL.md>FAMILY_EVENT_DETAIL</a>&gt;&gt;{0:1}
|
<b>n [ MARL | MARS ]{1:1}</b>
  +1 &lt;&lt;<a href=Ged.FAMILY_EVENT_DETAIL.md>FAMILY_EVENT_DETAIL</a>&gt;&gt;{0:1}
|
n RESI {0:1}
  +1 &lt;&lt;<a href=Ged.FAMILY_EVENT_DETAIL.md>FAMILY_EVENT_DETAIL</a>&gt;&gt;{0:1}
|
n EVEN [&lt;<a href=Ged.EVENT_DESCRIPTOR.md>EVENT_DESCRIPTOR</a>&gt; | &lt;<a href=Ged.NULL.md>NULL</a>&gt;] {0:1}
  +1 &lt;&lt;<a href=Ged.FAMILY_EVENT_DETAIL.md>FAMILY_EVENT_DETAIL</a>&gt;&gt;{0:1}
]
</pre>
Used in <a href=Ged.FAM_RECORD.md>FAM_RECORD</a><br />


## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#anul>ANUL</a>\|<a href=Ged.GLOSSARY.md#cens>CENS</a>\|<a href=Ged.GLOSSARY.md#div>DIV</a>\|<a href=Ged.GLOSSARY.md#divf>DIVF</a> |  | | |
+1 <a href=Ged.GLOSSARY.md#husb>HUSB</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#wife>WIFE</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#type>TYPE</a> | char{1:90} | | |
+1 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#plac>PLAC</a> | &lt;<a href=Ged.PLACE_NAME.md>PLACE_NAME</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#form>FORM</a> | char{1:120} | | |
+2 <a href=Ged.GLOSSARY.md#fone>FONE</a> | char{1:120} | | |
+3 <a href=Ged.GLOSSARY.md#type>TYPE</a> |  user_defined \| hangul \| kana | | |
+2 <a href=Ged.GLOSSARY.md#romn>ROMN</a> | char{1:120} | | |
+3 <a href=Ged.GLOSSARY.md#type>TYPE</a> | &lt;<a href=Ged.ROMANIZED_TYPE.md>ROMANIZED_TYPE</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#map>MAP</a> |  | | |
+3 <a href=Ged.GLOSSARY.md#lati>LATI</a> | char{5:8} | | |
+3 <a href=Ged.GLOSSARY.md#long>LONG</a> | char{5:8} | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+3 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
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
+1 <a href=Ged.GLOSSARY.md#agnc>AGNC</a> | char{1:120} | | |
+1 <a href=Ged.GLOSSARY.md#reli>RELI</a> | char{1:90} | | |
+1 <a href=Ged.GLOSSARY.md#caus>CAUS</a> | char{1:90} | | |
+1 <a href=Ged.GLOSSARY.md#resn>RESN</a> | confidential \| locked \| privacy  | | |
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
+0 <a href=Ged.GLOSSARY.md#enga>ENGA</a>\|<a href=Ged.GLOSSARY.md#marb>MARB</a>\|<a href=Ged.GLOSSARY.md#marc>MARC</a> |  | | |
+1 <a href=Ged.GLOSSARY.md#husb>HUSB</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#wife>WIFE</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#type>TYPE</a> | char{1:90} | | |
+1 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#plac>PLAC</a> | &lt;<a href=Ged.PLACE_NAME.md>PLACE_NAME</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#form>FORM</a> | char{1:120} | | |
+2 <a href=Ged.GLOSSARY.md#fone>FONE</a> | char{1:120} | | |
+3 <a href=Ged.GLOSSARY.md#type>TYPE</a> |  user_defined \| hangul \| kana | | |
+2 <a href=Ged.GLOSSARY.md#romn>ROMN</a> | char{1:120} | | |
+3 <a href=Ged.GLOSSARY.md#type>TYPE</a> | &lt;<a href=Ged.ROMANIZED_TYPE.md>ROMANIZED_TYPE</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#map>MAP</a> |  | | |
+3 <a href=Ged.GLOSSARY.md#lati>LATI</a> | char{5:8} | | |
+3 <a href=Ged.GLOSSARY.md#long>LONG</a> | char{5:8} | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+3 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
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
+1 <a href=Ged.GLOSSARY.md#agnc>AGNC</a> | char{1:120} | | |
+1 <a href=Ged.GLOSSARY.md#reli>RELI</a> | char{1:90} | | |
+1 <a href=Ged.GLOSSARY.md#caus>CAUS</a> | char{1:90} | | |
+1 <a href=Ged.GLOSSARY.md#resn>RESN</a> | confidential \| locked \| privacy  | | |
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
+0 <a href=Ged.GLOSSARY.md#marr>MARR</a> | [Y\|NULL] | | |
+1 <a href=Ged.GLOSSARY.md#husb>HUSB</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#wife>WIFE</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#type>TYPE</a> | char{1:90} | | |
+1 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#plac>PLAC</a> | &lt;<a href=Ged.PLACE_NAME.md>PLACE_NAME</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#form>FORM</a> | char{1:120} | | |
+2 <a href=Ged.GLOSSARY.md#fone>FONE</a> | char{1:120} | | |
+3 <a href=Ged.GLOSSARY.md#type>TYPE</a> |  user_defined \| hangul \| kana | | |
+2 <a href=Ged.GLOSSARY.md#romn>ROMN</a> | char{1:120} | | |
+3 <a href=Ged.GLOSSARY.md#type>TYPE</a> | &lt;<a href=Ged.ROMANIZED_TYPE.md>ROMANIZED_TYPE</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#map>MAP</a> |  | | |
+3 <a href=Ged.GLOSSARY.md#lati>LATI</a> | char{5:8} | | |
+3 <a href=Ged.GLOSSARY.md#long>LONG</a> | char{5:8} | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+3 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
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
+1 <a href=Ged.GLOSSARY.md#agnc>AGNC</a> | char{1:120} | | |
+1 <a href=Ged.GLOSSARY.md#reli>RELI</a> | char{1:90} | | |
+1 <a href=Ged.GLOSSARY.md#caus>CAUS</a> | char{1:90} | | |
+1 <a href=Ged.GLOSSARY.md#resn>RESN</a> | confidential \| locked \| privacy  | | |
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
+0 <a href=Ged.GLOSSARY.md#marl>MARL</a>\|<a href=Ged.GLOSSARY.md#mars>MARS</a> |  | | |
+1 <a href=Ged.GLOSSARY.md#husb>HUSB</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#wife>WIFE</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#type>TYPE</a> | char{1:90} | | |
+1 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#plac>PLAC</a> | &lt;<a href=Ged.PLACE_NAME.md>PLACE_NAME</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#form>FORM</a> | char{1:120} | | |
+2 <a href=Ged.GLOSSARY.md#fone>FONE</a> | char{1:120} | | |
+3 <a href=Ged.GLOSSARY.md#type>TYPE</a> |  user_defined \| hangul \| kana | | |
+2 <a href=Ged.GLOSSARY.md#romn>ROMN</a> | char{1:120} | | |
+3 <a href=Ged.GLOSSARY.md#type>TYPE</a> | &lt;<a href=Ged.ROMANIZED_TYPE.md>ROMANIZED_TYPE</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#map>MAP</a> |  | | |
+3 <a href=Ged.GLOSSARY.md#lati>LATI</a> | char{5:8} | | |
+3 <a href=Ged.GLOSSARY.md#long>LONG</a> | char{5:8} | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+3 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
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
+1 <a href=Ged.GLOSSARY.md#agnc>AGNC</a> | char{1:120} | | |
+1 <a href=Ged.GLOSSARY.md#reli>RELI</a> | char{1:90} | | |
+1 <a href=Ged.GLOSSARY.md#caus>CAUS</a> | char{1:90} | | |
+1 <a href=Ged.GLOSSARY.md#resn>RESN</a> | confidential \| locked \| privacy  | | |
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
+0 <a href=Ged.GLOSSARY.md#resi>RESI</a> |  | | |
+1 <a href=Ged.GLOSSARY.md#husb>HUSB</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#wife>WIFE</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#type>TYPE</a> | char{1:90} | | |
+1 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#plac>PLAC</a> | &lt;<a href=Ged.PLACE_NAME.md>PLACE_NAME</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#form>FORM</a> | char{1:120} | | |
+2 <a href=Ged.GLOSSARY.md#fone>FONE</a> | char{1:120} | | |
+3 <a href=Ged.GLOSSARY.md#type>TYPE</a> |  user_defined \| hangul \| kana | | |
+2 <a href=Ged.GLOSSARY.md#romn>ROMN</a> | char{1:120} | | |
+3 <a href=Ged.GLOSSARY.md#type>TYPE</a> | &lt;<a href=Ged.ROMANIZED_TYPE.md>ROMANIZED_TYPE</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#map>MAP</a> |  | | |
+3 <a href=Ged.GLOSSARY.md#lati>LATI</a> | char{5:8} | | |
+3 <a href=Ged.GLOSSARY.md#long>LONG</a> | char{5:8} | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+3 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
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
+1 <a href=Ged.GLOSSARY.md#agnc>AGNC</a> | char{1:120} | | |
+1 <a href=Ged.GLOSSARY.md#reli>RELI</a> | char{1:90} | | |
+1 <a href=Ged.GLOSSARY.md#caus>CAUS</a> | char{1:90} | | |
+1 <a href=Ged.GLOSSARY.md#resn>RESN</a> | confidential \| locked \| privacy  | | |
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
+0 <a href=Ged.GLOSSARY.md#even>EVEN</a> | char{1:90}\|NULL | | |
+1 <a href=Ged.GLOSSARY.md#husb>HUSB</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#wife>WIFE</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#type>TYPE</a> | char{1:90} | | |
+1 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#plac>PLAC</a> | &lt;<a href=Ged.PLACE_NAME.md>PLACE_NAME</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#form>FORM</a> | char{1:120} | | |
+2 <a href=Ged.GLOSSARY.md#fone>FONE</a> | char{1:120} | | |
+3 <a href=Ged.GLOSSARY.md#type>TYPE</a> |  user_defined \| hangul \| kana | | |
+2 <a href=Ged.GLOSSARY.md#romn>ROMN</a> | char{1:120} | | |
+3 <a href=Ged.GLOSSARY.md#type>TYPE</a> | &lt;<a href=Ged.ROMANIZED_TYPE.md>ROMANIZED_TYPE</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#map>MAP</a> |  | | |
+3 <a href=Ged.GLOSSARY.md#lati>LATI</a> | char{5:8} | | |
+3 <a href=Ged.GLOSSARY.md#long>LONG</a> | char{5:8} | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+3 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
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
+1 <a href=Ged.GLOSSARY.md#agnc>AGNC</a> | char{1:120} | | |
+1 <a href=Ged.GLOSSARY.md#reli>RELI</a> | char{1:90} | | |
+1 <a href=Ged.GLOSSARY.md#caus>CAUS</a> | char{1:90} | | |
+1 <a href=Ged.GLOSSARY.md#resn>RESN</a> | confidential \| locked \| privacy  | | |
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

:warning: to be continued/checked


# INDIVIDUAL_ATTRIBUTE_STRUCTURE
## Abstract

## GEDCOM syntax and proprietary extensions

**INDIVIDUAL_ATTRIBUTE_STRUCTURE**:=
<pre>
[
<b>n CAST &lt;<a href=Ged.CASTE_NAME.md>CASTE_NAME</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n DSCR &lt;<a href=Ged.PHYSICAL_DESCRIPTION.md>PHYSICAL_DESCRIPTION</a>&gt; {1:1}</b>
  +1 [CONC | CONT ] &lt;<a href=Ged.PHYSICAL_DESCRIPTION.md>PHYSICAL_DESCRIPTION</a>&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n EDUC &lt;<a href=Ged.SCHOLASTIC_ACHIEVEMENT.md>SCHOLASTIC_ACHIEVEMENT</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n IDNO &lt;<a href=Ged.NATIONAL_ID_NUMBER.md>NATIONAL_ID_NUMBER</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n NATI &lt;<a href=Ged.NATIONAL_OR_TRIBAL_ORIGIN.md>NATIONAL_OR_TRIBAL_ORIGIN</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n NCHI &lt;<a href=Ged.COUNT_OF_CHILDREN.md>COUNT_OF_CHILDREN</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n NMR &lt;<a href=Ged.COUNT_OF_MARRIAGES.md>COUNT_OF_MARRIAGES</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n OCCU &lt;<a href=Ged.OCCUPATION.md>OCCUPATION</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n PROP &lt;<a href=Ged.POSSESSIONS.md>POSSESSIONS</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n RELI &lt;<a href=Ged.RELIGIOUS_AFFILIATION.md>RELIGIOUS_AFFILIATION</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n RESI (* Resides at *){1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n SSN &lt;<a href=Ged.SOCIAL_SECURITY_NUMBER.md>SOCIAL_SECURITY_NUMBER</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n TITL &lt;<a href=Ged.NOBILITY_TYPE_TITLE.md>NOBILITY_TYPE_TITLE</a>&gt;{1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n FACT &lt;<a href=Ged.ATTRIBUTE_DESCRIPTOR.md>ATTRIBUTE_DESCRIPTOR</a>&gt;{1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
]
</pre>
Used in <a href=Ged.INDIVIDUAL_RECORD.md>INDIVIDUAL_RECORD</a><br />


NOTE: The usage of IDNO or the FACT tag require that a subordinate TYPE tag be used to define
what kind of identification number or fact classification is being defined.  The TYPE tag can be used
with each of the above tags used in this structure.

## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#cast>CAST</a> | char{1:90} | | |
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
+1 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+0 <a href=Ged.GLOSSARY.md#dscr>DSCR</a> | char{1:248} | | |
+1 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
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
+1 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+0 <a href=Ged.GLOSSARY.md#educ>EDUC</a> | char{1:248} | | |
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
+1 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+0 <a href=Ged.GLOSSARY.md#idno>IDNO</a> | char{1:30} | | |
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
+1 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+0 <a href=Ged.GLOSSARY.md#nati>NATI</a> | char{1:120} | | |
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
+1 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+0 <a href=Ged.GLOSSARY.md#nchi>NCHI</a> | char{1:3} | | |
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
+1 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+0 <a href=Ged.GLOSSARY.md#nmr>NMR</a> | char{1:3} | | |
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
+1 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+0 <a href=Ged.GLOSSARY.md#occu>OCCU</a> | char{1:90} | | |
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
+1 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+0 <a href=Ged.GLOSSARY.md#prop>PROP</a> | char{1:248} | | |
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
+1 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+0 <a href=Ged.GLOSSARY.md#reli>RELI</a> | char{1:90} | | |
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
+1 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+0 <a href=Ged.GLOSSARY.md#resi>RESI</a> | (* | | |
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
+1 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+0 <a href=Ged.GLOSSARY.md#ssn>SSN</a> | char{9:11} | | |
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
+1 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+0 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:120} | | |
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
+1 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+0 <a href=Ged.GLOSSARY.md#fact>FACT</a> | char{1:90} | | |
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
+1 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |

:warning: to be continued/checked


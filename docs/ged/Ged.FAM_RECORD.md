# FAM_RECORD
## Abstract
The FAMily record is used to record marriages, common law marriages, and family unions caused by
two people becoming the parents of a child. There can be no more than one HUSB/father and one
WIFE/mother listed in each FAM_RECORD. If, for example, a man participated in more than one
family union, then he would appear in more than one FAM_RECORD. The family record structure
assumes that the HUSB/father is male and WIFE/mother is female.


## GEDCOM syntax and proprietary extensions

**FAM_RECORD**:=
<pre>
<b>n @&lt;<a href=Ged.XREF_FAM.md>XREF:FAM</a>&gt;@ FAM{1:1}</b>
  +1 RESN &lt;<a href=Ged.RESTRICTION_NOTICE.md>RESTRICTION_NOTICE</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.FAMILY_EVENT_STRUCTURE.md>FAMILY_EVENT_STRUCTURE</a>&gt;&gt;{0:M}
  +1 HUSB @&lt;<a href=Ged.XREF_INDI.md>XREF:INDI</a>&gt;@{0:1}
  +1 WIFE @&lt;<a href=Ged.XREF_INDI.md>XREF:INDI</a>&gt;@{0:1}
  +1 CHIL @&lt;<a href=Ged.XREF_INDI.md>XREF:INDI</a>&gt;@{0:M} *
  +1 NCHI &lt;<a href=Ged.COUNT_OF_CHILDREN.md>COUNT_OF_CHILDREN</a>&gt;{0:1}
  +1 SUBM @&lt;<a href=Ged.XREF_SUBM.md>XREF:SUBM</a>&gt;@{0:M}
  +1 &lt;&lt;<a href=Ged.LDS_SPOUSE_SEALING.md>LDS_SPOUSE_SEALING</a>&gt;&gt;{0:M}
  +1 REFN &lt;<a href=Ged.USER_REFERENCE_NUMBER.md>USER_REFERENCE_NUMBER</a>&gt;{0:M}
    +2 TYPE &lt;<a href=Ged.USER_REFERENCE_TYPE.md>USER_REFERENCE_TYPE</a>&gt;{0:1}
  +1 RIN &lt;<a href=Ged.AUTOMATED_RECORD_ID.md>AUTOMATED_RECORD_ID</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.CHANGE_STRUCTURE.md>CHANGE_STRUCTURE</a>&gt;&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.MULTIMEDIA_LINK.md>MULTIMEDIA_LINK</a>&gt;&gt;{0:M}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />


NOTE:
The preferred order of the CHILdren pointers within a FAMily structure is chronological by birth.

## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#fam>FAM</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#resn>RESN</a> | confidential \| locked \| privacy  | | |
+1 <a href=Ged.GLOSSARY.md#anul>ANUL</a>\|<a href=Ged.GLOSSARY.md#cens>CENS</a>\|<a href=Ged.GLOSSARY.md#div>DIV</a>\|<a href=Ged.GLOSSARY.md#divf>DIVF</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#husb>HUSB</a> |  | | |
+3 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#wife>WIFE</a> |  | | |
+3 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#type>TYPE</a> | char{1:90} | | |
+2 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#plac>PLAC</a> | &lt;<a href=Ged.PLACE_NAME.md>PLACE_NAME</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#form>FORM</a> | char{1:120} | | |
+3 <a href=Ged.GLOSSARY.md#fone>FONE</a> | char{1:120} | | |
+4 <a href=Ged.GLOSSARY.md#type>TYPE</a> |  user_defined \| hangul \| kana | | |
+3 <a href=Ged.GLOSSARY.md#romn>ROMN</a> | char{1:120} | | |
+4 <a href=Ged.GLOSSARY.md#type>TYPE</a> | &lt;<a href=Ged.ROMANIZED_TYPE.md>ROMANIZED_TYPE</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#map>MAP</a> |  | | |
+4 <a href=Ged.GLOSSARY.md#lati>LATI</a> | char{5:8} | | |
+4 <a href=Ged.GLOSSARY.md#long>LONG</a> | char{5:8} | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+4 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#addr>ADDR</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#adr1>ADR1</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#adr2>ADR2</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#adr3>ADR3</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#city>CITY</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#stae>STAE</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#post>POST</a> | char{1:10} | | |
+3 <a href=Ged.GLOSSARY.md#ctry>CTRY</a> | char{1:60} | | |
+2 <a href=Ged.GLOSSARY.md#phon>PHON</a> | char{1:25} | | |
+2 <a href=Ged.GLOSSARY.md#email>EMAIL</a> | char{5:120} | | |
+2 <a href=Ged.GLOSSARY.md#fax>FAX</a> | char{5:60} | | |
+2 <a href=Ged.GLOSSARY.md#www>WWW</a> | char{5:120} | | |
+2 <a href=Ged.GLOSSARY.md#agnc>AGNC</a> | char{1:120} | | |
+2 <a href=Ged.GLOSSARY.md#reli>RELI</a> | char{1:90} | | |
+2 <a href=Ged.GLOSSARY.md#caus>CAUS</a> | char{1:90} | | |
+2 <a href=Ged.GLOSSARY.md#resn>RESN</a> | confidential \| locked \| privacy  | | |
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
+1 <a href=Ged.GLOSSARY.md#enga>ENGA</a>\|<a href=Ged.GLOSSARY.md#marb>MARB</a>\|<a href=Ged.GLOSSARY.md#marc>MARC</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#husb>HUSB</a> |  | | |
+3 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#wife>WIFE</a> |  | | |
+3 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#type>TYPE</a> | char{1:90} | | |
+2 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#plac>PLAC</a> | &lt;<a href=Ged.PLACE_NAME.md>PLACE_NAME</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#form>FORM</a> | char{1:120} | | |
+3 <a href=Ged.GLOSSARY.md#fone>FONE</a> | char{1:120} | | |
+4 <a href=Ged.GLOSSARY.md#type>TYPE</a> |  user_defined \| hangul \| kana | | |
+3 <a href=Ged.GLOSSARY.md#romn>ROMN</a> | char{1:120} | | |
+4 <a href=Ged.GLOSSARY.md#type>TYPE</a> | &lt;<a href=Ged.ROMANIZED_TYPE.md>ROMANIZED_TYPE</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#map>MAP</a> |  | | |
+4 <a href=Ged.GLOSSARY.md#lati>LATI</a> | char{5:8} | | |
+4 <a href=Ged.GLOSSARY.md#long>LONG</a> | char{5:8} | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+4 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#addr>ADDR</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#adr1>ADR1</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#adr2>ADR2</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#adr3>ADR3</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#city>CITY</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#stae>STAE</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#post>POST</a> | char{1:10} | | |
+3 <a href=Ged.GLOSSARY.md#ctry>CTRY</a> | char{1:60} | | |
+2 <a href=Ged.GLOSSARY.md#phon>PHON</a> | char{1:25} | | |
+2 <a href=Ged.GLOSSARY.md#email>EMAIL</a> | char{5:120} | | |
+2 <a href=Ged.GLOSSARY.md#fax>FAX</a> | char{5:60} | | |
+2 <a href=Ged.GLOSSARY.md#www>WWW</a> | char{5:120} | | |
+2 <a href=Ged.GLOSSARY.md#agnc>AGNC</a> | char{1:120} | | |
+2 <a href=Ged.GLOSSARY.md#reli>RELI</a> | char{1:90} | | |
+2 <a href=Ged.GLOSSARY.md#caus>CAUS</a> | char{1:90} | | |
+2 <a href=Ged.GLOSSARY.md#resn>RESN</a> | confidential \| locked \| privacy  | | |
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
+1 <a href=Ged.GLOSSARY.md#marr>MARR</a> | [Y\|NULL] | | |
+2 <a href=Ged.GLOSSARY.md#husb>HUSB</a> |  | | |
+3 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#wife>WIFE</a> |  | | |
+3 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#type>TYPE</a> | char{1:90} | | |
+2 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#plac>PLAC</a> | &lt;<a href=Ged.PLACE_NAME.md>PLACE_NAME</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#form>FORM</a> | char{1:120} | | |
+3 <a href=Ged.GLOSSARY.md#fone>FONE</a> | char{1:120} | | |
+4 <a href=Ged.GLOSSARY.md#type>TYPE</a> |  user_defined \| hangul \| kana | | |
+3 <a href=Ged.GLOSSARY.md#romn>ROMN</a> | char{1:120} | | |
+4 <a href=Ged.GLOSSARY.md#type>TYPE</a> | &lt;<a href=Ged.ROMANIZED_TYPE.md>ROMANIZED_TYPE</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#map>MAP</a> |  | | |
+4 <a href=Ged.GLOSSARY.md#lati>LATI</a> | char{5:8} | | |
+4 <a href=Ged.GLOSSARY.md#long>LONG</a> | char{5:8} | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+4 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#addr>ADDR</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#adr1>ADR1</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#adr2>ADR2</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#adr3>ADR3</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#city>CITY</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#stae>STAE</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#post>POST</a> | char{1:10} | | |
+3 <a href=Ged.GLOSSARY.md#ctry>CTRY</a> | char{1:60} | | |
+2 <a href=Ged.GLOSSARY.md#phon>PHON</a> | char{1:25} | | |
+2 <a href=Ged.GLOSSARY.md#email>EMAIL</a> | char{5:120} | | |
+2 <a href=Ged.GLOSSARY.md#fax>FAX</a> | char{5:60} | | |
+2 <a href=Ged.GLOSSARY.md#www>WWW</a> | char{5:120} | | |
+2 <a href=Ged.GLOSSARY.md#agnc>AGNC</a> | char{1:120} | | |
+2 <a href=Ged.GLOSSARY.md#reli>RELI</a> | char{1:90} | | |
+2 <a href=Ged.GLOSSARY.md#caus>CAUS</a> | char{1:90} | | |
+2 <a href=Ged.GLOSSARY.md#resn>RESN</a> | confidential \| locked \| privacy  | | |
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
+1 <a href=Ged.GLOSSARY.md#marl>MARL</a>\|<a href=Ged.GLOSSARY.md#mars>MARS</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#husb>HUSB</a> |  | | |
+3 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#wife>WIFE</a> |  | | |
+3 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#type>TYPE</a> | char{1:90} | | |
+2 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#plac>PLAC</a> | &lt;<a href=Ged.PLACE_NAME.md>PLACE_NAME</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#form>FORM</a> | char{1:120} | | |
+3 <a href=Ged.GLOSSARY.md#fone>FONE</a> | char{1:120} | | |
+4 <a href=Ged.GLOSSARY.md#type>TYPE</a> |  user_defined \| hangul \| kana | | |
+3 <a href=Ged.GLOSSARY.md#romn>ROMN</a> | char{1:120} | | |
+4 <a href=Ged.GLOSSARY.md#type>TYPE</a> | &lt;<a href=Ged.ROMANIZED_TYPE.md>ROMANIZED_TYPE</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#map>MAP</a> |  | | |
+4 <a href=Ged.GLOSSARY.md#lati>LATI</a> | char{5:8} | | |
+4 <a href=Ged.GLOSSARY.md#long>LONG</a> | char{5:8} | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+4 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#addr>ADDR</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#adr1>ADR1</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#adr2>ADR2</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#adr3>ADR3</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#city>CITY</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#stae>STAE</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#post>POST</a> | char{1:10} | | |
+3 <a href=Ged.GLOSSARY.md#ctry>CTRY</a> | char{1:60} | | |
+2 <a href=Ged.GLOSSARY.md#phon>PHON</a> | char{1:25} | | |
+2 <a href=Ged.GLOSSARY.md#email>EMAIL</a> | char{5:120} | | |
+2 <a href=Ged.GLOSSARY.md#fax>FAX</a> | char{5:60} | | |
+2 <a href=Ged.GLOSSARY.md#www>WWW</a> | char{5:120} | | |
+2 <a href=Ged.GLOSSARY.md#agnc>AGNC</a> | char{1:120} | | |
+2 <a href=Ged.GLOSSARY.md#reli>RELI</a> | char{1:90} | | |
+2 <a href=Ged.GLOSSARY.md#caus>CAUS</a> | char{1:90} | | |
+2 <a href=Ged.GLOSSARY.md#resn>RESN</a> | confidential \| locked \| privacy  | | |
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
+1 <a href=Ged.GLOSSARY.md#resi>RESI</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#husb>HUSB</a> |  | | |
+3 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#wife>WIFE</a> |  | | |
+3 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#type>TYPE</a> | char{1:90} | | |
+2 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#plac>PLAC</a> | &lt;<a href=Ged.PLACE_NAME.md>PLACE_NAME</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#form>FORM</a> | char{1:120} | | |
+3 <a href=Ged.GLOSSARY.md#fone>FONE</a> | char{1:120} | | |
+4 <a href=Ged.GLOSSARY.md#type>TYPE</a> |  user_defined \| hangul \| kana | | |
+3 <a href=Ged.GLOSSARY.md#romn>ROMN</a> | char{1:120} | | |
+4 <a href=Ged.GLOSSARY.md#type>TYPE</a> | &lt;<a href=Ged.ROMANIZED_TYPE.md>ROMANIZED_TYPE</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#map>MAP</a> |  | | |
+4 <a href=Ged.GLOSSARY.md#lati>LATI</a> | char{5:8} | | |
+4 <a href=Ged.GLOSSARY.md#long>LONG</a> | char{5:8} | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+4 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#addr>ADDR</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#adr1>ADR1</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#adr2>ADR2</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#adr3>ADR3</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#city>CITY</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#stae>STAE</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#post>POST</a> | char{1:10} | | |
+3 <a href=Ged.GLOSSARY.md#ctry>CTRY</a> | char{1:60} | | |
+2 <a href=Ged.GLOSSARY.md#phon>PHON</a> | char{1:25} | | |
+2 <a href=Ged.GLOSSARY.md#email>EMAIL</a> | char{5:120} | | |
+2 <a href=Ged.GLOSSARY.md#fax>FAX</a> | char{5:60} | | |
+2 <a href=Ged.GLOSSARY.md#www>WWW</a> | char{5:120} | | |
+2 <a href=Ged.GLOSSARY.md#agnc>AGNC</a> | char{1:120} | | |
+2 <a href=Ged.GLOSSARY.md#reli>RELI</a> | char{1:90} | | |
+2 <a href=Ged.GLOSSARY.md#caus>CAUS</a> | char{1:90} | | |
+2 <a href=Ged.GLOSSARY.md#resn>RESN</a> | confidential \| locked \| privacy  | | |
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
+1 <a href=Ged.GLOSSARY.md#even>EVEN</a> | char{1:90}\|NULL | | |
+2 <a href=Ged.GLOSSARY.md#husb>HUSB</a> |  | | |
+3 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#wife>WIFE</a> |  | | |
+3 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#type>TYPE</a> | char{1:90} | | |
+2 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#plac>PLAC</a> | &lt;<a href=Ged.PLACE_NAME.md>PLACE_NAME</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#form>FORM</a> | char{1:120} | | |
+3 <a href=Ged.GLOSSARY.md#fone>FONE</a> | char{1:120} | | |
+4 <a href=Ged.GLOSSARY.md#type>TYPE</a> |  user_defined \| hangul \| kana | | |
+3 <a href=Ged.GLOSSARY.md#romn>ROMN</a> | char{1:120} | | |
+4 <a href=Ged.GLOSSARY.md#type>TYPE</a> | &lt;<a href=Ged.ROMANIZED_TYPE.md>ROMANIZED_TYPE</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#map>MAP</a> |  | | |
+4 <a href=Ged.GLOSSARY.md#lati>LATI</a> | char{5:8} | | |
+4 <a href=Ged.GLOSSARY.md#long>LONG</a> | char{5:8} | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+4 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#addr>ADDR</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#adr1>ADR1</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#adr2>ADR2</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#adr3>ADR3</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#city>CITY</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#stae>STAE</a> | char{1:60} | | |
+3 <a href=Ged.GLOSSARY.md#post>POST</a> | char{1:10} | | |
+3 <a href=Ged.GLOSSARY.md#ctry>CTRY</a> | char{1:60} | | |
+2 <a href=Ged.GLOSSARY.md#phon>PHON</a> | char{1:25} | | |
+2 <a href=Ged.GLOSSARY.md#email>EMAIL</a> | char{5:120} | | |
+2 <a href=Ged.GLOSSARY.md#fax>FAX</a> | char{5:60} | | |
+2 <a href=Ged.GLOSSARY.md#www>WWW</a> | char{5:120} | | |
+2 <a href=Ged.GLOSSARY.md#agnc>AGNC</a> | char{1:120} | | |
+2 <a href=Ged.GLOSSARY.md#reli>RELI</a> | char{1:90} | | |
+2 <a href=Ged.GLOSSARY.md#caus>CAUS</a> | char{1:90} | | |
+2 <a href=Ged.GLOSSARY.md#resn>RESN</a> | confidential \| locked \| privacy  | | |
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
+1 <a href=Ged.GLOSSARY.md#husb>HUSB</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#wife>WIFE</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#chil>CHIL</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#nchi>NCHI</a> | char{1:3} | | |
+1 <a href=Ged.GLOSSARY.md#subm>SUBM</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#slgs>SLGS</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#temp>TEMP</a> | char{4:5} | | |
+2 <a href=Ged.GLOSSARY.md#plac>PLAC</a> | &lt;<a href=Ged.PLACE_NAME.md>PLACE_NAME</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#stat>STAT</a> |  CANCELED \| COMPLETED \| DNS \| EXCLUDED \| DNS/CAN \| PRE-1970 \| SUBMITTED \| UNCLEARED  | | |
+3 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_EXACT.md>DATE_EXACT</a>&gt; | | |
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
+1 <a href=Ged.GLOSSARY.md#refn>REFN</a> | char{1:20} | | |
+2 <a href=Ged.GLOSSARY.md#type>TYPE</a> | char{1:40} | | |
+1 <a href=Ged.GLOSSARY.md#rin>RIN</a> | char{1:12} | | |
+1 <a href=Ged.GLOSSARY.md#chan>CHAN</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_EXACT.md>DATE_EXACT</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#time>TIME</a> |  hh:mm:ss.fs  | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+3 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
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


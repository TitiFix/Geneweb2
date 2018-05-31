# SOURCE_RECORD
## Abstract
Source records are used to provide a bibliographic description of the source cited.


## GEDCOM syntax and proprietary extensions

**SOURCE_RECORD**:=
<pre>
<b>n @&lt;<a href=Ged.XREF_SOUR.md>XREF:SOUR</a>&gt;@ SOUR{1:1}</b>
  +1 DATA{0:1}
    +2 EVEN &lt;<a href=Ged.EVENTS_RECORDED.md>EVENTS_RECORDED</a>&gt;{0:M}
      +3 DATE &lt;<a href=Ged.DATE_PERIOD.md>DATE_PERIOD</a>&gt;{0:1}
      +3 PLAC &lt;<a href=Ged.SOURCE_JURISDICTION_PLACE.md>SOURCE_JURISDICTION_PLACE</a>&gt;{0:1}
    +2 AGNC &lt;<a href=Ged.RESPONSIBLE_AGENCY.md>RESPONSIBLE_AGENCY</a>&gt;{0:1}
    +2 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 AUTH &lt;<a href=Ged.SOURCE_ORIGINATOR.md>SOURCE_ORIGINATOR</a>&gt;{0:1}
    +2 [CONC|CONT] &lt;<a href=Ged.SOURCE_ORIGINATOR.md>SOURCE_ORIGINATOR</a>&gt;{0:M}
  +1 TITL &lt;<a href=Ged.SOURCE_DESCRIPTIVE_TITLE.md>SOURCE_DESCRIPTIVE_TITLE</a>&gt;{0:1}
    +2 [CONC|CONT] &lt;<a href=Ged.SOURCE_DESCRIPTIVE_TITLE.md>SOURCE_DESCRIPTIVE_TITLE</a>&gt;{0:M}
  +1 ABBR &lt;<a href=Ged.SOURCE_FILED_BY_ENTRY.md>SOURCE_FILED_BY_ENTRY</a>&gt;{0:1}
  +1 PUBL &lt;<a href=Ged.SOURCE_PUBLICATION_FACTS.md>SOURCE_PUBLICATION_FACTS</a>&gt;{0:1}
    +2 [CONC|CONT] &lt;<a href=Ged.SOURCE_PUBLICATION_FACTS.md>SOURCE_PUBLICATION_FACTS</a>&gt;{0:M}
  +1 TEXT &lt;<a href=Ged.TEXT_FROM_SOURCE.md>TEXT_FROM_SOURCE</a>&gt;{0:1}
    +2 [CONC|CONT] &lt;<a href=Ged.TEXT_FROM_SOURCE.md>TEXT_FROM_SOURCE</a>&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.SOURCE_REPOSITORY_CITATION.md>SOURCE_REPOSITORY_CITATION</a>&gt;&gt;{0:M}
  +1 REFN &lt;<a href=Ged.USER_REFERENCE_NUMBER.md>USER_REFERENCE_NUMBER</a>&gt;{0:M}
    +2 TYPE &lt;<a href=Ged.USER_REFERENCE_TYPE.md>USER_REFERENCE_TYPE</a>&gt;{0:1}
  +1 RIN &lt;<a href=Ged.AUTOMATED_RECORD_ID.md>AUTOMATED_RECORD_ID</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.CHANGE_STRUCTURE.md>CHANGE_STRUCTURE</a>&gt;&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.MULTIMEDIA_LINK.md>MULTIMEDIA_LINK</a>&gt;&gt;{0:M}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />


NOTE: See the &lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt;> structure, which contains the pointer to this source record.

## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#sour>SOUR</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#data>DATA</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#even>EVEN</a> | &lt;<a href=Ged.EVENTS_RECORDED.md>EVENTS_RECORDED</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_PERIOD.md>DATE_PERIOD</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#plac>PLAC</a> | &lt;<a href=Ged.PLACE_NAME.md>PLACE_NAME</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#agnc>AGNC</a> | char{1:120} | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+3 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+1 <a href=Ged.GLOSSARY.md#auth>AUTH</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+1 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+1 <a href=Ged.GLOSSARY.md#abbr>ABBR</a> | char{ 1:60} | | |
+1 <a href=Ged.GLOSSARY.md#publ>PUBL</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+1 <a href=Ged.GLOSSARY.md#text>TEXT</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+1 <a href=Ged.GLOSSARY.md#repo>REPO</a> | [@XREF:REPO@\|NULL] | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+3 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#caln>CALN</a> | char{1:120} | | |
+3 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
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


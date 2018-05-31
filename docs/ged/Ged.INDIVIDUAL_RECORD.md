# INDIVIDUAL_RECORD
## Abstract
The individual record is a compilation of facts, known or discovered, about an individual.  Sometimes
these facts are from different sources.  This form allows documentation of the source where each of
the facts were discovered.
The normal lineage links are shown through the use of pointers from the individual to a family through either the FAMC tag or the FAMS tag.  The FAMC tag provides a pointer to a family where this person is a child.  The FAMS tag provides a pointer to a family where this person is a spouse or parent.  The &lt;<a href=Ged.CHILD_TO_FAMILY_LINK.md>CHILD_TO_FAMILY_LINK</a>&gt; structure contains a FAMC pointer which is required to show any child to parent linkage for pedigree navigation.  The &lt;<a href=Ged.CHILD_TO_FAMILY_LINK.md>CHILD_TO_FAMILY_LINK</a>&gt; structure also indicates whether the pedigree link represents a birth lineage, an adoption lineage, or a sealing lineage.


## GEDCOM syntax and proprietary extensions

**INDIVIDUAL_RECORD**:=
<pre>
<b>n @&lt;<a href=Ged.XREF_INDI.md>XREF:INDI</a>&gt;@ INDI{1:1}</b>
  +1 RESN &lt;<a href=Ged.RESTRICTION_NOTICE.md>RESTRICTION_NOTICE</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.PERSONAL_NAME_STRUCTURE.md>PERSONAL_NAME_STRUCTURE</a>&gt;&gt;{0:M}
  +1 SEX &lt;<a href=Ged.SEX_VALUE.md>SEX_VALUE</a>&gt; {0:1}
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_STRUCTURE.md>INDIVIDUAL_EVENT_STRUCTURE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_ATTRIBUTE_STRUCTURE.md>INDIVIDUAL_ATTRIBUTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.LDS_INDIVIDUAL_ORDINANCE.md>LDS_INDIVIDUAL_ORDINANCE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.CHILD_TO_FAMILY_LINK.md>CHILD_TO_FAMILY_LINK</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.SPOUSE_TO_FAMILY_LINK.md>SPOUSE_TO_FAMILY_LINK</a>&gt;&gt;{0:M}
  +1 SUBM @&lt;<a href=Ged.XREF_SUBM.md>XREF:SUBM</a>&gt;@{0:M}
  +1 &lt;&lt;<a href=Ged.ASSOCIATION_STRUCTURE.md>ASSOCIATION_STRUCTURE</a>&gt;&gt;{0:M}
  +1 ALIA @&lt;<a href=Ged.XREF_INDI.md>XREF:INDI</a>&gt;@{0:M}
  +1 ANCI @&lt;<a href=Ged.XREF_SUBM.md>XREF:SUBM</a>&gt;@{0:M}
  +1 DESI @&lt;<a href=Ged.XREF_SUBM.md>XREF:SUBM</a>&gt;@{0:M}
  +1 RFN &lt;<a href=Ged.PERMANENT_RECORD_FILE_NUMBER.md>PERMANENT_RECORD_FILE_NUMBER</a>&gt;{0:1}
  +1 AFN &lt;<a href=Ged.ANCESTRAL_FILE_NUMBER.md>ANCESTRAL_FILE_NUMBER</a>&gt;{0:1}
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
Linkage between a child and the family they belonged to at the time of an event can also be shown
by a FAMC pointer subordinate to the appropriate event.  For example, a FAMC pointer subordinate
to an adoption event indicates a relationship to family by adoption. Biological parents can be shown
by a FAMC pointer subordinate to the birth event(optional).
Other associations or relationships are represented by the ASSOciation tag.  The person's relation
or association is the person being pointed to. The association or relationship is stated by the value
on the subordinate RELA line.
For example:
' 0 @I1@ INDI
' 1 NAME Fred/Jones/
' 1 ASSO @I2@
' 2 RELA Godfather

## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#indi>INDI</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#resn>RESN</a> | confidential \| locked \| privacy  | | |
+1 <a href=Ged.GLOSSARY.md#name>NAME</a> | &lt;<a href=Ged.NAME_PERSONAL.md>NAME_PERSONAL</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#type>TYPE</a> |  aka \| birth \| immigrant \| maiden \| married \| user_defined  | | |
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
+2 <a href=Ged.GLOSSARY.md#fone>FONE</a> | char{1:120} | | |
+3 <a href=Ged.GLOSSARY.md#type>TYPE</a> |  user_defined \| hangul \| kana | | |
+3 <a href=Ged.GLOSSARY.md#npfx>NPFX</a> | &lt;<a href=Ged.NAME_PIECE_PREFIX.md>NAME_PIECE_PREFIX</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#givn>GIVN</a> | &lt;<a href=Ged.NAME_PIECE_GIVEN.md>NAME_PIECE_GIVEN</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#nick>NICK</a> | &lt;<a href=Ged.NAME_PIECE_NICKNAME.md>NAME_PIECE_NICKNAME</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#spfx>SPFX</a> | &lt;<a href=Ged.NAME_PIECE_SURNAME_PREFIX.md>NAME_PIECE_SURNAME_PREFIX</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#surn>SURN</a> | &lt;<a href=Ged.NAME_PIECE_SURNAME.md>NAME_PIECE_SURNAME</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#nsfx>NSFX</a> | &lt;<a href=Ged.NAME_PIECE_SUFFIX.md>NAME_PIECE_SUFFIX</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+4 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+3 <a href=Ged.GLOSSARY.md#sour>SOUR</a> | @XREF{1:22}@ | | |
+4 <a href=Ged.GLOSSARY.md#page>PAGE</a> | char{1:248} | | |
+4 <a href=Ged.GLOSSARY.md#even>EVEN</a> | &lt;<a href=Ged.EVENT_TYPE_CITED_FROM.md>EVENT_TYPE_CITED_FROM</a>&gt; | | |
+5 <a href=Ged.GLOSSARY.md#role>ROLE</a> | &lt;<a href=Ged.ROLE_IN_EVENT.md>ROLE_IN_EVENT</a>&gt; | | |
+4 <a href=Ged.GLOSSARY.md#data>DATA</a> |  | | |
+5 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | | |
+5 <a href=Ged.GLOSSARY.md#text>TEXT</a> | char{1:248} | | |
+6 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+4 <a href=Ged.GLOSSARY.md#obje>OBJE</a> | @XREF{1:22}@ | | |
+4 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+5 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+6 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+5 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+7 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+4 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+5 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+5 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+5 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+6 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+4 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+4 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+5 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+4 <a href=Ged.GLOSSARY.md#quay>QUAY</a> |  0 \| 1 \| 2 \| 3  | | |
+3 <a href=Ged.GLOSSARY.md#sour>SOUR</a> | char{1:248} | | |
+4 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+4 <a href=Ged.GLOSSARY.md#text>TEXT</a> | char{1:248} | | |
+5 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+4 <a href=Ged.GLOSSARY.md#obje>OBJE</a> | @XREF{1:22}@ | | |
+4 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+5 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+6 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+5 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+7 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+4 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+5 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+5 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+5 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+6 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+4 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+4 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+5 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+4 <a href=Ged.GLOSSARY.md#quay>QUAY</a> |  0 \| 1 \| 2 \| 3  | | |
+2 <a href=Ged.GLOSSARY.md#romn>ROMN</a> | char{1:120} | | |
+3 <a href=Ged.GLOSSARY.md#type>TYPE</a> | &lt;<a href=Ged.ROMANIZED_TYPE.md>ROMANIZED_TYPE</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#npfx>NPFX</a> | &lt;<a href=Ged.NAME_PIECE_PREFIX.md>NAME_PIECE_PREFIX</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#givn>GIVN</a> | &lt;<a href=Ged.NAME_PIECE_GIVEN.md>NAME_PIECE_GIVEN</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#nick>NICK</a> | &lt;<a href=Ged.NAME_PIECE_NICKNAME.md>NAME_PIECE_NICKNAME</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#spfx>SPFX</a> | &lt;<a href=Ged.NAME_PIECE_SURNAME_PREFIX.md>NAME_PIECE_SURNAME_PREFIX</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#surn>SURN</a> | &lt;<a href=Ged.NAME_PIECE_SURNAME.md>NAME_PIECE_SURNAME</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#nsfx>NSFX</a> | &lt;<a href=Ged.NAME_PIECE_SUFFIX.md>NAME_PIECE_SUFFIX</a>&gt; | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+3 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+4 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+3 <a href=Ged.GLOSSARY.md#sour>SOUR</a> | @XREF{1:22}@ | | |
+4 <a href=Ged.GLOSSARY.md#page>PAGE</a> | char{1:248} | | |
+4 <a href=Ged.GLOSSARY.md#even>EVEN</a> | &lt;<a href=Ged.EVENT_TYPE_CITED_FROM.md>EVENT_TYPE_CITED_FROM</a>&gt; | | |
+5 <a href=Ged.GLOSSARY.md#role>ROLE</a> | &lt;<a href=Ged.ROLE_IN_EVENT.md>ROLE_IN_EVENT</a>&gt; | | |
+4 <a href=Ged.GLOSSARY.md#data>DATA</a> |  | | |
+5 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | | |
+5 <a href=Ged.GLOSSARY.md#text>TEXT</a> | char{1:248} | | |
+6 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+4 <a href=Ged.GLOSSARY.md#obje>OBJE</a> | @XREF{1:22}@ | | |
+4 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+5 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+6 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+5 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+7 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+4 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+5 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+5 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+5 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+6 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+4 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+4 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+5 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+4 <a href=Ged.GLOSSARY.md#quay>QUAY</a> |  0 \| 1 \| 2 \| 3  | | |
+3 <a href=Ged.GLOSSARY.md#sour>SOUR</a> | char{1:248} | | |
+4 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+4 <a href=Ged.GLOSSARY.md#text>TEXT</a> | char{1:248} | | |
+5 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+4 <a href=Ged.GLOSSARY.md#obje>OBJE</a> | @XREF{1:22}@ | | |
+4 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+5 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+6 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+5 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+7 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+4 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+5 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | | |
+5 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | | |
+5 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | | |
+6 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | | |
+4 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+4 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+5 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+4 <a href=Ged.GLOSSARY.md#quay>QUAY</a> |  0 \| 1 \| 2 \| 3  | | |
+1 <a href=Ged.GLOSSARY.md#sex>SEX</a> | char{1:7} | | |
+1 <a href=Ged.GLOSSARY.md#birt>BIRT</a>\|<a href=Ged.GLOSSARY.md#chr>CHR</a> | [Y\|NULL] | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#famc>FAMC</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#deat>DEAT</a> | [Y\|NULL] | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#buri>BURI</a>\|<a href=Ged.GLOSSARY.md#crem>CREM</a> |  | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#adop>ADOP</a> |  | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#famc>FAMC</a> | @XREF{1:22}@ | | |
+3 <a href=Ged.GLOSSARY.md#adop>ADOP</a> |  HUSB \| WIFE \| BOTH  | | |
+1 <a href=Ged.GLOSSARY.md#bapm>BAPM</a>\|<a href=Ged.GLOSSARY.md#barm>BARM</a>\|<a href=Ged.GLOSSARY.md#basm>BASM</a>\|<a href=Ged.GLOSSARY.md#bles>BLES</a> |  | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#chra>CHRA</a>\|<a href=Ged.GLOSSARY.md#conf>CONF</a>\|<a href=Ged.GLOSSARY.md#fcom>FCOM</a>\|<a href=Ged.GLOSSARY.md#ordn>ORDN</a> |  | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#natu>NATU</a>\|<a href=Ged.GLOSSARY.md#emig>EMIG</a>\|<a href=Ged.GLOSSARY.md#immi>IMMI</a> |  | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#cens>CENS</a>\|<a href=Ged.GLOSSARY.md#prob>PROB</a>\|<a href=Ged.GLOSSARY.md#will>WILL</a> |  | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#grad>GRAD</a>\|<a href=Ged.GLOSSARY.md#reti>RETI</a> |  | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#even>EVEN</a> | char{1:90}\|NULL | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#cast>CAST</a> | char{1:90} | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#dscr>DSCR</a> | char{1:248} | | |
+2 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#educ>EDUC</a> | char{1:248} | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#idno>IDNO</a> | char{1:30} | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#nati>NATI</a> | char{1:120} | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#nchi>NCHI</a> | char{1:3} | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#nmr>NMR</a> | char{1:3} | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#occu>OCCU</a> | char{1:90} | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#prop>PROP</a> | char{1:248} | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#reli>RELI</a> | char{1:90} | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#resi>RESI</a> | (* | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#ssn>SSN</a> | char{9:11} | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:120} | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#fact>FACT</a> | char{1:90} | | |
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
+2 <a href=Ged.GLOSSARY.md#age>AGE</a> | &lt;<a href=Ged.AGE_AT_EVENT.md>AGE_AT_EVENT</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#bapl>BAPL</a>\|<a href=Ged.GLOSSARY.md#conl>CONL</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#temp>TEMP</a> | char{4:5} | | |
+2 <a href=Ged.GLOSSARY.md#plac>PLAC</a> | &lt;<a href=Ged.PLACE_NAME.md>PLACE_NAME</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#stat>STAT</a> |  CHILD \| COMPLETED \| EXCLUDED \| PRE-1970 \| STILLBORN \| SUBMITTED \| UNCLEARED  | | |
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
+1 <a href=Ged.GLOSSARY.md#endl>ENDL</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#temp>TEMP</a> | char{4:5} | | |
+2 <a href=Ged.GLOSSARY.md#plac>PLAC</a> | &lt;<a href=Ged.PLACE_NAME.md>PLACE_NAME</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#stat>STAT</a> |  CHILD \| COMPLETED \| EXCLUDED \| PRE-1970 \|  STILLBORN \| SUBMITTED \| UNCLEARED  | | |
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
+1 <a href=Ged.GLOSSARY.md#slgc>SLGC</a> |  | | |
+2 <a href=Ged.GLOSSARY.md#date>DATE</a> | &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#temp>TEMP</a> | char{4:5} | | |
+2 <a href=Ged.GLOSSARY.md#plac>PLAC</a> | &lt;<a href=Ged.PLACE_NAME.md>PLACE_NAME</a>&gt; | | |
+2 <a href=Ged.GLOSSARY.md#famc>FAMC</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#stat>STAT</a> |  BIC \| COMPLETED \| EXCLUDED \| DNS \| PRE-1970 \| STILLBORN \| SUBMITTED \| UNCLEARED  | | |
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
+1 <a href=Ged.GLOSSARY.md#famc>FAMC</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#pedi>PEDI</a> |  adopted \| birth \| foster \| sealing  | | |
+2 <a href=Ged.GLOSSARY.md#stat>STAT</a> | challenged \| disproven \| proven | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+3 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+1 <a href=Ged.GLOSSARY.md#fams>FAMS</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+3 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+1 <a href=Ged.GLOSSARY.md#subm>SUBM</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#asso>ASSO</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#rela>RELA</a> | 0 INDI | | |
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
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+2 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+3 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |
+1 <a href=Ged.GLOSSARY.md#alia>ALIA</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#anci>ANCI</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#desi>DESI</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#rfn>RFN</a> | &lt;<a href=Ged.PERMANENT_RECORD_FILE_NUMBER.md>PERMANENT_RECORD_FILE_NUMBER</a>&gt; | | |
+1 <a href=Ged.GLOSSARY.md#afn>AFN</a> | char{1:12} | | |
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


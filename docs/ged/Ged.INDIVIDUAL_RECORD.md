# INDIVIDUAL_RECORD
## Abstract
The individual record is a compilation of facts, known or discovered, about an individual.  Sometimes
these facts are from different sources.  This form allows documentation of the source where each of
the facts were discovered.
The normal lineage links are shown through the use of pointers from the individual to a family
through either the FAMC tag or the FAMS tag.  The FAMC tag provides a pointer to a family where
this person is a child.  The FAMS tag provides a pointer to a family where this person is a spouse or
parent.  The <&lt;<a href=Ged.CHILD_TO_FAMILY_LINK.md>CHILD_TO_FAMILY_LINK</a>&gt;> structure contains a FAMC pointer
which is required to show any child to parent linkage for pedigree navigation.  The
<&lt;<a href=Ged.CHILD_TO_FAMILY_LINK.md>CHILD_TO_FAMILY_LINK</a>&gt;> structure also indicates whether the pedigree link represents a
birth lineage, an adoption lineage, or a sealing lineage.
Linkage between a child and the family they belonged to at the time of an event can also be shown
by a FAMC pointer subordinate to the appropriate event.  For example, a FAMC pointer subordinate
to an adoption event indicates a relationship to family by adoption. Biological parents can be shown
by a FAMC pointer subordinate to the birth event(optional).
Other associations or relationships are represented by the ASSOciation tag.  The person's relation
or association is the person being pointed to. The association or relationship is stated by the value
on the subordinate RELA line.


## GEDCOM syntax and proprietary extensions
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

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
NOTE: For example:
> 0 @I1@ INDI
> 1 NAME Fred/Jones/
> 1 ASSO @I2@
> 2 RELA Godfather
## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#indi>INDI</a> | @XREF:INDI@ | | |
+1 <a href=Ged.GLOSSARY.md#resn>RESN</a> | RESTRICTION_NOTICE | | |
+1  | PERSONAL_NAME_STRUCTURE | | |
+1 <a href=Ged.GLOSSARY.md#sex>SEX</a> | SEX_VALUE | | |
+1  | INDIVIDUAL_EVENT_STRUCTURE | | |
+1  | INDIVIDUAL_ATTRIBUTE_STRUCTURE | | |
+1  | LDS_INDIVIDUAL_ORDINANCE | | |
+1  | CHILD_TO_FAMILY_LINK | | |
+1  | SPOUSE_TO_FAMILY_LINK | | |
+1 <a href=Ged.GLOSSARY.md#subm>SUBM</a> | @XREF:SUBM@ | | |
+1  | ASSOCIATION_STRUCTURE | | |
+1 <a href=Ged.GLOSSARY.md#alia>ALIA</a> | @XREF:INDI@ | | |
+1 <a href=Ged.GLOSSARY.md#anci>ANCI</a> | @XREF:SUBM@ | | |
+1 <a href=Ged.GLOSSARY.md#desi>DESI</a> | @XREF:SUBM@ | | |
+1 <a href=Ged.GLOSSARY.md#rfn>RFN</a> | PERMANENT_RECORD_FILE_NUMBER | | |
+1 <a href=Ged.GLOSSARY.md#afn>AFN</a> | ANCESTRAL_FILE_NUMBER | | |
+1 <a href=Ged.GLOSSARY.md#refn>REFN</a> | USER_REFERENCE_NUMBER | | |
+2 <a href=Ged.GLOSSARY.md#type>TYPE</a> | USER_REFERENCE_TYPE | | |
+1 <a href=Ged.GLOSSARY.md#rin>RIN</a> | AUTOMATED_RECORD_ID | | |
+1  | CHANGE_STRUCTURE | | |
+1  | NOTE_STRUCTURE | | |
+1  | SOURCE_CITATION | | |
+1  | MULTIMEDIA_LINK | | |

:warning: to be continued/checked


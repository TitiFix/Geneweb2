# FAM_RECORD
## Abstract
The FAMily record is used to record marriages, common law marriages, and family unions caused by
two people becoming the parents of a child. There can be no more than one HUSB/father and one
WIFE/mother listed in each FAM_RECORD. If, for example, a man participated in more than one
family union, then he would appear in more than one FAM_RECORD. The family record structure
assumes that the HUSB/father is male and WIFE/mother is female.


## GEDCOM syntax and proprietary extensions
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

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
+0 <a href=Ged.GLOSSARY.md#fam>FAM</a> | @XREF:FAM@ | | |
+1 <a href=Ged.GLOSSARY.md#resn>RESN</a> | RESTRICTION_NOTICE | | |
+1  | FAMILY_EVENT_STRUCTURE | | |
+1 <a href=Ged.GLOSSARY.md#husb>HUSB</a> | @XREF:INDI@ | | |
+1 <a href=Ged.GLOSSARY.md#wife>WIFE</a> | @XREF:INDI@ | | |
+1 <a href=Ged.GLOSSARY.md#chil>CHIL</a> | @XREF:INDI@ | | |
+1 <a href=Ged.GLOSSARY.md#nchi>NCHI</a> | COUNT_OF_CHILDREN | | |
+1 <a href=Ged.GLOSSARY.md#subm>SUBM</a> | @XREF:SUBM@ | | |
+1  | LDS_SPOUSE_SEALING | | |
+1 <a href=Ged.GLOSSARY.md#refn>REFN</a> | USER_REFERENCE_NUMBER | | |
+2 <a href=Ged.GLOSSARY.md#type>TYPE</a> | USER_REFERENCE_TYPE | | |
+1 <a href=Ged.GLOSSARY.md#rin>RIN</a> | AUTOMATED_RECORD_ID | | |
+1  | CHANGE_STRUCTURE | | |
+1  | NOTE_STRUCTURE | | |
+1  | SOURCE_CITATION | | |
+1  | MULTIMEDIA_LINK | | |

:warning: to be continued/checked


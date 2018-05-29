# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**FAM_RECORD**:=
<pre>
<b>n @&lt;<a href=Ged.XREF_FAM>XREF:FAM</a>&gt;@ FAM{1:1}</b>
  +1 RESN &lt;<a href=Ged.RESTRICTION_NOTICE>RESTRICTION_NOTICE</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.FAMILY_EVENT_STRUCTURE>FAMILY_EVENT_STRUCTURE</a>&gt;&gt;{0:M}
  +1 HUSB @&lt;<a href=Ged.XREF_INDI>XREF:INDI</a>&gt;@{0:1}
  +1 WIFE @&lt;<a href=Ged.XREF_INDI>XREF:INDI</a>&gt;@{0:1}
  +1 CHIL @&lt;<a href=Ged.XREF_INDI>XREF:INDI</a>&gt;@{0:M} *
  +1 NCHI &lt;<a href=Ged.COUNT_OF_CHILDREN>COUNT_OF_CHILDREN</a>&gt;{0:1}
  +1 SUBM @&lt;<a href=Ged.XREF_SUBM>XREF:SUBM</a>&gt;@{0:M}
  +1 &lt;&lt;<a href=Ged.LDS_SPOUSE_SEALING>LDS_SPOUSE_SEALING</a>&gt;&gt;{0:M}
  +1 REFN &lt;<a href=Ged.USER_REFERENCE_NUMBER>USER_REFERENCE_NUMBER</a>&gt;{0:M}
    +2 TYPE &lt;<a href=Ged.USER_REFERENCE_TYPE>USER_REFERENCE_TYPE</a>&gt;{0:1}
  +1 RIN &lt;<a href=Ged.AUTOMATED_RECORD_ID>AUTOMATED_RECORD_ID</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.CHANGE_STRUCTURE>CHANGE_STRUCTURE</a>&gt;&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.SOURCE_CITATION>SOURCE_CITATION</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.MULTIMEDIA_LINK>MULTIMEDIA_LINK</a>&gt;&gt;{0:M}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE>LINEAGE_LINKED_STRUCTURE</a><br />


* NOTE :
The preferred order of the CHILdren pointers within a FAMily structure is chronological by birth.
# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
n @ | XREF:FAM | | |
+1 RESN | RESTRICTION_NOTICE | | |
+1 | FAMILY_EVENT_STRUCTURE | | |
+1 HUSB | @ | | |
+1 WIFE | @ | | |
+1 CHIL | @ | | |
+1 NCHI | COUNT_OF_CHILDREN | | |
+1 SUBM | @ | | |
+1 | LDS_SPOUSE_SEALING | | |
+1 REFN | USER_REFERENCE_NUMBER | | |
+2 TYPE | USER_REFERENCE_TYPE | | |
+1 RIN | AUTOMATED_RECORD_ID | | |
+1 | CHANGE_STRUCTURE | | |
+1 | NOTE_STRUCTURE | | |
+1 | SOURCE_CITATION | | |
+1 | MULTIMEDIA_LINK | | |

:warning: to be continued/checked


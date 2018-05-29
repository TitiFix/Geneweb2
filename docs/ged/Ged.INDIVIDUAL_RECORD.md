# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**INDIVIDUAL_RECORD**:=
<pre>
<b>n @XREF:INDI@ INDI{1:1}</b>
  +1 RESN &lt;<a href=Ged.RESTRICTION_NOTICE>RESTRICTION_NOTICE</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.PERSONAL_NAME_STRUCTURE>PERSONAL_NAME_STRUCTURE</a>&gt;&gt;{0:M}
  +1 SEX &lt;<a href=Ged.SEX_VALUE>SEX_VALUE</a>&gt; {0:1}
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_STRUCTURE>INDIVIDUAL_EVENT_STRUCTURE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_ATTRIBUTE_STRUCTURE>INDIVIDUAL_ATTRIBUTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.LDS_INDIVIDUAL_ORDINANCE>LDS_INDIVIDUAL_ORDINANCE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.CHILD_TO_FAMILY_LINK>CHILD_TO_FAMILY_LINK</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.SPOUSE_TO_FAMILY_LINK>SPOUSE_TO_FAMILY_LINK</a>&gt;&gt;{0:M}
  +1 SUBM @&lt;<a href=Ged.XREF_SUBM>XREF:SUBM</a>&gt;@{0:M}
  +1 &lt;&lt;<a href=Ged.ASSOCIATION_STRUCTURE>ASSOCIATION_STRUCTURE</a>&gt;&gt;{0:M}
  +1 ALIA @&lt;<a href=Ged.XREF_INDI>XREF:INDI</a>&gt;@{0:M}
  +1 ANCI @&lt;<a href=Ged.XREF_SUBM>XREF:SUBM</a>&gt;@{0:M}
  +1 DESI @&lt;<a href=Ged.XREF_SUBM>XREF:SUBM</a>&gt;@{0:M}
  +1 RFN &lt;<a href=Ged.PERMANENT_RECORD_FILE_NUMBER>PERMANENT_RECORD_FILE_NUMBER</a>&gt;{0:1}
  +1 AFN &lt;<a href=Ged.ANCESTRAL_FILE_NUMBER>ANCESTRAL_FILE_NUMBER</a>&gt;{0:1}
  +1 REFN &lt;<a href=Ged.USER_REFERENCE_NUMBER>USER_REFERENCE_NUMBER</a>&gt;{0:M}
    +2 TYPE &lt;<a href=Ged.USER_REFERENCE_TYPE>USER_REFERENCE_TYPE</a>&gt;{0:1}
  +1 RIN &lt;<a href=Ged.AUTOMATED_RECORD_ID>AUTOMATED_RECORD_ID</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.CHANGE_STRUCTURE>CHANGE_STRUCTURE</a>&gt;&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.SOURCE_CITATION>SOURCE_CITATION</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.MULTIMEDIA_LINK>MULTIMEDIA_LINK</a>&gt;&gt;{0:M}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE>LINEAGE_LINKED_STRUCTURE</a><br />

# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+1 RESN | RESTRICTION_NOTICE | | |
+1 | PERSONAL_NAME_STRUCTURE | | |
+1 SEX | SEX_VALUE | | |
+1 | INDIVIDUAL_EVENT_STRUCTURE | | |
+1 | INDIVIDUAL_ATTRIBUTE_STRUCTURE | | |
+1 | LDS_INDIVIDUAL_ORDINANCE | | |
+1 | CHILD_TO_FAMILY_LINK | | |
+1 | SPOUSE_TO_FAMILY_LINK | | |
+1 SUBM | @ | | |
+1 | ASSOCIATION_STRUCTURE | | |
+1 ALIA | @ | | |
+1 ANCI | @ | | |
+1 DESI | @ | | |
+1 RFN | PERMANENT_RECORD_FILE_NUMBER | | |
+1 AFN | ANCESTRAL_FILE_NUMBER | | |
+1 REFN | USER_REFERENCE_NUMBER | | |
+2 TYPE | USER_REFERENCE_TYPE | | |
+1 RIN | AUTOMATED_RECORD_ID | | |
+1 | CHANGE_STRUCTURE | | |
+1 | NOTE_STRUCTURE | | |
+1 | SOURCE_CITATION | | |
+1 | MULTIMEDIA_LINK | | |

:warning: to be continued/checked


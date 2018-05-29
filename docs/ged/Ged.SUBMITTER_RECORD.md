# Abstract
The submitter record identifies an individual or organization that contributed information contained
in the GEDCOM transmission. All records in the transmission are assumed to be submitted by the
SUBMITTER referenced in the HEADer, unless a SUBMitter reference inside a specific record
points at a different SUBMITTER record.


# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**SUBMITTER_RECORD**:=
<pre>
<b>n @&lt;<a href=Ged.XREF_SUBM.md>XREF:SUBM</a>&gt;@ SUBM{1:1}</b>
<b>  +1 NAME &lt;<a href=Ged.SUBMITTER_NAME.md>SUBMITTER_NAME</a>&gt;{1:1}</b>
  +1 &lt;&lt;<a href=Ged.ADDRESS_STRUCTURE.md>ADDRESS_STRUCTURE</a>&gt;&gt;{0:1} *
  +1 &lt;&lt;<a href=Ged.MULTIMEDIA_LINK.md>MULTIMEDIA_LINK</a>&gt;&gt;{0:M}
  +1 LANG &lt;<a href=Ged.LANGUAGE_PREFERENCE.md>LANGUAGE_PREFERENCE</a>&gt;{0:3}
  +1 RFN &lt;<a href=Ged.SUBMITTER_REGISTERED_RFN.md>SUBMITTER_REGISTERED_RFN</a>&gt;{0:1}
  +1 RIN &lt;<a href=Ged.AUTOMATED_RECORD_ID.md>AUTOMATED_RECORD_ID</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.CHANGE_STRUCTURE.md>CHANGE_STRUCTURE</a>&gt;&gt;{0:1}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />


NOTE : submissions to the ancestral file require the name and address of the submitter.
# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0  | XREF:SUBM | | |
+1 NAME | SUBMITTER_NAME | | |
+1  | ADDRESS_STRUCTURE | | |
+1  | MULTIMEDIA_LINK | | |
+1 LANG | LANGUAGE_PREFERENCE | | |
+1 RFN | SUBMITTER_REGISTERED_RFN | | |
+1 RIN | AUTOMATED_RECORD_ID | | |
+1  | NOTE_STRUCTURE | | |
+1  | CHANGE_STRUCTURE | | |

:warning: to be continued/checked


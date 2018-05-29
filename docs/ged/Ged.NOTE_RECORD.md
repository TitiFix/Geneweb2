# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**NOTE_RECORD**:=
<pre>
<b>n @&lt;<a href=Ged.XREF_NOTE.md>XREF:NOTE</a>&gt;@ NOTE &lt;<a href=Ged.SUBMITTER_TEXT.md>SUBMITTER_TEXT</a>&gt;{1:1}</b>
  +1 [CONC|CONT] &lt;<a href=Ged.SUBMITTER_TEXT.md>SUBMITTER_TEXT</a>&gt;{0:M}
  +1 REFN &lt;<a href=Ged.USER_REFERENCE_NUMBER.md>USER_REFERENCE_NUMBER</a>&gt;{0:M}
    +2 TYPE &lt;<a href=Ged.USER_REFERENCE_TYPE.md>USER_REFERENCE_TYPE</a>&gt;{0:1}
  +1 RIN &lt;<a href=Ged.AUTOMATED_RECORD_ID.md>AUTOMATED_RECORD_ID</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.CHANGE_STRUCTURE.md>CHANGE_STRUCTURE</a>&gt;&gt;{0:1}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />

# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
n@ | XREF:NOTE | | |
n@<XREF:NOTE>@ NOTE | SUBMITTER_TEXT | | |
+1 CONC/CONT | SUBMITTER_TEXT | | |
+1 REFN | USER_REFERENCE_NUMBER | | |
+2 TYPE | USER_REFERENCE_TYPE | | |
+1 RIN | AUTOMATED_RECORD_ID | | |
+1 | SOURCE_CITATION | | |
+1 | CHANGE_STRUCTURE | | |

:warning: to be continued/checked


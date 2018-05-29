# Abstract


# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**MULTIMEDIA_RECORD**:=
<pre>
<b>n @&lt;<a href=Ged.XREF_OBJE.md>XREF:OBJE</a>&gt;@ OBJE{1:1}</b>
<b>  +1 FILE &lt;<a href=Ged.MULTIMEDIA_FILE_REFN.md>MULTIMEDIA_FILE_REFN</a>&gt;{1:M}</b>
<b>    +2 FORM &lt;<a href=Ged.MULTIMEDIA_FORMAT.md>MULTIMEDIA_FORMAT</a>&gt;{1:1}</b>
      +3 TYPE &lt;<a href=Ged.SOURCE_MEDIA_TYPE.md>SOURCE_MEDIA_TYPE</a>&gt;{0:1}
    +2 TITL &lt;<a href=Ged.DESCRIPTIVE_TITLE.md>DESCRIPTIVE_TITLE</a>&gt;{0:1}
  +1 REFN &lt;<a href=Ged.USER_REFERENCE_NUMBER.md>USER_REFERENCE_NUMBER</a>&gt;{0:M}
    +2 TYPE &lt;<a href=Ged.USER_REFERENCE_TYPE.md>USER_REFERENCE_TYPE</a>&gt;{0:1}
  +1 RIN &lt;<a href=Ged.AUTOMATED_RECORD_ID.md>AUTOMATED_RECORD_ID</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.CHANGE_STRUCTURE.md>CHANGE_STRUCTURE</a>&gt;&gt;{0:1}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />


NOTE : The BLOB context of the multimedia record was removed in version 5.5.1. A reference to a multimedia
file was added to the record structure.  The file reference occurs one to many times so that multiple files
can be grouped together, each pertaining to the same context. For example, if you wanted to associate a
sound clip and a photo, you would reference each multimedia file and indicate the format using the
FORM tag subordinate to each file reference.
# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0  | XREF:OBJE | | |
+1 FILE | MULTIMEDIA_FILE_REFN | | |
+2 FORM | MULTIMEDIA_FORMAT | | |
+3 TYPE | SOURCE_MEDIA_TYPE | | |
+2 TITL | DESCRIPTIVE_TITLE | | |
+1 REFN | USER_REFERENCE_NUMBER | | |
+2 TYPE | USER_REFERENCE_TYPE | | |
+1 RIN | AUTOMATED_RECORD_ID | | |
+1  | NOTE_STRUCTURE | | |
+1  | SOURCE_CITATION | | |
+1  | CHANGE_STRUCTURE | | |

:warning: to be continued/checked


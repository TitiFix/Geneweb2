# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**MULTIMEDIA_RECORD**:=
<pre>
<b>n @&lt;<a href=Ged.XREF_OBJE>XREF:OBJE</a>&gt;@ OBJE{1:1}</b>
<b>  +1 FILE &lt;<a href=Ged.MULTIMEDIA_FILE_REFN>MULTIMEDIA_FILE_REFN</a>&gt;{1:M}</b>
<b>    +2 FORM &lt;<a href=Ged.MULTIMEDIA_FORMAT>MULTIMEDIA_FORMAT</a>&gt;{1:1}</b>
      +3 TYPE &lt;<a href=Ged.SOURCE_MEDIA_TYPE>SOURCE_MEDIA_TYPE</a>&gt;{0:1}
    +2 TITL &lt;<a href=Ged.DESCRIPTIVE_TITLE>DESCRIPTIVE_TITLE</a>&gt;{0:1}
  +1 REFN &lt;<a href=Ged.USER_REFERENCE_NUMBER>USER_REFERENCE_NUMBER</a>&gt;{0:M}
    +2 TYPE &lt;<a href=Ged.USER_REFERENCE_TYPE>USER_REFERENCE_TYPE</a>&gt;{0:1}
  +1 RIN &lt;<a href=Ged.AUTOMATED_RECORD_ID>AUTOMATED_RECORD_ID</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.SOURCE_CITATION>SOURCE_CITATION</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.CHANGE_STRUCTURE>CHANGE_STRUCTURE</a>&gt;&gt;{0:1}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE>LINEAGE_LINKED_STRUCTURE</a><br />

# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
n @ | XREF:OBJE | | |
+1 FILE | MULTIMEDIA_FILE_REFN | | |
+2 FORM | MULTIMEDIA_FORMAT | | |
+3 TYPE | SOURCE_MEDIA_TYPE | | |
+2 TITL | DESCRIPTIVE_TITLE | | |
+1 REFN | USER_REFERENCE_NUMBER | | |
+2 TYPE | USER_REFERENCE_TYPE | | |
+1 RIN | AUTOMATED_RECORD_ID | | |
+1 | NOTE_STRUCTURE | | |
+1 | SOURCE_CITATION | | |
+1 | CHANGE_STRUCTURE | | |

:warning: to be continued/checked


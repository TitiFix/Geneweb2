# Abstract


# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**MULTIMEDIA_LINK**:=
<pre>
<b>n OBJE @&lt;<a href=Ged.XREF_OBJE.md>XREF:OBJE</a>&gt;@ {1:1}</b>
| /* new 5.5.1 structure */
<b>n OBJE {1:1}</b>
<b>  +1 FILE &lt;<a href=Ged.MULTIMEDIA_FILE_REFN.md>MULTIMEDIA_FILE_REFN</a>&gt; {1:M}</b>
<b>    +2 FORM &lt;<a href=Ged.MULTIMEDIA_FORMAT.md>MULTIMEDIA_FORMAT</a>&gt; {1:1}</b>
      +3 MEDI &lt;<a href=Ged.SOURCE_MEDIA_TYPE.md>SOURCE_MEDIA_TYPE</a>&gt; {0:1}
  +1 TITL &lt;<a href=Ged.DESCRIPTIVE_TITLE.md>DESCRIPTIVE_TITLE</a>&gt; {0:1}
| /* 5.5 structure */
<b>n OBJE {1:1}</b>
<b>  +1 FILE &lt;<a href=Ged.MULTIMEDIA_FILE_REFN.md>MULTIMEDIA_FILE_REFN</a>&gt; {1:M}</b>
<b>  +1 FORM &lt;<a href=Ged.MULTIMEDIA_FORMAT.md>MULTIMEDIA_FORMAT</a>&gt; {1:1}</b>
    +2 MEDI&lt;<a href=Ged.SOURCE_MEDIA_TYPE.md>SOURCE_MEDIA_TYPE</a>&gt; {0:1}
</pre>
Used in <a href=Ged.FAM_RECORD.md>FAM_RECORD</a>, <a href=Ged.INDIVIDUAL_RECORD.md>INDIVIDUAL_RECORD</a>, <a href=Ged.SOURCE_RECORD.md>SOURCE_RECORD</a>, <a href=Ged.SUBMITTER_RECORD.md>SUBMITTER_RECORD</a>, <a href=Ged.EVENT_DETAIL.md>EVENT_DETAIL</a>, <a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a><br />


NOTE : some systems may have output the following 5.5 structure. The new context above was
introduced in order to allow a grouping of related multimedia files to a particular context.
# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 OBJE | XREF:OBJE | | |
+1 FILE | MULTIMEDIA_FILE_REFN | | |
+2 FORM | MULTIMEDIA_FORMAT | | |
+3 MEDI | SOURCE_MEDIA_TYPE | | |
+1 TITL | DESCRIPTIVE_TITLE | | |

:warning: to be continued/checked


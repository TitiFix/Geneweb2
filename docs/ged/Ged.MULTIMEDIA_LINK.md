# MULTIMEDIA_LINK
## Abstract


## GEDCOM syntax and proprietary extensions
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**MULTIMEDIA_LINK**:=
<pre>
<b>n OBJE @&lt;<a href=Ged.XREF_OBJE.md>XREF:OBJE</a>&gt;@ {1:1}</b>
| (* new 5.5.1 structure *)
<b>n OBJE {1:1}</b>
<b>  +1 FILE &lt;<a href=Ged.MULTIMEDIA_FILE_REFN.md>MULTIMEDIA_FILE_REFN</a>&gt; {1:M}</b>
<b>    +2 FORM &lt;<a href=Ged.MULTIMEDIA_FORMAT.md>MULTIMEDIA_FORMAT</a>&gt; {1:1}</b>
      +3 MEDI &lt;<a href=Ged.SOURCE_MEDIA_TYPE.md>SOURCE_MEDIA_TYPE</a>&gt; {0:1}
  +1 TITL &lt;<a href=Ged.DESCRIPTIVE_TITLE.md>DESCRIPTIVE_TITLE</a>&gt; {0:1}
| (* 5.5 structure *)
<b>n OBJE {1:1}</b>
<b>  +1 FILE &lt;<a href=Ged.MULTIMEDIA_FILE_REFN.md>MULTIMEDIA_FILE_REFN</a>&gt; {1:M}</b>
<b>  +1 FORM &lt;<a href=Ged.MULTIMEDIA_FORMAT.md>MULTIMEDIA_FORMAT</a>&gt; {1:1}</b>
    +2 MEDI&lt;<a href=Ged.SOURCE_MEDIA_TYPE.md>SOURCE_MEDIA_TYPE</a>&gt; {0:1}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />
NOTE: some systems may have output the following 5.5 structure. The new context above was
introduced in order to allow a grouping of related multimedia files to a particular context.
## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#obje>OBJE</a> | @XREF:OBJE@ | | |
+0 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+1 <a href=Ged.GLOSSARY.md#file>FILE</a> | MULTIMEDIA_FILE_REFN | | |
+2 <a href=Ged.GLOSSARY.md#form>FORM</a> | MULTIMEDIA_FORMAT | | |
+3 <a href=Ged.GLOSSARY.md#medi>MEDI</a> | SOURCE_MEDIA_TYPE | | |
+1 <a href=Ged.GLOSSARY.md#titl>TITL</a> | DESCRIPTIVE_TITLE | | |
+0 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | | |
+1 <a href=Ged.GLOSSARY.md#file>FILE</a> | MULTIMEDIA_FILE_REFN | | |
+1 <a href=Ged.GLOSSARY.md#form>FORM</a> | MULTIMEDIA_FORMAT | | |
+2 <a href=Ged.GLOSSARY.md#medi>MEDI</a> | SOURCE_MEDIA_TYPE | | |

:warning: to be continued/checked


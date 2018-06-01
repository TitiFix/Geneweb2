# MULTIMEDIA_LINK
## Abstract
An external multimedia file. The transfer of the multimedia files are external to GEDCOM. The 5.5 form with embedded objects are deprecated (BLOB Tag)


## GEDCOM syntax and proprietary extensions

**MULTIMEDIA_LINK**:=
<pre>
<b>n OBJE @&lt;<a href=Ged.XREF_OBJE.md>XREF:OBJE</a>&gt;@ {1:1}</b>
| (* 5.5.1 structure, n files per object possible *)
<b>n OBJE {1:1}</b>
  +1 TITL &lt;<a href=Ged.DESCRIPTIVE_TITLE.md>DESCRIPTIVE_TITLE</a>&gt; {0:1}
<b>    +2 FORM &lt;<a href=Ged.MULTIMEDIA_FORMAT.md>MULTIMEDIA_FORMAT</a>&gt; {1:1}</b>
<b>  +1 FILE &lt;<a href=Ged.MULTIMEDIA_FILE_REF.md>MULTIMEDIA_FILE_REF</a>&gt; {1:M}</b>
      +3 MEDI &lt;<a href=Ged.SOURCE_MEDIA_TYPE.md>SOURCE_MEDIA_TYPE</a>&gt; {0:1}
| (* 5.5 structure, 1 file per object only *)
<b>n OBJE {1:1}</b>
  +1 TITL &lt;<a href=Ged.DESCRIPTIVE_TITLE.md>DESCRIPTIVE_TITLE</a>&gt; {0:1}
<b>  +1 FORM &lt;<a href=Ged.MULTIMEDIA_FORMAT.md>MULTIMEDIA_FORMAT</a>&gt; {1:1}</b>
<b>  +1 FILE &lt;<a href=Ged.MULTIMEDIA_FILE_REF.md>MULTIMEDIA_FILE_REF</a>&gt; {1:1}</b>
    +2 MEDI&lt;<a href=Ged.SOURCE_MEDIA_TYPE.md>SOURCE_MEDIA_TYPE</a>&gt; {0:1}
</pre>
Used in <a href=Ged.FAMILY_RECORD.md>FAMILY_RECORD</a>, <a href=Ged.INDIVIDUAL_RECORD.md>INDIVIDUAL_RECORD</a>, <a href=Ged.SOURCE_RECORD.md>SOURCE_RECORD</a>, <a href=Ged.SUBMITTER_RECORD.md>SUBMITTER_RECORD</a>, <a href=Ged.FAMILY_EVENT_DETAIL.md>FAMILY_EVENT_DETAIL</a>, <a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>, <a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a><br />


NOTE: some systems may have output the following 5.5 structure. The new context above was
introduced in order to allow a grouping of related multimedia files to a particular context.

## Geneweb behavior

level tag  | Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#obje>OBJE</a> | @XREF{1:22}@ | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | ? | ? | 
+2 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | ? | ? | 
+3 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#obje>OBJE</a> |  | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | ? | ? | 
+2 <a href=Ged.GLOSSARY.md#medi>MEDI</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | ? | ? | 

🚧 to be continued/checked


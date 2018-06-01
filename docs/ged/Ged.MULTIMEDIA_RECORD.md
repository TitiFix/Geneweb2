# MULTIMEDIA_RECORD
## Abstract

## GEDCOM syntax and proprietary extensions

**MULTIMEDIA_RECORD**:=
<pre>
<b>n @&lt;<a href=Ged.XREF_OBJE.md>XREF:OBJE</a>&gt;@ OBJE{1:1}</b>
<b>  +1 FILE &lt;<a href=Ged.MULTIMEDIA_FILE_REF.md>MULTIMEDIA_FILE_REF</a>&gt;{1:M}</b>
<b>    +2 FORM &lt;<a href=Ged.MULTIMEDIA_FORMAT.md>MULTIMEDIA_FORMAT</a>&gt;{1:1}</b>
      +3 TYPE &lt;<a href=Ged.SOURCE_MEDIA_TYPE.md>SOURCE_MEDIA_TYPE</a>&gt;{0:1}
    +2 TITL &lt;<a href=Ged.DESCRIPTIVE_TITLE.md>DESCRIPTIVE_TITLE</a>&gt;{0:1}
  +1 REFN &lt;<a href=Ged.USER_REFERENCE_NUMBER.md>USER_REFERENCE_NUMBER</a>&gt;{0:M} &#x1F5D1;
    +2 TYPE &lt;<a href=Ged.USER_REFERENCE_TYPE.md>USER_REFERENCE_TYPE</a>&gt;{0:1} &#x1F5D1;
  +1 RIN &lt;<a href=Ged.AUTOMATED_RECORD_ID.md>AUTOMATED_RECORD_ID</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.CHANGE_STRUCTURE.md>CHANGE_STRUCTURE</a>&gt;&gt;{0:1}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />


NOTE: The BLOB context of the multimedia record was removed in version 5.5.1. A reference to a multimedia
file was added to the record structure.  The file reference occurs one to many times so that multiple files
can be grouped together, each pertaining to the same context. For example, if you wanted to associate a
sound clip and a photo, you would reference each multimedia file and indicate the format using the
FORM tag subordinate to each file reference.

## Geneweb behavior

level tag  | Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#obje>OBJE</a> | @XREF{1:22}@ | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#file>FILE</a> | char{1:30} | ? | ? | 
+2 <a href=Ged.GLOSSARY.md#form>FORM</a> |  bmp \| gif \| jpg \| ole \| pcx \| tif \| wav  | ? | ? | 
+3 <a href=Ged.GLOSSARY.md#type>TYPE</a> |  audio \| book \| card \| electronic \| fiche \| film \| magazine \| manuscript \| map \| newspaper \| photo \| tombstone \| video  | ? | ? | 
+2 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:248} | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#refn>REFN</a> | 🗑 deprecated | ? | ? | 
+2 <a href=Ged.GLOSSARY.md#type>TYPE</a> | 🗑 deprecated | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#rin>RIN</a> | char{1:12} | ? | ? | 
+1  | &lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt; | ? | ? | 
+1  | &lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt; | ? | ? | 
+1  | &lt;<a href=Ged.CHANGE_STRUCTURE.md>CHANGE_STRUCTURE</a>&gt; | ? | ? | 

🚧 to be continued/checked


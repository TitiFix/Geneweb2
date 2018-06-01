# SUBMITTER_RECORD
## Abstract
The submitter record identifies an individual or organization that contributed information contained
in the GEDCOM transmission.


## GEDCOM syntax and proprietary extensions

**SUBMITTER_RECORD**:=
<pre>
<b>n @&lt;<a href=Ged.XREF_SUBM.md>XREF:SUBM</a>&gt;@ SUBM{1:1}</b>
<b>  +1 NAME &lt;<a href=Ged.SUBMITTER_NAME.md>SUBMITTER_NAME</a>&gt;{1:1}</b>
  +1 &lt;&lt;<a href=Ged.ADDRESS_STRUCTURE.md>ADDRESS_STRUCTURE</a>&gt;&gt;{0:1}*
  +1 &lt;&lt;<a href=Ged.MULTIMEDIA_LINK.md>MULTIMEDIA_LINK</a>&gt;&gt;{0:M}
  +1 LANG &lt;<a href=Ged.LANGUAGE_PREFERENCE.md>LANGUAGE_PREFERENCE</a>&gt;{0:3}
  +1 RFN &lt;<a href=Ged.SUBMITTER_REGISTERED_RFN.md>SUBMITTER_REGISTERED_RFN</a>&gt;{0:1} &#x1F5D1;
  +1 RIN &lt;<a href=Ged.AUTOMATED_RECORD_ID.md>AUTOMATED_RECORD_ID</a>&gt;{0:1}
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.CHANGE_STRUCTURE.md>CHANGE_STRUCTURE</a>&gt;&gt;{0:1}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />


NOTE:
- All records in the file are assumed to be submitted by the SUBMITTER referenced in the HEADer, unless a SUBMitter reference inside a specific record points at a different SUBMITTER record.
- Submissions to the ancestral file require the name and address of the submitter.

## Geneweb behavior

level tag  | Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#subm>SUBM</a> | @XREF{1:22}@ | ignore | missing &#x26A0; | Must be add to the header.
+1 <a href=Ged.GLOSSARY.md#name>NAME</a> | char{1:60} | ignore | no | 
+1  | &lt;<a href=Ged.ADDRESS_STRUCTURE.md>ADDRESS_STRUCTURE</a>&gt; | ignore | no | 
+1  | &lt;<a href=Ged.MULTIMEDIA_LINK.md>MULTIMEDIA_LINK</a>&gt; | ignore | no | 
+1 <a href=Ged.GLOSSARY.md#lang>LANG</a> | &lt;<a href=Ged.LANGUAGE_ID.md>LANGUAGE_ID</a>&gt; | ignore | no | 
+1 <a href=Ged.GLOSSARY.md#rfn>RFN</a> | 🗑 deprecated | ignore | no | 
+1 <a href=Ged.GLOSSARY.md#rin>RIN</a> | char{1:12} | ignore | no | 
+1  | &lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt; | ignore | no | 
+1  | &lt;<a href=Ged.CHANGE_STRUCTURE.md>CHANGE_STRUCTURE</a>&gt; | ignore | no | 




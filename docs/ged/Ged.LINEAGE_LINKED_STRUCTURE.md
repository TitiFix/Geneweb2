<!-- licence GPL V2, cf https://github.com/TitiFix/geneweb -->
# LINEAGE_LINKED_STRUCTURE
## Abstract
&#x1F6A7; **DOCUMENTATION UNDER CONSTRUCTION - NO DUE DATE** - &#x1F6A7;
The lineage-linked GEDCOM structure is the main structure of GEDCOM files. A header and a trailer record are required, and they can enclose any number of data records. Tags must be used in the same context as shown in the following form. User defined tags must be used (begin with an under-score, see &lt;<a href=Ged.USER_DEFINED_TAG.md>USER_DEFINED_TAG</a>&gt; ).


## GEDCOM syntax and proprietary extensions

**LINEAGE_LINKED_STRUCTURE**:=
<pre>
<b>0 &lt;&lt;<a href=Ged.HEADER_RECORD.md>HEADER_RECORD</a>&gt;&gt;{1:1}</b>
0 &lt;&lt;<a href=Ged.SUBMISSION_RECORD.md>SUBMISSION_RECORD</a>&gt;&gt;{0:1} &#x1F5D1;
<b>0 &lt;&lt;<a href=Ged.SUBMITTER_RECORD.md>SUBMITTER_RECORD</a>&gt;&gt;{1:1}</b>
0 &lt;&lt;<a href=Ged.INDIVIDUAL_RECORD.md>INDIVIDUAL_RECORD</a>&gt;&gt;{0:M}
0 &lt;&lt;<a href=Ged.FAMILY_RECORD.md>FAMILY_RECORD</a>&gt;&gt;{0:M}
0 &lt;&lt;<a href=Ged.MULTIMEDIA_RECORD.md>MULTIMEDIA_RECORD</a>&gt;&gt;{0:M}
0 &lt;&lt;<a href=Ged.NOTE_RECORD.md>NOTE_RECORD</a>&gt;&gt;{0:M}
0 &lt;&lt;<a href=Ged.REPOSITORY_RECORD.md>REPOSITORY_RECORD</a>&gt;&gt;{0:M}
0 &lt;&lt;<a href=Ged.SOURCE_RECORD.md>SOURCE_RECORD</a>&gt;&gt;{0:M}
<b>0 &lt;&lt;<a href=Ged.TRLR_RECORD.md>TRLR_RECORD</a>&gt;&gt;{1:1}</b>
</pre>

NOTE: This documentation is not a copy of the GEDCOM standard (Some grammars errors are corrected, some field names are renamed for improved understanding, deprecated tag are identified, several version are mixed to determine GENEWEB behavior with old tag, commonly extension after the draft 5.5.1 publication are included). In these documentation the following conventions are used :
- **bold** when field is mandatory
- (* texte *) : a comment for the reader (not to reproduce in gedcom file production).
and following symbols are used :
- &#x26A0; indicate "attention required"
- &#x1F6A7; indicate "an information to be completed"
- &#x1F4CD; indicate "need an evolution"
- &#x1F5D1; indicate "obsolete, do not use"
- &#x25B6; indicate "a modification add by 5.5.1 draft"
- &#x23E9; indicate "proprietary extension/coding commonly used (standard 5.5.x update needed)"

## Geneweb behavior



The &lt;&lt;<a href=Ged.SUBMITTER_RECORD.md>SUBMITTER_RECORD</a>&gt;&gt;, &lt;&lt;<a href=Ged.SOURCE_RECORD.md>SOURCE_RECORD</a>&gt;&gt;, &lt;&lt;<a href=Ged.REPOSITORY_RECORD.md>REPOSITORY_RECORD</a>&gt;&gt; are not supported (ignored at GEDCOM import and, therefore not generated). if ged2web -iun import option is used &lt;<a href=Ged.XREF_SOUR.md>XREF:SOUR</a>&gt; is included in individual or family notes.

&#x1F6A7; **DOCUMENTATION UNDER CONSTRUCTION - NO DUE DATE** - &#x1F6A7;



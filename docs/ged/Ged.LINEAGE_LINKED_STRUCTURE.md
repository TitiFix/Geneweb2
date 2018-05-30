# LINEAGE_LINKED_STRUCTURE
## Abstract
The lineage-linked GEDCOM structure is the main structure of GEDCOM files. A header and a trailer record are required, and they can enclose any number of data records. Tags must be used in the same context as shown in the following form. User defined tags must be used (begin with an under-score, see &lt;<a href=Ged.USER_DEFINED_TAG.md>USER_DEFINED_TAG</a>&gt; ).


## GEDCOM syntax and proprietary extensions
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**LINEAGE_LINKED_STRUCTURE**:=
<pre>
<b>0 &lt;&lt;<a href=Ged.HEADER_RECORD.md>HEADER_RECORD</a>&gt;&gt;{1:1}</b>
0 &lt;&lt;<a href=Ged.SUBMISSION_RECORD.md>SUBMISSION_RECORD</a>&gt;&gt;{0:1}
<b>0 &lt;&lt;<a href=Ged.SUBMITTER_RECORD.md>SUBMITTER_RECORD</a>&gt;&gt;{1:1}</b>
0 &lt;&lt;<a href=Ged.INDIVIDUAL_RECORD.md>INDIVIDUAL_RECORD</a>&gt;&gt;{0:M}
0 &lt;&lt;<a href=Ged.FAM_RECORD.md>FAM_RECORD</a>&gt;&gt;{0:M}
0 &lt;&lt;<a href=Ged.MULTIMEDIA_RECORD.md>MULTIMEDIA_RECORD</a>&gt;&gt;{0:M}
0 &lt;&lt;<a href=Ged.NOTE_RECORD.md>NOTE_RECORD</a>&gt;&gt;{0:M}
0 &lt;&lt;<a href=Ged.REPOSITORY_RECORD.md>REPOSITORY_RECORD</a>&gt;&gt;{0:M}
0 &lt;&lt;<a href=Ged.SOURCE_RECORD.md>SOURCE_RECORD</a>&gt;&gt;{0:M}
<b>0 &lt;&lt;<a href=Ged.TRLR_RECORD.md>TRLR_RECORD</a>&gt;&gt;{1:1}</b>
</pre>
## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0  | HEADER_RECORD | | |
+0  | SUBMISSION_RECORD | | |
+0  | SUBMITTER_RECORD | | |
+0  | INDIVIDUAL_RECORD | | |
+0  | FAM_RECORD | | |
+0  | MULTIMEDIA_RECORD | | |
+0  | NOTE_RECORD | | |
+0  | REPOSITORY_RECORD | | |
+0  | SOURCE_RECORD | | |
+0  | TRLR_RECORD | | |

:warning: to be continued/checked


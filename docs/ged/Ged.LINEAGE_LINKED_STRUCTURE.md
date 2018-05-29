# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**LINEAGE_LINKED_STRUCTURE**:=
<pre>
<b>0 &lt;&lt;<a href=Ged.HEADER_RECORD>HEADER_RECORD</a>&gt;&gt;{1:1}</b>
0 &lt;&lt;<a href=Ged.SUBMISSION_RECORD>SUBMISSION_RECORD</a>&gt;&gt;{0:1}
<b>0 &lt;&lt;<a href=Ged.SUBMITTER_RECORD>SUBMITTER_RECORD</a>&gt;&gt;{1:1}</b>
0 &lt;&lt;<a href=Ged.INDIVIDUAL_RECORD>INDIVIDUAL_RECORD</a>&gt;&gt;{0:M}
0 &lt;&lt;<a href=Ged.FAM_RECORD>FAM_RECORD</a>&gt;&gt;{0:M}
0 &lt;&lt;<a href=Ged.MULTIMEDIA_RECORD>MULTIMEDIA_RECORD</a>&gt;&gt;{0:M}
0 &lt;&lt;<a href=Ged.NOTE_RECORD>NOTE_RECORD</a>&gt;&gt;{0:M}
0 &lt;&lt;<a href=Ged.REPOSITORY_RECORD>REPOSITORY_RECORD</a>&gt;&gt;{0:M}
0 &lt;&lt;<a href=Ged.SOURCE_RECORD>SOURCE_RECORD</a>&gt;&gt;{0:M}
<b>0 TRLR{1:1}</b>
</pre>
# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
0 | HEADER_RECORD | | |
0 | SUBMISSION_RECORD | | |
0 | SUBMITTER_RECORD | | |
0 | INDIVIDUAL_RECORD | | |
0 | FAM_RECORD | | |
0 | MULTIMEDIA_RECORD | | |
0 | NOTE_RECORD | | |
0 | REPOSITORY_RECORD | | |
0 | SOURCE_RECORD | | |

:warning: to be continued/checked


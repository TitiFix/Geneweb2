﻿# SPOUSE_TO_FAMILY_LINK
## Abstract
Primitive Elements of the Lineage-Linked Form
The field sizes show the minimum recommended field length within a database that is constrained to fixed
length fields. The field sizes are in addition to the GEDCOM level and tag overhead. GEDCOM lines are
limited to 255 characters. However, the CONCatenation or CONTinuation tags can be used to expand a
field beyond this limit. CONT line implies that a new line should appear to preserve formatting.  CONC
implies concatenation to the previous line without a new line.  This is used so that a text note or
description can be processed (word wrapped) in a text window without fixed carriage returns.  The
CONT and CONC tags are being used to extend specified textual values.


## GEDCOM syntax and proprietary extensions

**SPOUSE_TO_FAMILY_LINK**:=
<pre>
<b>n FAMS @&lt;<a href=Ged.XREF_FAM.md>XREF:FAM</a>&gt;@{1:1}</b>
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
</pre>
Used in <a href=Ged.INDIVIDUAL_RECORD.md>INDIVIDUAL_RECORD</a><br />


## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#fams>FAMS</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF{1:22}@ | | |
+1 <a href=Ged.GLOSSARY.md#note>NOTE</a> | char{1:248}\|NULL | | |
+2 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | | |

:warning: to be continued/checked

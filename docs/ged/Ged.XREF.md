﻿<!-- licence GPL V2, cf https://github.com/TitiFix/geneweb -->
# XREF
## Abstract
Either a pointer or an unique cross-reference identifier. If this element appears before the tag in a
GEDCOM line, then it is a cross-reference identifier. If it appears after the tag in a GEDCOM line,
then it is a pointer. The method of delimiting a pointer or cross-reference identifier is to enclose the
pointer or cross-reference identifier within at signs (@), for example, @I123@. A XREF may not
begin with a number sign (#). This is to avoid confusion with an escape sequence prefix (@#). The use
of a colon (:) in the XREF is reserved for creating future network cross-references and the use of an
exclamation (!) is reserved for intra-record pointers. Uniqueness of the cross-reference identifier is
required within the file.


## GEDCOM syntax and proprietary extensions

**XREF**:={Size=1:22}
<pre>
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />
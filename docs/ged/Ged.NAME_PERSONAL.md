﻿# NAME_PERSONAL
## Abstract
The surname of an individual, if known, is enclosed between two slash (/) characters. The order of the
n ame parts should be the order that the person would, by custom of their culture, have used when ®
giving it to a recorder. Early versions of Personal Ancestral File  and other products did not use the
trailing slash when the surname was the last element of the name.


## GEDCOM syntax and proprietary extensions

**NAME_PERSONAL**:={Size=1:120}
<pre>
[ &lt;<a href=Ged.NAME_TEXT.md>NAME_TEXT</a>&gt;
| /&lt;<a href=Ged.NAME_TEXT.md>NAME_TEXT</a>&gt;/
| &lt;<a href=Ged.NAME_TEXT.md>NAME_TEXT</a>&gt; /&lt;<a href=Ged.NAME_TEXT.md>NAME_TEXT</a>&gt;/
| /&lt;<a href=Ged.NAME_TEXT.md>NAME_TEXT</a>&gt;/ &lt;<a href=Ged.NAME_TEXT.md>NAME_TEXT</a>&gt;
| &lt;<a href=Ged.NAME_TEXT.md>NAME_TEXT</a>&gt; /&lt;<a href=Ged.NAME_TEXT.md>NAME_TEXT</a>&gt;/ &lt;<a href=Ged.NAME_TEXT.md>NAME_TEXT</a>&gt; ]
</pre>
Used in <a href=Ged.PERSONAL_NAME_STRUCTURE.md>PERSONAL_NAME_STRUCTURE</a><br />


NOTE:
- If part of name is illegible, that part is indicated by an ellipsis (...).
- Capitalize the name of a person or place in the conventional manner—capitalize the first letter of each part and lowercase the other letters, unless conventional usage is otherwise. For example: McMurray.
Examples:
William Lee (given name only or surname not known)
/Parry/ (surname only)
William Lee /Parry/
William Lee /Mac Parry/ (both parts (Mac and Parry) are surname parts
William /Lee/ Parry (surname imbedded in the name string)
William Lee /Pa.../

## Geneweb behavior



:warning: to be continued/checked

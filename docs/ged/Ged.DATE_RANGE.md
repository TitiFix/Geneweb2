﻿# DATE_RANGE
## Abstract

## GEDCOM syntax and proprietary extensions

**DATE_RANGE**:={Size=8:35}
<pre>
[ BEF &lt;<a href=Ged.DATE.md>DATE</a>&gt; | AFT &lt;<a href=Ged.DATE.md>DATE</a>&gt; | BET &lt;<a href=Ged.DATE.md>DATE</a>&gt; AND &lt;<a href=Ged.DATE.md>DATE</a>&gt; ]
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />
Where:
AFT=Event happened after the given date.
BEF=Event happened before the given date.
BET=Event happened some time between date 1 AND date 2. For example, bet 1904 and 1915
indicates that the event state (perhaps a single day) existed somewhere between 1904 and
1915 inclusive.
NOTE: The date range differs from the date period in that the date range is an estimate that an event happened
on a single date somewhere in the date range specified.
The following are equivalent and interchangeable:
Short formLong Form
1852BET 1 JAN 1852 AND 31 DEC 1852
1852BET 1 JAN 1852 AND DEC 1852
1852BET JAN 1852 AND 31 DEC 1852
1852BET JAN 1852 AND DEC 1852
JAN 1920BET 1 JAN 1920 AND 31 JAN 1920

## Geneweb behavior



:warning: to be continued/checked

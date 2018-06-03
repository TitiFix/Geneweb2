<!-- licence GPL V2, cf https://github.com/TitiFix/geneweb -->
# DATE_PERIOD
## Abstract

## GEDCOM syntax and proprietary extensions

**DATE_PERIOD**:={Size=7:35}
<pre>
[FROM &lt;<a href=Ged.DATE.md>DATE</a>&gt; | TO &lt;<a href=Ged.DATE.md>DATE</a>&gt; | FROM &lt;<a href=Ged.DATE.md>DATE</a>&gt; TO &lt;<a href=Ged.DATE.md>DATE</a>&gt; ]
</pre>
Used in <a href=Ged.SOURCE_RECORD.md>SOURCE_RECORD</a><br />


Where:
- FROM=Indicates the beginning of a happening or state.
- TO=Indicates the ending of a happening or state.
Examples:
FROM 1904 to 1915
=The state of some attribute existed from 1904 to 1915 inclusive.
FROM 1904
=The state of the attribute began in 1904 but the end date is unknown.
TO 1915
=The state ended in 1915 but the begin date is unknown.

## Geneweb behavior



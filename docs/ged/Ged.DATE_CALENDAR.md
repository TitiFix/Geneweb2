<!-- licence GPL V2, cf https://github.com/TitiFix/geneweb -->
# DATE_CALENDAR
## Abstract
The selection is based on the &lt;<a href=Ged.DATE_CALENDAR_ESCAPE.md>DATE_CALENDAR_ESCAPE</a>&gt; that precedes the &lt;<a href=Ged.DATE_CALENDAR.md>DATE_CALENDAR</a>&gt; value immediately to the left.  If &lt;<a href=Ged.DATE_CALENDAR_ESCAPE.md>DATE_CALENDAR_ESCAPE</a>&gt; doesn't appear at this point, then @#DGREGORIAN@ is assumed.  No future calendar types will use words (e.g., month names) from this list: FROM, TO, BEF, AFT, BET, AND, ABT, EST, CAL, or INT.


## GEDCOM syntax and proprietary extensions

**DATE_CALENDAR**:={Size=4:35}
<pre>
[ &lt;<a href=Ged.DATE_GREG.md>DATE_GREG</a>&gt; | &lt;<a href=Ged.DATE_JULN.md>DATE_JULN</a>&gt; | &lt;<a href=Ged.DATE_HEBR.md>DATE_HEBR</a>&gt; | &lt;<a href=Ged.DATE_FREN.md>DATE_FREN</a>&gt; | &lt;<a href=Ged.DATE_FUTURE.md>DATE_FUTURE</a>&gt; ]
</pre>
Used in <a href=Ged.DATE.md>DATE</a><br />


NOTE: When only a day and month appears as a DATE value it is considered a date phrase and not a valid date form.
Date EscapeSyntax Selected
@#DGREGORIAN@&lt;<a href=Ged.DATE_GREG.md>DATE_GREG</a>&gt;
@#DJULIAN@&lt;<a href=Ged.DATE_JULN.md>DATE_JULN</a>&gt;
@#DHEBREW@&lt;<a href=Ged.DATE_HEBR.md>DATE_HEBR</a>&gt;
@#DFRENCH R@&lt;<a href=Ged.DATE_FREN.md>DATE_FREN</a>&gt;
@#DROMAN@for future definition
@#DUNKNOWN@ calendar not known

## Geneweb behavior



🚧 to be continued/checked


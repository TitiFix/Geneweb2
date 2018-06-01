# DATE_VALUE
## Abstract
The DATE_VALUE represents the date of an activity, attribute, or event where:
INT=Interpreted from knowledge about the associated date phrase included in parentheses.
An acceptable alternative to the date phrase choice is to use one of the other choices such as
&lt;<a href=Ged.DATE_APPROXIMATED.md>DATE_APPROXIMATED</a>&gt; choice as the DATE line value and then include the date phrase value
as a NOTE value subordinate to the DATE line tag.


## GEDCOM syntax and proprietary extensions

**DATE_VALUE**:={Size=1:35}
<pre>
[ &lt;<a href=Ged.DATE.md>DATE</a>&gt; | &lt;<a href=Ged.DATE_PERIOD.md>DATE_PERIOD</a>&gt; | &lt;<a href=Ged.DATE_RANGE.md>DATE_RANGE</a>&gt;| &lt;<a href=Ged.DATE_APPROXIMATED.md>DATE_APPROXIMATED</a>&gt; | INT &lt;<a href=Ged.DATE.md>DATE</a>&gt; (&lt;<a href=Ged.DATE_PHRASE.md>DATE_PHRASE</a>&gt;) | (&lt;<a href=Ged.DATE_PHRASE.md>DATE_PHRASE</a>&gt;) ]
</pre>
Used in <a href=Ged.FAMILY_EVENT_DETAIL.md>FAMILY_EVENT_DETAIL</a>, <a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>, <a href=Ged.DATE_LDS_ORD.md>DATE_LDS_ORD</a>, <a href=Ged.ENTRY_RECORDING_DATE.md>ENTRY_RECORDING_DATE</a><br />


NOTE: The date value can take on the date form of just a date, an approximated date, between a date and
another date, and from one date to another date.  The preferred form of showing date imprecision, is
to show, for example, MAY 1890 rather than ABT 12 MAY 1890.  This is because limits have not
been assigned to the precision of the prefixes such as ABT or EST.

## Geneweb behavior



🚧 to be continued/checked


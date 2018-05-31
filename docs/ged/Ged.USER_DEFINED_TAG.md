# USER_DEFINED_TAG
## Abstract
A user-defined tag that is contained in the GEDCOM current transmission. This tag must begin with an underscore (_) and should only be interpreted in the context of the sending system.


## GEDCOM syntax and proprietary extensions

**USER_DEFINED_TAG**:={Size=1:15}
<pre>
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />
NOTE:
- Using a NOTE field is a more universal way of transmitting genealogical data that does not fit into the standard
GEDCOM structure.
- Systems that read user-defined tags must consider that they have meaning only with respect to a system contained in the &lt;<a href=Ged.HEADER_RECORD.md>HEADER_RECORD</a>&gt;> context (i.e &lt;<a href=Ged.SYSTEM_ID.md>SYSTEM_ID</a>&gt;).
- Otherwise Escape Sequence Format for the Lineage-Linked Form can be used
Very few Lineage-Linked GEDCOM compatible systems uses the escape sequence feature provided in the GEDCOM grammar.

## Geneweb behavior



:warning: to be continued/checked


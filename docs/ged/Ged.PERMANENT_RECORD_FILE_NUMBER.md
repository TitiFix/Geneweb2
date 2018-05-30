# PERMANENT_RECORD_FILE_NUMBER
## Abstract
The record number that uniquely identifies this record within a registered network resource. The
n umber will be usable as a cross-reference pointer. The use of the colon (:) is reserved to indicate the
separation of the "registered resource identifier" (which precedes the colon) and the unique "record
identifier" within that resource (which follows the colon). If the colon is used, implementations that
check pointers should not expect to find a matching cross-reference identifier in the transmission but
would find it in the indicated database within a network. Making resource files available to a public
n etwork is a future implementation.


## GEDCOM syntax and proprietary extensions
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**PERMANENT_RECORD_FILE_NUMBER**:={Size=1:90}
<pre>
&lt;<a href=Ged.REGISTERED_RESOURCE_IDENTIFIER.md>REGISTERED_RESOURCE_IDENTIFIER</a>&gt;:&lt;<a href=Ged.RECORD_IDENTIFIER.md>RECORD_IDENTIFIER</a>&gt;
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />## Geneweb behavior


:warning: to be continued/checked


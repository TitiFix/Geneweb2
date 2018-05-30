# INDIVIDUAL_EVENT_STRUCTURE
## Abstract
As a general rule, events are things that happen on a specific date. Use the date form ‘BET date
AND date’ to indicate that an event took place at some time between two dates. Resist the
temptation to use a ‘FROM date TO date’ form in an event structure.  If the subject of your
recording occurred over a period of time, then it is probably not an event, but rather an attribute or
fact.
The EVEN tag in this structure is for recording general events that are not shown in the above
<&lt;<a href=Ged.INDIVIDUAL_EVENT_STRUCTURE.md>INDIVIDUAL_EVENT_STRUCTURE</a>&gt;>.  The event indicated by this general EVEN tag is
defined by the value of the subordinate TYPE tag. For example, a person that signed a lease for land
dated  October 2, 1837 and a lease for equipment dated November 4, 1837 would be written in
GEDCOM as::
1 EVEN
2 TYPE Land Lease
2 DATE 2 OCT 1837
1 EVEN
2 TYPE Equipment Lease
2 DATE 4 NOV 1837
The TYPE tag can be optionally used to modify the basic understanding of its superior event or
attribute.  For example:
1 GRAD
2 TYPE College
The occurrence of an event is asserted by the presence of either a DATE tag and value or a PLACe
tag and value in the event structure. When neither the date value nor the place value are known then
a Y(es) value on the parent event tag line is required to assert that the event happened.  For example
each of the following GEDCOM structures assert that a death happened:
1 DEAT Y
1 DEAT
2 DATE 2 OCT 1937
1 DEAT
2 PLAC Cove, Cache, Utah
Using this convention, as opposed to the just the presence of the tag, protects GEDCOM processors
which removes (prunes) lines which have neither a value nor any subordinate line.  It also allows a
n ote or source to be attached to an event context without implying that the event occurred.
It is not proper GEDCOM form to use a N(o) value with an event tag to infer that it did not happen.
A convention to handle events which never happened may be defined in the future.


## GEDCOM syntax and proprietary extensions
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**INDIVIDUAL_EVENT_STRUCTURE**:=
<pre>
[
<b>n [ BIRT | CHR ] [Y|&lt;<a href=Ged.NULL.md>NULL</a>&gt;]{1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
  +1 FAMC @&lt;<a href=Ged.XREF_FAM.md>XREF:FAM</a>&gt;@{0:1}
|
<b>n DEAT  [Y|&lt;<a href=Ged.NULL.md>NULL</a>&gt;] {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n [ BURI | CREM ] {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n ADOP{1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
  +1 FAMC @&lt;<a href=Ged.XREF_FAM.md>XREF:FAM</a>&gt;@{0:1}
    +2 ADOP &lt;<a href=Ged.ADOPTED_BY_WHICH_PARENT.md>ADOPTED_BY_WHICH_PARENT</a>&gt;{0:1}
|
n [ BAPM | BARM | BASM | BLES ]{0:1}
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
n [ CHRA | CONF | FCOM | ORDN ]{0:1}
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n [ NATU | EMIG | IMMI ]{1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n [ CENS | PROB | WILL]{1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n [ GRAD | RETI ] {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt; {0:1} *
|
n EVEN [&lt;<a href=Ged.EVENT_DESCRIPTOR.md>EVENT_DESCRIPTOR</a>&gt; | &lt;<a href=Ged.NULL.md>NULL</a>&gt;] {0:1}
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt; {0:1} *
]
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0  | BIRT | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |
+1 <a href=Ged.GLOSSARY.md#FAMC>FAMC</a> | @XREF:FAM@ | | |
+0 <a href=Ged.GLOSSARY.md#DEAT>DEAT</a> | [Y|NULL] | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |
+0  | BURI | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |
+0 <a href=Ged.GLOSSARY.md#ADOP>ADOP</a> |  | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |
+1 <a href=Ged.GLOSSARY.md#FAMC>FAMC</a> | @XREF:FAM@ | | |
+2 <a href=Ged.GLOSSARY.md#ADOP>ADOP</a> | ADOPTED_BY_WHICH_PARENT | | |
+0  | BAPM | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |
+0  | CHRA | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |
+0  | NATU | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |
+0  | CENS | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |
+0  | GRAD | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |
+0 <a href=Ged.GLOSSARY.md#EVEN>EVEN</a> | [EVENT_DESCRIPTOR | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |

:warning: to be continued/checked


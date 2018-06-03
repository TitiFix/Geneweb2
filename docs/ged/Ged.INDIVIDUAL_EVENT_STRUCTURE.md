<!-- licence GPL V2, cf https://github.com/TitiFix/geneweb -->
# INDIVIDUAL_EVENT_STRUCTURE
## Abstract
As a general rule, events are things that happen on a specific date. Use the date form ‘BET date
AND date’ to indicate that an event took place at some time between two dates. Resist the
temptation to use a ‘FROM date TO date’ form in an event structure.  If the subject of your
recording occurred over a period of time, then it is probably not an event, but rather an attribute or fact.
The EVEN tag in this structure is for recording general events that are not shown in the above
&lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_STRUCTURE.md>INDIVIDUAL_EVENT_STRUCTURE</a>&gt;&gt;.  The event indicated by this general EVEN tag is
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


## GEDCOM syntax and proprietary extensions

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
Used in <a href=Ged.INDIVIDUAL_RECORD.md>INDIVIDUAL_RECORD</a><br />


NOTE:
Using this convention, as opposed to the just the presence of the tag, protects GEDCOM processors
which removes (prunes) lines which have neither a value nor any subordinate line.  It also allows a
n ote or source to be attached to an event context without implying that the event occurred.
It is not proper GEDCOM form to use a N(o) value with an event tag to infer that it did not happen.
A convention to handle events which never happened may be defined in the future.

## Geneweb behavior



level tag  | Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#birt>BIRT</a>\|<a href=Ged.GLOSSARY.md#chr>CHR</a> | [Y\|NULL] | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#famc>FAMC</a> | @XREF{1:22}@ | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#deat>DEAT</a> | [Y\|NULL] | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#buri>BURI</a>\|<a href=Ged.GLOSSARY.md#crem>CREM</a> |  | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#adop>ADOP</a> |  | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#famc>FAMC</a> | @XREF{1:22}@ | ? | ? | 
+2 <a href=Ged.GLOSSARY.md#adop>ADOP</a> |  HUSB \| WIFE \| BOTH  | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#bapm>BAPM</a>\|<a href=Ged.GLOSSARY.md#barm>BARM</a>\|<a href=Ged.GLOSSARY.md#basm>BASM</a>\|<a href=Ged.GLOSSARY.md#bles>BLES</a> |  | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#chra>CHRA</a>\|<a href=Ged.GLOSSARY.md#conf>CONF</a>\|<a href=Ged.GLOSSARY.md#fcom>FCOM</a>\|<a href=Ged.GLOSSARY.md#ordn>ORDN</a> |  | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#natu>NATU</a>\|<a href=Ged.GLOSSARY.md#emig>EMIG</a>\|<a href=Ged.GLOSSARY.md#immi>IMMI</a> |  | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#cens>CENS</a>\|<a href=Ged.GLOSSARY.md#prob>PROB</a>\|<a href=Ged.GLOSSARY.md#will>WILL</a> |  | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#grad>GRAD</a>\|<a href=Ged.GLOSSARY.md#reti>RETI</a> |  | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#even>EVEN</a> | char{1:90}\|NULL | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 

🚧 to be continued/checked


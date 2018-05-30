# FAMILY_EVENT_STRUCTURE
## Abstract


## GEDCOM syntax and proprietary extensions
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**FAMILY_EVENT_STRUCTURE**:=
<pre>
[
n [ ANUL | CENS | DIV | DIVF ] {0:1}
  +1 &lt;&lt;<a href=Ged.FAMILY_EVENT_DETAIL.md>FAMILY_EVENT_DETAIL</a>&gt;&gt;{0:1}
|
n [ ENGA | MARB | MARC ]{0:1}
  +1 &lt;&lt;<a href=Ged.FAMILY_EVENT_DETAIL.md>FAMILY_EVENT_DETAIL</a>&gt;&gt;{0:1}
|
<b>n MARR  [Y|&lt;<a href=Ged.NULL.md>NULL</a>&gt;]{1:1}</b>
  +1 &lt;&lt;<a href=Ged.FAMILY_EVENT_DETAIL.md>FAMILY_EVENT_DETAIL</a>&gt;&gt;{0:1}
|
<b>n [ MARL | MARS ]{1:1}</b>
  +1 &lt;&lt;<a href=Ged.FAMILY_EVENT_DETAIL.md>FAMILY_EVENT_DETAIL</a>&gt;&gt;{0:1}
|
n RESI {0:1}
  +1 &lt;&lt;<a href=Ged.FAMILY_EVENT_DETAIL.md>FAMILY_EVENT_DETAIL</a>&gt;&gt;{0:1}
|
n EVEN [&lt;<a href=Ged.EVENT_DESCRIPTOR.md>EVENT_DESCRIPTOR</a>&gt; | &lt;<a href=Ged.NULL.md>NULL</a>&gt;] {0:1}
  +1 &lt;&lt;<a href=Ged.FAMILY_EVENT_DETAIL.md>FAMILY_EVENT_DETAIL</a>&gt;&gt;{0:1}
]
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0  | ANUL | | |
+1  | FAMILY_EVENT_DETAIL | | |
+0  | ENGA | | |
+1  | FAMILY_EVENT_DETAIL | | |
+0 <a href=Ged.GLOSSARY.md#marr>MARR</a> | [Y|NULL] | | |
+1  | FAMILY_EVENT_DETAIL | | |
+0  | MARL | | |
+1  | FAMILY_EVENT_DETAIL | | |
+0 <a href=Ged.GLOSSARY.md#resi>RESI</a> |  | | |
+1  | FAMILY_EVENT_DETAIL | | |
+0 <a href=Ged.GLOSSARY.md#even>EVEN</a> | [EVENT_DESCRIPTOR | | |
+1  | FAMILY_EVENT_DETAIL | | |

:warning: to be continued/checked


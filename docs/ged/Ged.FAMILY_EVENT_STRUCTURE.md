<!-- licence GPL V2, cf https://github.com/TitiFix/geneweb -->
# FAMILY_EVENT_STRUCTURE
## Abstract

## GEDCOM syntax and proprietary extensions

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
Used in <a href=Ged.FAMILY_RECORD.md>FAMILY_RECORD</a><br />


## Geneweb behavior



level tag  | Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#anul>ANUL</a>\|<a href=Ged.GLOSSARY.md#cens>CENS</a>\|<a href=Ged.GLOSSARY.md#div>DIV</a>\|<a href=Ged.GLOSSARY.md#divf>DIVF</a> |  | ? | ? | 
+1  | &lt;<a href=Ged.FAMILY_EVENT_DETAIL.md>FAMILY_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#enga>ENGA</a>\|<a href=Ged.GLOSSARY.md#marb>MARB</a>\|<a href=Ged.GLOSSARY.md#marc>MARC</a> |  | ? | ? | 
+1  | &lt;<a href=Ged.FAMILY_EVENT_DETAIL.md>FAMILY_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#marr>MARR</a> | [Y\|NULL] | ? | ? | 
+1  | &lt;<a href=Ged.FAMILY_EVENT_DETAIL.md>FAMILY_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#marl>MARL</a>\|<a href=Ged.GLOSSARY.md#mars>MARS</a> |  | ? | ? | 
+1  | &lt;<a href=Ged.FAMILY_EVENT_DETAIL.md>FAMILY_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#resi>RESI</a> |  | ? | ? | 
+1  | &lt;<a href=Ged.FAMILY_EVENT_DETAIL.md>FAMILY_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#even>EVEN</a> | char{1:90}\|NULL | ? | ? | 
+1  | &lt;<a href=Ged.FAMILY_EVENT_DETAIL.md>FAMILY_EVENT_DETAIL</a>&gt; | ? | ? | 

🚧 to be continued/checked


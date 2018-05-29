# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**FAMILY_EVENT_STRUCTURE**:=
<pre>
[
<b>n [ ANUL | CENS | DIV | DIVF ] {1:1}</b>
  +1 &lt;&lt;<a href=Ged.FAMILY_EVENT_DETAIL>FAMILY_EVENT_DETAIL</a>&gt;&gt;{0:1}
|
<b>n [ ENGA | MARB | MARC ]{1:1}</b>
  +1 &lt;&lt;<a href=Ged.FAMILY_EVENT_DETAIL>FAMILY_EVENT_DETAIL</a>&gt;&gt;{0:1}
|
<b>n MARR  [Y|&lt;<a href=Ged.NULL>NULL</a>&gt;]{1:1}</b>
  +1 &lt;&lt;<a href=Ged.FAMILY_EVENT_DETAIL>FAMILY_EVENT_DETAIL</a>&gt;&gt;{0:1}
|
<b>n [ MARL | MARS ]{1:1}</b>
  +1 &lt;&lt;<a href=Ged.FAMILY_EVENT_DETAIL>FAMILY_EVENT_DETAIL</a>&gt;&gt;{0:1}
|
n RESI {0:1}
  +1 &lt;&lt;<a href=Ged.FAMILY_EVENT_DETAIL>FAMILY_EVENT_DETAIL</a>&gt;&gt;{0:1}
|
<b>n EVEN [&lt;<a href=Ged.EVENT_DESCRIPTOR>EVENT_DESCRIPTOR</a>&gt; | &lt;<a href=Ged.NULL>NULL</a>&gt;] {1:1}</b>
  +1 &lt;&lt;<a href=Ged.FAMILY_EVENT_DETAIL>FAMILY_EVENT_DETAIL</a>&gt;&gt;{0:1}
]
</pre>
Used in <a href=Ged.FAM_RECORD>FAM_RECORD</a><br />

# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+1 | FAMILY_EVENT_DETAIL | | |
+1 | FAMILY_EVENT_DETAIL | | |
n MARR |  | | |
+1 | FAMILY_EVENT_DETAIL | | |
+1 | FAMILY_EVENT_DETAIL | | |
+1 | FAMILY_EVENT_DETAIL | | |
nEVEN [ | EVENT_DESCRIPTOR | | |
nEVEN [<EVENT_DESCRIPTOR> | | | | |
+1 | FAMILY_EVENT_DETAIL | | |

:warning: to be continued/checked


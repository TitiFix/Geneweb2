# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**FAMILY_EVENT_DETAIL**:=
<pre>
n HUSB{0:1}
<b>  +1 AGE &lt;<a href=Ged.AGE_AT_EVENT>AGE_AT_EVENT</a>&gt;{1:1}</b>
n WIFE{0:1}
<b>  +1 AGE &lt;<a href=Ged.AGE_AT_EVENT>AGE_AT_EVENT</a>&gt;{1:1}</b>
n &lt;&lt;<a href=Ged.EVENT_DETAIL>EVENT_DETAIL</a>&gt;&gt;{0:1}
</pre>
Used in <a href=Ged.FAMILY_EVENT_STRUCTURE>FAMILY_EVENT_STRUCTURE</a><br />

# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+1AGE | AGE_AT_EVENT | | |
+1AGE | AGE_AT_EVENT | | |

:warning: to be continued/checked


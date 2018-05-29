# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**PLACE_STRUCTURE**:=
<pre>
<b>n PLAC &lt;<a href=Ged.PLACE_NAME>PLACE_NAME</a>&gt; {1:1}</b>
  +1 FORM &lt;<a href=Ged.PLACE_HIERARCHY>PLACE_HIERARCHY</a>&gt; {0:1}
  +1 FONE &lt;<a href=Ged.PLACE_PHONETIC_VARIATION>PLACE_PHONETIC_VARIATION</a>&gt;{0:M}
<b>    +2 TYPE &lt;<a href=Ged.PHONETIC_TYPE>PHONETIC_TYPE</a>&gt;{1:1}</b>
  +1 ROMN &lt;<a href=Ged.PLACE_ROMANIZED_VARIATION>PLACE_ROMANIZED_VARIATION</a>&gt;{0:M}
<b>    +2 TYPE &lt;<a href=Ged.ROMANIZED_TYPE>ROMANIZED_TYPE</a>&gt;{1:1}</b>
  +1 MAP{0:1}
<b>    +2 LATI &lt;<a href=Ged.PLACE_LATITUDE>PLACE_LATITUDE</a>&gt;{1:1}</b>
<b>    +2 LONG &lt;<a href=Ged.PLACE_LONGITUDE>PLACE_LONGITUDE</a>&gt;{1:1}</b>
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
</pre>
Used in <a href=Ged.EVENT_DETAIL>EVENT_DETAIL</a><br />

# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
nPLAC | PLACE_NAME | | |
+1 FORM | PLACE_HIERARCHY | | |
+1 FONE | PLACE_PHONETIC_VARIATION | | |
+2 TYPE | PHONETIC_TYPE | | |
+1 ROMN | PLACE_ROMANIZED_VARIATION | | |
+2 TYPE | ROMANIZED_TYPE | | |
+2 LATI | PLACE_LATITUDE | | |
+2 LONG | PLACE_LONGITUDE | | |
+1 | NOTE_STRUCTURE | | |

:warning: to be continued/checked


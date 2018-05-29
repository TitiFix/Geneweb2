# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**PERSONAL_NAME_STRUCTURE**:=
<pre>
<b>n NAME &lt;<a href=Ged.NAME_PERSONAL.md>NAME_PERSONAL</a>&gt; {1:1}</b>
  +1 TYPE &lt;<a href=Ged.NAME_TYPE.md>NAME_TYPE</a>&gt; {0:1}
  +1 &lt;&lt;<a href=Ged.PERSONAL_NAME_PIECES.md>PERSONAL_NAME_PIECES</a>&gt;&gt; {0:1}
  +1 FONE &lt;<a href=Ged.NAME_PHONETIC_VARIATION.md>NAME_PHONETIC_VARIATION</a>&gt; {0:M}
<b>    +2 TYPE &lt;<a href=Ged.PHONETIC_TYPE.md>PHONETIC_TYPE</a>&gt; {1:1}</b>
    +2 &lt;&lt;<a href=Ged.PERSONAL_NAME_PIECES.md>PERSONAL_NAME_PIECES</a>&gt;&gt; {0:1}
  +1 ROMN &lt;<a href=Ged.NAME_ROMANIZED_VARIATION.md>NAME_ROMANIZED_VARIATION</a>&gt; {0:M}
<b>    +2 TYPE &lt;<a href=Ged.ROMANIZED_TYPE.md>ROMANIZED_TYPE</a>&gt; {1:1}</b>
    +2 &lt;&lt;<a href=Ged.PERSONAL_NAME_PIECES.md>PERSONAL_NAME_PIECES</a>&gt;&gt; {0:1}
</pre>
Used in <a href=Ged.INDIVIDUAL_RECORD.md>INDIVIDUAL_RECORD</a><br />

# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
nNAME | NAME_PERSONAL | | |
+1 TYPE | NAME_TYPE | | |
+1 | PERSONAL_NAME_PIECES | | |
+1 FONE | NAME_PHONETIC_VARIATION | | |
+2 TYPE | PHONETIC_TYPE | | |
+2 | PERSONAL_NAME_PIECES | | |
+1 ROMN | NAME_ROMANIZED_VARIATION | | |
+2 TYPE | ROMANIZED_TYPE | | |
+2 | PERSONAL_NAME_PIECES | | |

:warning: to be continued/checked


# PERSONAL_NAME_STRUCTURE
## Abstract
The name value is formed in the manner the name is normally spoken, with the given name and family
n ame (surname) separated by slashes (/). (See &lt;<a href=Ged.NAME_PERSONAL.md>NAME_PERSONAL</a>&gt;) Based on the
dynamic nature or unknown compositions of naming conventions, it is difficult to provide more
detailed name piece structure to handle every case. The NPFX, GIVN, NICK, SPFX, SURN, and
NSFX tags are provided optionally for systems that cannot operate effectively with less structured
information.  For current future compatibility, all systems must construct their names based on the
&lt;<a href=Ged.NAME_PERSONAL.md>NAME_PERSONAL</a>&gt; structure. Those using the optional name pieces should assume that few
systems will process them, and most will not provide the name pieces.
A &lt;<a href=Ged.NAME_TYPE.md>NAME_TYPE</a>&gt; is used to specify the particular variation that this name is.  For example; if the
n ame type is subordinate to the &lt;<a href=Ged.NAME_PERSONAL.md>NAME_PERSONAL</a>&gt; it could indicate that this name is a name
taken at immigration or that it could be an ‘also known as’ name
Future GEDCOM releases (6.0 or later) will likely apply a very different strategy to resolve this
problem, possibly using a sophisticated parser and a name-knowledge database.


## GEDCOM syntax and proprietary extensions
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
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#name>NAME</a> | NAME_PERSONAL | | |
+1 <a href=Ged.GLOSSARY.md#type>TYPE</a> | NAME_TYPE | | |
+1  | PERSONAL_NAME_PIECES | | |
+1 <a href=Ged.GLOSSARY.md#fone>FONE</a> | NAME_PHONETIC_VARIATION | | |
+2 <a href=Ged.GLOSSARY.md#type>TYPE</a> | PHONETIC_TYPE | | |
+2  | PERSONAL_NAME_PIECES | | |
+1 <a href=Ged.GLOSSARY.md#romn>ROMN</a> | NAME_ROMANIZED_VARIATION | | |
+2 <a href=Ged.GLOSSARY.md#type>TYPE</a> | ROMANIZED_TYPE | | |
+2  | PERSONAL_NAME_PIECES | | |

:warning: to be continued/checked


# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**NAME_PERSONAL**:={Size=1:120}
<pre>
[ &lt;<a href=Ged.NAME_TEXT.md>NAME_TEXT</a>&gt;
| /&lt;<a href=Ged.NAME_TEXT.md>NAME_TEXT</a>&gt;/
| &lt;<a href=Ged.NAME_TEXT.md>NAME_TEXT</a>&gt; /&lt;<a href=Ged.NAME_TEXT.md>NAME_TEXT</a>&gt;/
| /&lt;<a href=Ged.NAME_TEXT.md>NAME_TEXT</a>&gt;/ &lt;<a href=Ged.NAME_TEXT.md>NAME_TEXT</a>&gt;
| &lt;<a href=Ged.NAME_TEXT.md>NAME_TEXT</a>&gt; /&lt;<a href=Ged.NAME_TEXT.md>NAME_TEXT</a>&gt;/ &lt;<a href=Ged.NAME_TEXT.md>NAME_TEXT</a>&gt; ]
</pre>
Used in <a href=Ged.PERSONAL_NAME_STRUCTURE.md>PERSONAL_NAME_STRUCTURE</a><br />

# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
[ | NAME_TEXT | | |
| / | NAME_TEXT | | |
| | NAME_TEXT | | |
| <NAME_TEXT> | / | | |
| / | NAME_TEXT | | |
| /<NAME_TEXT>/ | NAME_TEXT | | |
| | NAME_TEXT | | |
| <NAME_TEXT> | / | | |
| <NAME_TEXT> | /<NAME_TEXT>/ | | |

:warning: to be continued/checked


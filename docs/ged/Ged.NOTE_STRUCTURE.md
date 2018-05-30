# NOTE_STRUCTURE
## Abstract


## GEDCOM syntax and proprietary extensions
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**NOTE_STRUCTURE**:=
<pre>
[
<b>n NOTE @&lt;<a href=Ged.XREF_NOTE.md>XREF:NOTE</a>&gt;@ {1:1}</b>
|
<b>n NOTE [&lt;<a href=Ged.SUBMITTER_TEXT.md>SUBMITTER_TEXT</a>&gt; | &lt;<a href=Ged.NULL.md>NULL</a>&gt;] {1:1}</b>
  +1 [CONC|CONT] &lt;<a href=Ged.SUBMITTER_TEXT.md>SUBMITTER_TEXT</a>&gt; {0:M}
]
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />
NOTE: There are special considerations required when using the CONC tag. The usage is to provide a
n ote string that can be concatenated together so that the display program can do its own word
wrapping according to its display window size. The requirement for usage is to either break the text
line in the middle of a word, or if at the end of a word, to add a space to the first of the next CONC
line. Otherwise most operating systems will strip off the trailing space and the space is lost in the
reconstitution of the note.
## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#note>NOTE</a> | @XREF:NOTE@ | | |
+0 <a href=Ged.GLOSSARY.md#note>NOTE</a> | [SUBMITTER_TEXT | | |
+1 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | SUBMITTER_TEXT | | |

:warning: to be continued/checked


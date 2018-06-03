<!-- licence GPL V2, cf https://github.com/TitiFix/geneweb -->
# PERSONAL_NAME_PIECES
## Abstract
Text which appears on a name line before the given and surname parts of a name.
i.e. (Lt. Cmndr.) Joseph /Allen/ jr.
In this example Lt. Cmndr. is considered as the name prefix portion.


## GEDCOM syntax and proprietary extensions

**PERSONAL_NAME_PIECES**:=
<pre>
n NPFX &lt;<a href=Ged.NAME_PIECE_PREFIX.md>NAME_PIECE_PREFIX</a>&gt; {0:1}
n GIVN &lt;<a href=Ged.NAME_PIECE_GIVEN.md>NAME_PIECE_GIVEN</a>&gt; {0:1}
n NICK &lt;<a href=Ged.NAME_PIECE_NICKNAME.md>NAME_PIECE_NICKNAME</a>&gt; {0:1}
n SPFX &lt;<a href=Ged.NAME_PIECE_SURNAME_PREFIX.md>NAME_PIECE_SURNAME_PREFIX</a>&gt; {0:1}
n SURN &lt;<a href=Ged.NAME_PIECE_SURNAME.md>NAME_PIECE_SURNAME</a>&gt; {0:1}
n NSFX &lt;<a href=Ged.NAME_PIECE_SUFFIX.md>NAME_PIECE_SUFFIX</a>&gt; {0:1}
n &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt; {0:M}
n &lt;&lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt;&gt; {0:M}
</pre>
Used in <a href=Ged.PERSONAL_NAME_STRUCTURE.md>PERSONAL_NAME_STRUCTURE</a><br />


## Geneweb behavior


🚧 UNDER CONSTRUCTION : to be continued/checked 🚧 



level tag  | Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#npfx>NPFX</a> | &lt;<a href=Ged.NAME_PIECE_PREFIX.md>NAME_PIECE_PREFIX</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#givn>GIVN</a> | &lt;<a href=Ged.NAME_PIECE_GIVEN.md>NAME_PIECE_GIVEN</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#nick>NICK</a> | &lt;<a href=Ged.NAME_PIECE_NICKNAME.md>NAME_PIECE_NICKNAME</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#spfx>SPFX</a> | &lt;<a href=Ged.NAME_PIECE_SURNAME_PREFIX.md>NAME_PIECE_SURNAME_PREFIX</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#surn>SURN</a> | &lt;<a href=Ged.NAME_PIECE_SURNAME.md>NAME_PIECE_SURNAME</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#nsfx>NSFX</a> | &lt;<a href=Ged.NAME_PIECE_SUFFIX.md>NAME_PIECE_SUFFIX</a>&gt; | ? | ? | 
+0  | &lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt; | ? | ? | 
+0  | &lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt; | ? | ? | 

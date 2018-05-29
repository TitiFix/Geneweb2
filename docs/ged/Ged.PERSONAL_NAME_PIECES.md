# Abstract


# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**PERSONAL_NAME_PIECES**:=
<pre>
n NPFX &lt;<a href=Ged.NAME_PIECE_PREFIX.md>NAME_PIECE_PREFIX</a>&gt; {0:1}
n GIVN &lt;<a href=Ged.NAME_PIECE_GIVEN.md>NAME_PIECE_GIVEN</a>&gt; {0:1}
n NICK &lt;<a href=Ged.NAME_PIECE_NICKNAME.md>NAME_PIECE_NICKNAME</a>&gt; {0:1}
n SPFX &lt;NAME_PIECE_SURNAME_PREFIX {0:1}
n SURN &lt;<a href=Ged.NAME_PIECE_SURNAME.md>NAME_PIECE_SURNAME</a>&gt; {0:1}
n NSFX &lt;<a href=Ged.NAME_PIECE_SUFFIX.md>NAME_PIECE_SUFFIX</a>&gt; {0:1}
n &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt; {0:M}
n &lt;&lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt;&gt; {0:M}
</pre>
Used in <a href=Ged.PERSONAL_NAME_STRUCTURE.md>PERSONAL_NAME_STRUCTURE</a><br />

# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 NPFX | NAME_PIECE_PREFIX | | |
+0 GIVN | NAME_PIECE_GIVEN | | |
+0 NICK | NAME_PIECE_NICKNAME | | |
+0 SPFX | NAME_PIECE_SURNAME_PREFIX {0:1}
n SURN <NAME_PIECE_SURNAME | | |
+0 NSFX | NAME_PIECE_SUFFIX | | |
+0  | NOTE_STRUCTURE | | |
+0  | SOURCE_CITATION | | |

:warning: to be continued/checked


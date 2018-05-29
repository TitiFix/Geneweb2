# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**SOURCE_REPOSITORY_CITATION**:=
<pre>
<b>n REPO [ @XREF:REPO@ | &lt;<a href=Ged.NULL>NULL</a>&gt;]{1:1}</b>
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 CALN &lt;<a href=Ged.SOURCE_CALL_NUMBER>SOURCE_CALL_NUMBER</a>&gt;{0:M}
    +2 MEDI &lt;<a href=Ged.SOURCE_MEDIA_TYPE>SOURCE_MEDIA_TYPE</a>&gt;{0:1}
</pre>
Used in <a href=Ged.SOURCE_RECORD>SOURCE_RECORD</a><br />

# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
nREPO [ | @XREF:REPO@ | | |
+1 | NOTE_STRUCTURE | | |
+1 CALN | SOURCE_CALL_NUMBER | | |
+2 MEDI | SOURCE_MEDIA_TYPE | | |

:warning: to be continued/checked


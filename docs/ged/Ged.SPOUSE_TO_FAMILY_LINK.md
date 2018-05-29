# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**SPOUSE_TO_FAMILY_LINK**:=
<pre>
<b>n FAMS @&lt;<a href=Ged.XREF_FAM>XREF:FAM</a>&gt;@{1:1}</b>
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
</pre>
Used in <a href=Ged.INDIVIDUAL_RECORD>INDIVIDUAL_RECORD</a><br />

# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
nFAMS @ | XREF:FAM | | |
+1 | NOTE_STRUCTURE | | |

:warning: to be continued/checked


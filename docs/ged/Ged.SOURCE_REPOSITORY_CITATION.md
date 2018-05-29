# Abstract
This structure is used within a source record to point to a name and address record of the holder of the
source document.  Formal and informal repository name and addresses are stored in the
REPOSITORY_RECORD.  Informal repositories include owner's of an unpublished work or of a rare
published source, or a keeper of personal collections. An example would be the owner of a family Bible
containing unpublished family genealogical entries. More formal repositories, such as the Family History
Library, should show a call number of the source at that repository. The call number of that source
should be recorded using a subordinate CALN tag.  Systems which do not use repository name and
address record, should describe where the information cited is stored in the <&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;>
of the REPOsitory source citation structure.


# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**SOURCE_REPOSITORY_CITATION**:=
<pre>
<b>n REPO [ @XREF:REPO@ | &lt;<a href=Ged.NULL.md>NULL</a>&gt;]{1:1}</b>
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
  +1 CALN &lt;<a href=Ged.SOURCE_CALL_NUMBER.md>SOURCE_CALL_NUMBER</a>&gt;{0:M}
    +2 MEDI &lt;<a href=Ged.SOURCE_MEDIA_TYPE.md>SOURCE_MEDIA_TYPE</a>&gt;{0:1}
</pre>
Used in <a href=Ged.SOURCE_RECORD.md>SOURCE_RECORD</a><br />

# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 REPO [ @XREF:REPO@ | | NULL | | |
+1  | NOTE_STRUCTURE | | |
+1 CALN | SOURCE_CALL_NUMBER | | |
+2 MEDI | SOURCE_MEDIA_TYPE | | |

:warning: to be continued/checked


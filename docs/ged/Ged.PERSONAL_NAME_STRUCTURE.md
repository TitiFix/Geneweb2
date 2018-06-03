<!-- licence GPL V2, cf https://github.com/TitiFix/geneweb -->
# PERSONAL_NAME_STRUCTURE
## Abstract
The name value is formed in the manner the name is normally spoken, with the given name and family
n ame (surname) separated by slashes (/). (See &lt;<a href=Ged.NAME_PERSONAL.md>NAME_PERSONAL</a>&gt;) Based on the
dynamic nature or unknown compositions of naming conventions, it is difficult to provide more
detailed name piece structure to handle every case. The NPFX, GIVN, NICK, SPFX, SURN, and
NSFX tags are provided optionally for systems that cannot operate effectively with less structured
information.


## GEDCOM syntax and proprietary extensions

**PERSONAL_NAME_STRUCTURE**:=
<pre>
<b>n NAME &lt;<a href=Ged.NAME_PERSONAL.md>NAME_PERSONAL</a>&gt; {1:1}</b>
  +1 TYPE &lt;<a href=Ged.NAME_TYPE.md>NAME_TYPE</a>&gt; {0:1} &#x25B6;
  +1 &lt;&lt;<a href=Ged.PERSONAL_NAME_PIECES.md>PERSONAL_NAME_PIECES</a>&gt;&gt; {0:1} (* 5.0 definition *)
  +1 FONE &lt;<a href=Ged.NAME_PHONETIC_VARIATION.md>NAME_PHONETIC_VARIATION</a>&gt; {0:M} &#x25B6;
<b>    +2 TYPE &lt;<a href=Ged.PHONETIC_TYPE.md>PHONETIC_TYPE</a>&gt; {1:1} &#x25B6;</b>
    +2 &lt;&lt;<a href=Ged.PERSONAL_NAME_PIECES.md>PERSONAL_NAME_PIECES</a>&gt;&gt; {0:1} &#x25B6;
  +1 ROMN &lt;<a href=Ged.NAME_ROMANIZED_VARIATION.md>NAME_ROMANIZED_VARIATION</a>&gt; {0:M} &#x25B6;
<b>    +2 TYPE &lt;<a href=Ged.ROMANIZED_TYPE.md>ROMANIZED_TYPE</a>&gt; {1:1} &#x25B6;</b>
    +2 &lt;&lt;<a href=Ged.PERSONAL_NAME_PIECES.md>PERSONAL_NAME_PIECES</a>&gt;&gt; {0:1} &#x25B6;
</pre>
Used in <a href=Ged.INDIVIDUAL_RECORD.md>INDIVIDUAL_RECORD</a><br />


NOTE:
- For current future compatibility, all systems must construct their names based on the &lt;<a href=Ged.NAME_PERSONAL.md>NAME_PERSONAL</a>&gt; structure. Those using the optional name pieces should assume that few systems will process them, and most will not provide the name pieces.
- A &lt;<a href=Ged.NAME_TYPE.md>NAME_TYPE</a>&gt; is used to specify the particular variation that this name is.  For example; if the name type is subordinate to the &lt;<a href=Ged.NAME_PERSONAL.md>NAME_PERSONAL</a>&gt; it could indicate that this name is a name taken at immigration or that it could be an ‘also known as’ name.
- The structure allows name pieces to be specifically identified as subordinate parts of the name line. Most products will not use subordinate name pieces. A nickname can  be included on the name line by enclosing it in double quotation marks (changed in 5.5.)
- Systems using the subordinate name parts must still provide the name structure formed in the same way specified for &lt;<a href=Ged.NAME_PERSONAL.md>NAME_PERSONAL</a>&gt;.

## Geneweb behavior



level tag  | Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#name>NAME</a> | &lt;<a href=Ged.NAME_PERSONAL.md>NAME_PERSONAL</a>&gt; | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#type>TYPE</a> |  aka \| birth \| immigrant \| maiden \| married \| user_defined  | ? | ? | 
+1  | &lt;<a href=Ged.PERSONAL_NAME_PIECES.md>PERSONAL_NAME_PIECES</a>&gt; | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#fone>FONE</a> | char{1:120} | ? | ? | 
+2 <a href=Ged.GLOSSARY.md#type>TYPE</a> |  user_defined \| hangul \| kana | ? | ? | 
+2  | &lt;<a href=Ged.PERSONAL_NAME_PIECES.md>PERSONAL_NAME_PIECES</a>&gt; | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#romn>ROMN</a> | char{1:120} | ? | ? | 
+2 <a href=Ged.GLOSSARY.md#type>TYPE</a> | &lt;<a href=Ged.ROMANIZED_TYPE.md>ROMANIZED_TYPE</a>&gt; | ? | ? | 
+2  | &lt;<a href=Ged.PERSONAL_NAME_PIECES.md>PERSONAL_NAME_PIECES</a>&gt; | ? | ? | 

🚧 to be continued/checked


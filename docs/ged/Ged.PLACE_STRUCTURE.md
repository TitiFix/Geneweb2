# PLACE_STRUCTURE
## Abstract
The jurisdictional name of the place where the event took place.
in 5.5.1, the &lt;&lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt;&gt;


## GEDCOM syntax and proprietary extensions

**PLACE_STRUCTURE**:=
<pre>
<b>n PLAC &lt;<a href=Ged.PLACE_NAME.md>PLACE_NAME</a>&gt; {1:1}</b>
  +1 FORM &lt;<a href=Ged.PLACE_HIERARCHY.md>PLACE_HIERARCHY</a>&gt; {0:1}
  +1 FONE &lt;<a href=Ged.PLACE_PHONETIC_VARIATION.md>PLACE_PHONETIC_VARIATION</a>&gt;{0:M} &#x25B6;
<b>    +2 TYPE &lt;<a href=Ged.PHONETIC_TYPE.md>PHONETIC_TYPE</a>&gt;{1:1} &#x25B6;</b>
  +1 ROMN &lt;<a href=Ged.PLACE_ROMANIZED_VARIATION.md>PLACE_ROMANIZED_VARIATION</a>&gt;{0:M} &#x25B6;
<b>    +2 TYPE &lt;<a href=Ged.ROMANIZED_TYPE.md>ROMANIZED_TYPE</a>&gt;{1:1} &#x25B6;</b>
  +1 MAP{0:1} &#x25B6;
<b>    +2 LATI &lt;<a href=Ged.PLACE_LATITUDE.md>PLACE_LATITUDE</a>&gt;{1:1} &#x25B6;</b>
<b>    +2 LONG &lt;<a href=Ged.PLACE_LONGITUDE.md>PLACE_LONGITUDE</a>&gt;{1:1} &#x25B6;</b>
  +1 &lt;&lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt;&gt; (* &#x25B6; remove in 5.5.1, don't use &#x1F6AB; *)
  +1 &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
</pre>
Used in <a href=Ged.EVENT_DETAIL.md>EVENT_DETAIL</a><br />


## Geneweb behavior

level tag  | Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#plac>PLAC</a> | &lt;<a href=Ged.PLACE_NAME.md>PLACE_NAME</a>&gt; | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#form>FORM</a> | char{1:120} | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#fone>FONE</a> | char{1:120} | ? | ? | 
+2 <a href=Ged.GLOSSARY.md#type>TYPE</a> |  user_defined \| hangul \| kana | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#romn>ROMN</a> | char{1:120} | ? | ? | 
+2 <a href=Ged.GLOSSARY.md#type>TYPE</a> | &lt;<a href=Ged.ROMANIZED_TYPE.md>ROMANIZED_TYPE</a>&gt; | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#map>MAP</a> |  | ? | ? | 
+2 <a href=Ged.GLOSSARY.md#lati>LATI</a> | char{5:8} | ? | ? | 
+2 <a href=Ged.GLOSSARY.md#long>LONG</a> | char{5:8} | ? | ? | 
+1  | &lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt; | ? | ? | 
+1  | &lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt; | ? | ? | 

🚧 to be continued/checked


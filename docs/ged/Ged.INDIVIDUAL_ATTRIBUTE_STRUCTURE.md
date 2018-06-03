<!-- licence GPL V2, cf https://github.com/TitiFix/geneweb -->
# INDIVIDUAL_ATTRIBUTE_STRUCTURE
## Abstract
The name of an individual's rank or status in society which is sometimes based on racial or religious differences, or differences in wealth, inherited  rank, profession, occupation, etc.


## GEDCOM syntax and proprietary extensions

**INDIVIDUAL_ATTRIBUTE_STRUCTURE**:=
<pre>
[
<b>n CAST &lt;<a href=Ged.CASTE_NAME.md>CASTE_NAME</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n DSCR &lt;<a href=Ged.PHYSICAL_DESCRIPTION.md>PHYSICAL_DESCRIPTION</a>&gt; {1:1}</b>
  +1 [CONC | CONT ] &lt;<a href=Ged.PHYSICAL_DESCRIPTION.md>PHYSICAL_DESCRIPTION</a>&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n EDUC &lt;<a href=Ged.SCHOLASTIC_ACHIEVEMENT.md>SCHOLASTIC_ACHIEVEMENT</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n IDNO &lt;<a href=Ged.NATIONAL_ID_NUMBER.md>NATIONAL_ID_NUMBER</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n NATI &lt;<a href=Ged.NATIONAL_OR_TRIBAL_ORIGIN.md>NATIONAL_OR_TRIBAL_ORIGIN</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n NCHI &lt;<a href=Ged.COUNT_OF_CHILDREN.md>COUNT_OF_CHILDREN</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n NMR &lt;<a href=Ged.COUNT_OF_MARRIAGES.md>COUNT_OF_MARRIAGES</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n OCCU &lt;<a href=Ged.OCCUPATION.md>OCCUPATION</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n PROP &lt;<a href=Ged.POSSESSIONS.md>POSSESSIONS</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n RELI &lt;<a href=Ged.RELIGIOUS_AFFILIATION.md>RELIGIOUS_AFFILIATION</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n RESI (* Resides at *){1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n SSN &lt;<a href=Ged.SOCIAL_SECURITY_NUMBER.md>SOCIAL_SECURITY_NUMBER</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n TITL &lt;<a href=Ged.NOBILITY_TYPE_TITLE.md>NOBILITY_TYPE_TITLE</a>&gt;{1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n FACT &lt;<a href=Ged.ATTRIBUTE_DESCRIPTOR.md>ATTRIBUTE_DESCRIPTOR</a>&gt;{1:1} &#x25B6;</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1}*  &#x25B6;
]
</pre>
Used in <a href=Ged.INDIVIDUAL_RECORD.md>INDIVIDUAL_RECORD</a><br />


NOTE: The usage of IDNO or the FACT tag require that a subordinate TYPE tag be used to define
what kind of identification number or fact classification is being defined.  The TYPE tag can be used
with each of the above tags used in this structure.

## Geneweb behavior


🚧 UNDER CONSTRUCTION : to be continued/checked 🚧 



level tag  | Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#cast>CAST</a> | char{1:90} | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#dscr>DSCR</a> | char{1:248} | ? | ? | 
+1 <a href=Ged.GLOSSARY.md#conc>CONC</a>\|<a href=Ged.GLOSSARY.md#cont>CONT</a> | char{1:248} | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#educ>EDUC</a> | char{1:248} | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#idno>IDNO</a> | char{1:30} | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#nati>NATI</a> | char{1:120} | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#nchi>NCHI</a> | char{1:3} | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#nmr>NMR</a> | char{1:3} | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#occu>OCCU</a> | char{1:90} | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#prop>PROP</a> | char{1:248} | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#reli>RELI</a> | char{1:90} | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#resi>RESI</a> | (* | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#ssn>SSN</a> | char{9:11} | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#titl>TITL</a> | char{1:120} | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 
+0 <a href=Ged.GLOSSARY.md#fact>FACT</a> | char{1:90} | ? | ? | 
+1  | &lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt; | ? | ? | 

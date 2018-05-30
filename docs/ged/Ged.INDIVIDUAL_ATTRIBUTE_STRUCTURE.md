# INDIVIDUAL_ATTRIBUTE_STRUCTURE
## Abstract


## GEDCOM syntax and proprietary extensions
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

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
<b>n FACT &lt;<a href=Ged.ATTRIBUTE_DESCRIPTOR.md>ATTRIBUTE_DESCRIPTOR</a>&gt;{1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
]
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />
NOTE: The usage of IDNO or the FACT tag require that a subordinate TYPE tag be used to define
what kind of identification number or fact classification is being defined.  The TYPE tag can be used
with each of the above tags used in this structure.
## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#CAST>CAST</a> | CASTE_NAME | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |
+0 <a href=Ged.GLOSSARY.md#DSCR>DSCR</a> | PHYSICAL_DESCRIPTION | | |
+1  | | | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |
+0 <a href=Ged.GLOSSARY.md#EDUC>EDUC</a> | SCHOLASTIC_ACHIEVEMENT | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |
+0 <a href=Ged.GLOSSARY.md#IDNO>IDNO</a> | NATIONAL_ID_NUMBER | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |
+0 <a href=Ged.GLOSSARY.md#NATI>NATI</a> | NATIONAL_OR_TRIBAL_ORIGIN | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |
+0 <a href=Ged.GLOSSARY.md#NCHI>NCHI</a> | COUNT_OF_CHILDREN | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |
+0 <a href=Ged.GLOSSARY.md#NMR>NMR</a> | COUNT_OF_MARRIAGES | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |
+0 <a href=Ged.GLOSSARY.md#OCCU>OCCU</a> | OCCUPATION | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |
+0 <a href=Ged.GLOSSARY.md#PROP>PROP</a> | POSSESSIONS | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |
+0 <a href=Ged.GLOSSARY.md#RELI>RELI</a> | RELIGIOUS_AFFILIATION | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |
+0 <a href=Ged.GLOSSARY.md#RESI>RESI</a> | (* | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |
+0 <a href=Ged.GLOSSARY.md#SSN>SSN</a> | SOCIAL_SECURITY_NUMBER | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |
+0 <a href=Ged.GLOSSARY.md#TITL>TITL</a> | NOBILITY_TYPE_TITLE | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |
+0 <a href=Ged.GLOSSARY.md#FACT>FACT</a> | ATTRIBUTE_DESCRIPTOR | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |

:warning: to be continued/checked


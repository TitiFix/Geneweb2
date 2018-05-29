# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**INDIVIDUAL_ATTRIBUTE_STRUCTURE**:=
<pre>
[
<b>n CAST &lt;<a href=Ged.CASTE_NAME>CASTE_NAME</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n DSCR &lt;<a href=Ged.PHYSICAL_DESCRIPTION>PHYSICAL_DESCRIPTION</a>&gt; {1:1}</b>
  +1 [CONC | CONT ] &lt;<a href=Ged.PHYSICAL_DESCRIPTION>PHYSICAL_DESCRIPTION</a>&gt;{0:M}
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n EDUC &lt;<a href=Ged.SCHOLASTIC_ACHIEVEMENT>SCHOLASTIC_ACHIEVEMENT</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n IDNO &lt;<a href=Ged.NATIONAL_ID_NUMBER>NATIONAL_ID_NUMBER</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n NATI &lt;<a href=Ged.NATIONAL_OR_TRIBAL_ORIGIN>NATIONAL_OR_TRIBAL_ORIGIN</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n NCHI &lt;<a href=Ged.COUNT_OF_CHILDREN>COUNT_OF_CHILDREN</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n NMR &lt;<a href=Ged.COUNT_OF_MARRIAGES>COUNT_OF_MARRIAGES</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n OCCU &lt;<a href=Ged.OCCUPATION>OCCUPATION</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n PROP &lt;<a href=Ged.POSSESSIONS>POSSESSIONS</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n RELI &lt;<a href=Ged.RELIGIOUS_AFFILIATION>RELIGIOUS_AFFILIATION</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n RESI /* Resides at */{1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n SSN &lt;<a href=Ged.SOCIAL_SECURITY_NUMBER>SOCIAL_SECURITY_NUMBER</a>&gt; {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n TITL &lt;<a href=Ged.NOBILITY_TYPE_TITLE>NOBILITY_TYPE_TITLE</a>&gt;{1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n FACT &lt;<a href=Ged.ATTRIBUTE_DESCRIPTOR>ATTRIBUTE_DESCRIPTOR</a>&gt;{1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
]
</pre>
Used in <a href=Ged.INDIVIDUAL_RECORD>INDIVIDUAL_RECORD</a><br />


* NOTE : The usage of IDNO or the FACT tag require that a subordinate TYPE tag be used to define
what kind of identification number or fact classification is being defined.  The TYPE tag can be used
with each of the above tags used in this structure.
# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
nCAST | CASTE_NAME | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |
nDSCR | PHYSICAL_DESCRIPTION | | |
+1 [CONC | | | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |
nEDUC | SCHOLASTIC_ACHIEVEMENT | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |
nIDNO | NATIONAL_ID_NUMBER | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |
nNATI | NATIONAL_OR_TRIBAL_ORIGIN | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |
nNCHI | COUNT_OF_CHILDREN | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |
nNMR | COUNT_OF_MARRIAGES | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |
nOCCU | OCCUPATION | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |
nPROP | POSSESSIONS | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |
nRELI | RELIGIOUS_AFFILIATION | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |
nSSN | SOCIAL_SECURITY_NUMBER | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |
nTITL | NOBILITY_TYPE_TITLE | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |
nFACT | ATTRIBUTE_DESCRIPTOR | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |

:warning: to be continued/checked


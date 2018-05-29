# Abstract


# GEDCOM Syntax (extension included)
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
<b>n RESI /* Resides at */{1:1}</b>
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
Used in <a href=Ged.INDIVIDUAL_RECORD.md>INDIVIDUAL_RECORD</a><br />


NOTE : The usage of IDNO or the FACT tag require that a subordinate TYPE tag be used to define
what kind of identification number or fact classification is being defined.  The TYPE tag can be used
with each of the above tags used in this structure.
# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 CAST | CASTE_NAME | | |
+1  | INDIVIDUAL_EVENT_DETAIL | | |
+0 DSCR | PHYSICAL_DESCRIPTION | | |
+0 EDUC | SCHOLASTIC_ACHIEVEMENT | | |
+0 IDNO | NATIONAL_ID_NUMBER | | |
+0 NATI | NATIONAL_OR_TRIBAL_ORIGIN | | |
+0 NCHI | COUNT_OF_CHILDREN | | |
+0 NMR | COUNT_OF_MARRIAGES | | |
+0 OCCU | OCCUPATION | | |
+0 PROP | POSSESSIONS | | |
+0 RELI | RELIGIOUS_AFFILIATION | | |
+0 SSN | SOCIAL_SECURITY_NUMBER | | |
+0 TITL | NOBILITY_TYPE_TITLE | | |
+0 FACT | ATTRIBUTE_DESCRIPTOR | | |

:warning: to be continued/checked


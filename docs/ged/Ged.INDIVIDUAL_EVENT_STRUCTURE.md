# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**INDIVIDUAL_EVENT_STRUCTURE**:=
<pre>
[
<b>n [ BIRT | CHR ] [Y|&lt;<a href=Ged.NULL.md>NULL</a>&gt;]{1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
  +1 FAMC @&lt;<a href=Ged.XREF_FAM.md>XREF:FAM</a>&gt;@{0:1}
|
<b>n DEAT  [Y|&lt;<a href=Ged.NULL.md>NULL</a>&gt;] {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n [ BURI | CREM ] {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n ADOP{1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
  +1 FAMC @&lt;<a href=Ged.XREF_FAM.md>XREF:FAM</a>&gt;@{0:1}
    +2 ADOP &lt;<a href=Ged.ADOPTED_BY_WHICH_PARENT.md>ADOPTED_BY_WHICH_PARENT</a>&gt;{0:1}
|
<b>n [ BAPM | BARM | BASM | BLES ]{1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n [ CHRA | CONF | FCOM | ORDN ]{1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n [ NATU | EMIG | IMMI ]{1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n [ CENS | PROB | WILL]{1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt;{0:1} *
|
<b>n [ GRAD | RETI ] {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt; {0:1} *
|
<b>n EVEN  {1:1}</b>
  +1 &lt;&lt;<a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a>&gt;&gt; {0:1} *
]
</pre>
Used in <a href=Ged.INDIVIDUAL_RECORD.md>INDIVIDUAL_RECORD</a><br />

# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
n[ BIRT | | | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |
+1 FAMC | @ | | |
nDEAT  | [Y| | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |
+1 FAMC | @ | | |
+2 ADOP | ADOPTED_BY_WHICH_PARENT | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |
+1 | INDIVIDUAL_EVENT_DETAIL | | |

:warning: to be continued/checked


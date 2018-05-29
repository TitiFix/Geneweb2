# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**ADDRESS_STRUCTURE**:=
<pre>
<b>n ADDR &lt;<a href=Ged.ADDRESS_LINE>ADDRESS_LINE</a>&gt;{1:1}</b>
  +1 CONT &lt;<a href=Ged.ADDRESS_LINE>ADDRESS_LINE</a>&gt;{0:3}
  +1 ADR1 &lt;<a href=Ged.ADDRESS_LINE1>ADDRESS_LINE1</a>&gt;{0:1}
  +1 ADR2 &lt;<a href=Ged.ADDRESS_LINE2>ADDRESS_LINE2</a>&gt;{0:1}
  +1 ADR3 &lt;<a href=Ged.ADDRESS_LINE3>ADDRESS_LINE3</a>&gt;{0:1}
  +1 CITY &lt;<a href=Ged.ADDRESS_CITY>ADDRESS_CITY</a>&gt;{0:1}
  +1 STAE &lt;<a href=Ged.ADDRESS_STATE>ADDRESS_STATE</a>&gt;{0:1}
  +1 POST &lt;<a href=Ged.ADDRESS_POSTAL_CODE>ADDRESS_POSTAL_CODE</a>&gt;{0:1}
  +1 CTRY &lt;<a href=Ged.ADDRESS_COUNTRY>ADDRESS_COUNTRY</a>&gt;{0:1}
n PHON &lt;<a href=Ged.PHONE_NUMBER>PHONE_NUMBER</a>&gt;{0:3}
n EMAIL &lt;<a href=Ged.ADDRESS_EMAIL>ADDRESS_EMAIL</a>&gt;{0:3}
n FAX&lt;<a href=Ged.ADDRESS_FAX>ADDRESS_FAX</a>&gt;{0:3}
n WWW &lt;<a href=Ged.ADDRESS_WEB_PAGE>ADDRESS_WEB_PAGE</a>&gt;{0:3}
</pre>
Used in <a href=Ged.HEADER_RECORD>HEADER_RECORD</a>, <a href=Ged.REPOSITORY_RECORD>REPOSITORY_RECORD</a>, <a href=Ged.SUBMITTER_RECORD>SUBMITTER_RECORD</a>, <a href=Ged.EVENT_DETAIL>EVENT_DETAIL</a><br />

# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
nADDR | ADDRESS_LINE | | |
+1 CONT | ADDRESS_LINE | | |
+1 ADR1 | ADDRESS_LINE1 | | |
+1 ADR2 | ADDRESS_LINE2 | | |
+1 ADR3 | ADDRESS_LINE3 | | |
+1 CITY | ADDRESS_CITY | | |
+1 STAE | ADDRESS_STATE | | |
+1 POST | ADDRESS_POSTAL_CODE | | |
+1 CTRY | ADDRESS_COUNTRY | | |
nPHON | PHONE_NUMBER | | |
nEMAIL | ADDRESS_EMAIL | | |
nFAX | ADDRESS_FAX | | |
nWWW | ADDRESS_WEB_PAGE | | |

:warning: to be continued/checked


# ADDRESS_STRUCTURE
## Abstract
The address structure should be formed as it would appear on a mailing label using the ADDR and
the CONT lines to form the address structure.  The ADDR and CONT lines are required for any
address. The additional subordinate address tags such as STAE and CTRY are provided to be used
by systems that have structured their addresses for indexing and sorting. For backward compatibility
these lines are not to be used in lieu of the required ADDR.and CONT line structure.


## GEDCOM syntax and proprietary extensions
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**ADDRESS_STRUCTURE**:=
<pre>
<b>n ADDR &lt;<a href=Ged.ADDRESS_LINE.md>ADDRESS_LINE</a>&gt;{1:1}</b>
  +1 CONT &lt;<a href=Ged.ADDRESS_LINE.md>ADDRESS_LINE</a>&gt;{0:3}
  +1 ADR1 &lt;<a href=Ged.ADDRESS_LINE1.md>ADDRESS_LINE1</a>&gt;{0:1}
  +1 ADR2 &lt;<a href=Ged.ADDRESS_LINE2.md>ADDRESS_LINE2</a>&gt;{0:1}
  +1 ADR3 &lt;<a href=Ged.ADDRESS_LINE3.md>ADDRESS_LINE3</a>&gt;{0:1}
  +1 CITY &lt;<a href=Ged.ADDRESS_CITY.md>ADDRESS_CITY</a>&gt;{0:1}
  +1 STAE &lt;<a href=Ged.ADDRESS_STATE.md>ADDRESS_STATE</a>&gt;{0:1}
  +1 POST &lt;<a href=Ged.ADDRESS_POSTAL_CODE.md>ADDRESS_POSTAL_CODE</a>&gt;{0:1}
  +1 CTRY &lt;<a href=Ged.ADDRESS_COUNTRY.md>ADDRESS_COUNTRY</a>&gt;{0:1}
n PHON &lt;<a href=Ged.PHONE_NUMBER.md>PHONE_NUMBER</a>&gt;{0:3}
n EMAIL &lt;<a href=Ged.ADDRESS_EMAIL.md>ADDRESS_EMAIL</a>&gt;{0:3}
n FAX&lt;<a href=Ged.ADDRESS_FAX.md>ADDRESS_FAX</a>&gt;{0:3}
n WWW &lt;<a href=Ged.ADDRESS_WEB_PAGE.md>ADDRESS_WEB_PAGE</a>&gt;{0:3}
</pre>
Used in <a href=Ged.LINEAGE_LINKED_STRUCTURE.md>LINEAGE_LINKED_STRUCTURE</a><br />## Geneweb behavior

level tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
+0 <a href=Ged.GLOSSARY.md#ADDR>ADDR</a> | ADDRESS_LINE | | |
+1 <a href=Ged.GLOSSARY.md#CONT>CONT</a> | ADDRESS_LINE | | |
+1 <a href=Ged.GLOSSARY.md#ADR1>ADR1</a> | ADDRESS_LINE1 | | |
+1 <a href=Ged.GLOSSARY.md#ADR2>ADR2</a> | ADDRESS_LINE2 | | |
+1 <a href=Ged.GLOSSARY.md#ADR3>ADR3</a> | ADDRESS_LINE3 | | |
+1 <a href=Ged.GLOSSARY.md#CITY>CITY</a> | ADDRESS_CITY | | |
+1 <a href=Ged.GLOSSARY.md#STAE>STAE</a> | ADDRESS_STATE | | |
+1 <a href=Ged.GLOSSARY.md#POST>POST</a> | ADDRESS_POSTAL_CODE | | |
+1 <a href=Ged.GLOSSARY.md#CTRY>CTRY</a> | ADDRESS_COUNTRY | | |
+0 <a href=Ged.GLOSSARY.md#PHON>PHON</a> | PHONE_NUMBER | | |
+0 <a href=Ged.GLOSSARY.md#EMAIL>EMAIL</a> | ADDRESS_EMAIL | | |
+0 <a href=Ged.GLOSSARY.md#FAX>FAX</a> | ADDRESS_FAX | | |
+0 <a href=Ged.GLOSSARY.md#WWW>WWW</a> | ADDRESS_WEB_PAGE | | |

:warning: to be continued/checked


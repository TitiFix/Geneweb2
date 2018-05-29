# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**DATE_EXACT**:=
<pre>
&lt;<a href=Ged.DAY>DAY</a>&gt; &lt;<a href=Ged.MONTH>MONTH</a>&gt; &lt;<a href=Ged.YEAR_GREG>YEAR_GREG</a>&gt;
</pre>
Used in <a href=Ged.CHANGE_DATE>CHANGE_DATE</a>, <a href=Ged.PUBLICATION_DATE>PUBLICATION_DATE</a>, <a href=Ged.TRANSMISSION_DATE>TRANSMISSION_DATE</a><br />

# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
<DAY> | MONTH | | |
<DAY> <MONTH> | YEAR_GREG | | |

:warning: to be continued/checked


# Abstract

# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**EVENT_DETAIL**:=
<pre>
n TYPE &lt;<a href=Ged.EVENT_OR_FACT_CLASSIFICATION.md>EVENT_OR_FACT_CLASSIFICATION</a>&gt;{0:1}
n DATE &lt;<a href=Ged.DATE_VALUE.md>DATE_VALUE</a>&gt;{0:1}
n &lt;&lt;<a href=Ged.PLACE_STRUCTURE.md>PLACE_STRUCTURE</a>&gt;&gt;{0:1}
n &lt;&lt;<a href=Ged.ADDRESS_STRUCTURE.md>ADDRESS_STRUCTURE</a>&gt;&gt;{0:1}
n AGNC &lt;<a href=Ged.RESPONSIBLE_AGENCY.md>RESPONSIBLE_AGENCY</a>&gt;{0:1}
n RELI &lt;<a href=Ged.RELIGIOUS_AFFILIATION.md>RELIGIOUS_AFFILIATION</a>&gt;{0:1}
n CAUS &lt;<a href=Ged.CAUSE_OF_EVENT.md>CAUSE_OF_EVENT</a>&gt;{0:1}
n RESN &lt;<a href=Ged.RESTRICTION_NOTICE.md>RESTRICTION_NOTICE</a>&gt;{0:1}
n &lt;&lt;<a href=Ged.NOTE_STRUCTURE.md>NOTE_STRUCTURE</a>&gt;&gt;{0:M}
n &lt;&lt;<a href=Ged.SOURCE_CITATION.md>SOURCE_CITATION</a>&gt;&gt;{0:M}
n &lt;&lt;<a href=Ged.MULTIMEDIA_LINK.md>MULTIMEDIA_LINK</a>&gt;&gt;{0:M}
</pre>
Used in <a href=Ged.FAMILY_EVENT_DETAIL.md>FAMILY_EVENT_DETAIL</a>, <a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a><br />

# Geneweb behavior

level+tag  | + Attribut type or value | Import behavior | Export behavior  | Comment 
---------- | ------------- | :---------------: | :-----------------:| -----------
nTYPE | EVENT_OR_FACT_CLASSIFICATION | | |
nDATE | DATE_VALUE | | |
nAGNC | RESPONSIBLE_AGENCY | | |
nRELI | RELIGIOUS_AFFILIATION | | |
nCAUS | CAUSE_OF_EVENT | | |
nRESN | RESTRICTION_NOTICE | | |

:warning: to be continued/checked


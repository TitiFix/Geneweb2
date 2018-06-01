# EVENT_OR_FACT_CLASSIFICATION
## Abstract
A descriptive word or phrase used to further classify the parent event or attribute tag. This should be
used whenever either of  the generic EVEN or FACT tags are used. The value of this primative is
responsible for classifying the generic event or fact being cited.


## GEDCOM syntax and proprietary extensions

**EVENT_OR_FACT_CLASSIFICATION**:={Size=1:90}
<pre>
</pre>
Used in <a href=Ged.FAMILY_EVENT_DETAIL.md>FAMILY_EVENT_DETAIL</a>, <a href=Ged.INDIVIDUAL_EVENT_DETAIL.md>INDIVIDUAL_EVENT_DETAIL</a><br />


NOTE: For example, if the attribute being
defined was one of the persons skills, such as woodworking, the FACT tag would have the value of
`Woodworking', followed by a subordinate TYPE tag with the value `Skills.'
1 FACT Woodworking
2 TYPE Skills
This groups the fact into a generic skills attribute, and in particular this entry records the fact that this
individual possessed the skill of woodworking. Using the subordinate TYPE tag classification method
with any of the other defined event tags provides a further classification of the parent tag but does not
change the basic meaning of the parent tag. For example, a MARR tag could be subordinated with a
TYPE tag with an EVENT_DESCRIPTOR value of `Common Law.'
1 MARR
2 TYPE Common Law
This classifies the entry as a common law marriage but the event is still a marriage event. Other
descriptor values might include, for example,`stillborn' as a qualifier to BIRTh or `Tribal Custom' as a
qualifier to MARRiage.

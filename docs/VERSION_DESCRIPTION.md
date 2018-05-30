# VERSION DESCRIPTION DOCUMENT
## Version Informations and Overview

### General informations : 
	GeneWeb Version 7.00.exp
	see https://github.com/geneweb/geneweb
	Licence GNU GENERAL PUBLIC LICENSE V2 - cf [LICENSE](../LICENSE) file 

	Current Fork/branch
		https://github.com/TitiFix/geneweb
		Fork TitiFix\GeneWeb
		Branch gedImprovements

### Overview :
These branch is temporary for GEDCOM import/export update/improvement.

The present documentation list GEDCOM issues from https://github.com/geneweb/geneweb/issues (in relation with the GEDCOM import / export from Geneweb)

## Documentation
The official documentation : http://geneweb.tuxfamily.org/

Additional documentation for import / export GEDCOM :
* Current [WIKI](../../../wiki)
* Gedcom [LINEAGE LINKED FORM](ged/Ged.LINEAGE_LINKED_STRUCTURE.md) (5.5, 5.5.1 and commons usages mixed) and Geneweb behavior (It is not a full gedcom documentation or reference/official documentation )

GEDCOM reference documentation : https://www.familysearch.org/developers/docs/gedcom/
(GEDCOM is no longer maintained by Family Search. 
The GEDCOM specifications 5.5 and draft 5.5.1 are provided only as a reference)

## ISSUES SOLVED IN THIS VERSION :
[#164](https://github.com/geneweb/geneweb/issues/164) - export Gedcom UTF8<br />
[#576](https://github.com/geneweb/geneweb/issues/576) - Converting failure of a text file (from utf8 to unicode)<br />
[#611](https://github.com/geneweb/geneweb/issues/611) - Do not split line in the middle of a multi-byte utf-8 char <br />
[#627](https://github.com/geneweb/geneweb/issues/627) - Import/Export GEDCOM : Incorrect charset name used <br />
[#631](https://github.com/geneweb/geneweb/issues/631) - PR #630 : Export GEDCOM : The text of the notes is no longer cut to a fixed length <br />
[#634](https://github.com/geneweb/geneweb/issues/634) - PR #635 : Some command line syntax errors for ged2gwb etc ... not processed. <br />

## KNOWN BUGS/ERRORS, ENHANCEMENTS REQUESTS :
[#137](https://github.com/geneweb/geneweb/issues/137) - PACS<br />
[#143](https://github.com/geneweb/geneweb/issues/143) - gwb2ged : identité <br />
[#172](https://github.com/geneweb/geneweb/issues/172) - Import GEDCOM et "level+1 CONC blabla"<br />
[#240](https://github.com/geneweb/geneweb/issues/240) - Images and their storage location<br />
[#246](https://github.com/geneweb/geneweb/issues/246) - affichage de RELA Godfather ...marraine et filleul inversé <br />
[#283](https://github.com/geneweb/geneweb/issues/283) - Nombre et numérotation des personnes différentes entre la 6.07 et la 7.00<br />
[#284](https://github.com/geneweb/geneweb/issues/284) - version 7.00 , different behavior depending on how sources are written in a GEDCOM<br />
[#286](https://github.com/geneweb/geneweb/issues/286) - Curious errors using ged2gwb<br />
[#320](https://github.com/geneweb/geneweb/issues/320) - GEDCOM date "EST AFT 1731" is not parsed --> Normal (not compliant GEDCOM), EST must be ignore<br />
[#338](https://github.com/geneweb/geneweb/issues/338) - Export Gedcom with internal number<br />
[#389](https://github.com/geneweb/geneweb/issues/389) - Importing GEDCOM may leave inconsistent dates in Geneweb date field<br />
[#394](https://github.com/geneweb/geneweb/issues/394) - ged2gwb: separate multiple notes with a horizontal rule (&lt;hr&gt;)<br />
[#605](https://github.com/geneweb/geneweb/issues/605) - support GEDCOM CHAN tag (change date) <br />
[#620](https://github.com/geneweb/geneweb/issues/620) - Import GEDCOM : "EVEN + TYPE nomen" import don't work without informations added<br />
[#637](https://github.com/geneweb/geneweb/issues/637) - Add BOM decode for UTF-8 encoding in gwc1/gwc2 (and reject other BOM)

## Installation Instructions
see [README.md](../README.md) and [INSTALL](../INSTALL) files

## Release Notes
:warning: To be defined

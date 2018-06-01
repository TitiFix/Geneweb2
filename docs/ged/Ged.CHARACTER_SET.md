# CHARACTER_SET
## Abstract
A code value that represents the character set to be used for read/write with the GEDCOM file.


## GEDCOM syntax and proprietary extensions

**CHARACTER_SET**:={Size=1:9}
<pre>
[ ANSEL | &#x25B6; UTF-8 | UNICODE | &#x1F5D1; ASCII | &#x23E9; ANSI | &#x23E9; MACINTOSH ]
</pre>
Used in <a href=Ged.HEADER_RECORD.md>HEADER_RECORD</a><br />


NOTE:
- &#x1F5D1; ASCII GEDCOM denomination is used for an the "USA version 8-Bits" (not original ASCII 7-Bits, replace by ANSI bellow by most programmers ); This value should be **deprecated**.
- &#x23E9; ANSI is an alias used by many program for ISO/CEI 8859-1 Latin-1. Currently 8859-1 takes over the 8-bit ANSI character set GEDCOM ASCII and ANSI denomination are currently aliases for 8859-1)
- UNICODE is the UTF-16 character set (Little Endian or Big Endian depending byte order mark at the beginning of the gedcom file). UNICODE (UTF-16) is not widely supported.
- Originally, the preferred character set was  ANSEL, which includes ASCII 7 bits as a subset.
- The IBMPC character set is not allowed. This character set cannot be interpreted properly without knowing which code page the sender was using.
- ANSI or &#x25B6; UTF-8 are currently the most popular CHARSET

## Geneweb behavior



- ANSI and MACINTOSH character set missing in gw2ged (export GEDCOM), see <a href=https://github.com/geneweb/geneweb/issues/627>Issue #627</a>
- ASCII must be used (override charset with gw2ged) for import GEDCOM with ANSI character set
- UTF-8 with BOM is not supported, see <a href=https://github.com/geneweb/geneweb/issues/637>Issue #637</a>
- UNICODE are not supported.



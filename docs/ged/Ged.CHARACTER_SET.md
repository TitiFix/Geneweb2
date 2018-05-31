# CHARACTER_SET
## Abstract
A code value that represents the character set to be used for read/write with the GEDCOM file.


## GEDCOM syntax and proprietary extensions

**CHARACTER_SET**:={Size=1:8}
<pre>
[ ANSEL | :play: UTF-8 | UNICODE | :wastebasket: ASCII | :ff: ANSI | :ff: MACINTOSH ]
</pre>
Used in <a href=Ged.HEADER_RECORD.md>HEADER_RECORD</a><br />


NOTE:
- :wastebasket: ASCII GEDCOM denomination is used for an the "USA version 8-Bits" (not original ASCII 7-Bits, replace by ANSI bellow by most programmers ); This value should be **deprecated**.
- :ff: ANSI is an alias used by many program for ISO/CEI 8859-1 Latin-1. Currently 8859-1 takes over the 8-bit ANSI character set GEDCOM ASCII and ANSI denomination are currently aliases for 8859-1)
- UNICODE is the UTF-16 character set (Little Endian or Big Endian depending byte order mark at the beginning of the gedcom file). UNICODE (UTF-16) is not widely supported.
- Originally, the preferred character set was  ANSEL, which includes ASCII 7 bits as a subset.
- The IBMPC character set is not allowed. This character set cannot be interpreted properly without knowing which code page the sender was using.
- ANSI or :play: UTF-8 are currently the most popular CHARSET

## Geneweb behavior



:warning: to be continued/checked


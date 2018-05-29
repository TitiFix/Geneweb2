# Abstract
A code value that represents the character set to be used to interpret this data.
ASCII is the USA version 8-Bit (ANSI)
UNICODE is UTF-16 charset (Little Endian or Big Endian depending byte order mark at the beginning of the gedcom file)
ANSI is an alias used by many program for ISO/CEI 8859-1 Latin-1. Currently 8859-1 takes over the 8-bit ANSI character set (same charset as ASCII)
Originally, the preferred character set was  ANSEL, which includes ASCII as a subset.
UNICODE (UTF-16) is not widely supported.


# GEDCOM Syntax (extension included)
Convention used : **bold** when mandatory, _italic_ when add by 5.5.1 draft, &#x23E9; indicate proprietary coding commonly used (amendment need to standard)<br />

**CHARACTER_SET**:={Size=1:8}
<pre>
[ ANSEL | UTF-8 | UNICODE | ASCII | &#x23E9; ANSI]
</pre>
Used in <a href=Ged.HEADER_RECORD.md>HEADER_RECORD</a><br />


NOTE :
- The IBMPC character set is not allowed. This character set cannot be interpreted properly
without knowing which code page the sender was using.
- UNICODE (UTF-16) is not widely supported.
- ANSI or UTF-8 are currently the most popular CHARSET
# Geneweb behavior


:warning: to be continued/checked


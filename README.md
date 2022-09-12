CRC-64
======

Simple cross-platform command-line tool for computing CRC-64 checksums.

```
Synopsis:
   crc64.exe [OPTIONS] [<file_1> [<file_2> ... <file_n>]]

Options:
   --help --version  Print help screen / show version information
   --binary          Output the digest in binary format (default is hex-format)
   --decimal         Output the digest in decimal string format
   --upper-case      Print hex-string as upper-case (default is lower-case)
   --no-padding      Print the digest *without* any leading zeros
   --silent          Suppress error messages
   --ignore-errors   Ignore I/O errors and proceeed with the next file
   --no-flush        Do *not* flush the standard output stream after each file
   --init-with-zero  Initialize CRC with zero (default is 0xFFF...FFF)
   --negate-final    Negate the final CRC result
```

One output line is generated per input file:
```
<CRC64-Checksum>[SP]<File-Size>[SP]<File-Name>[LF]
```
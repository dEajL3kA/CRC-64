CRC-64
======

Simple cross-platform command-line tool for computing **CRC-64** ([ECMA-182](https://www.ecma-international.org/wp-content/uploads/ECMA-182_1st_edition_december_1992.pdf)) checksums.

Generator polynomial: **`0x42F0E1EBA9EA3693`**

By default, the computation is initialized with `0xFFF…FFF`, the length of the input data is appended to the message, and the final CRC value is **not** negated. The default output format is hexadecimal (base-16), padded with leading zeros.

```
Synopsis:
   crc64.exe [OPTIONS] [<file_1> [<file_2> ... <file_n>]]

Options:
   -h --help --version  Show help screen / show version information
   -b --binary          Output digest in binary format (default is hex-string)
   -d --decimal         Output digest in decimal string format
   -u --upper-case      Print digest as upper-case (default is lower-case)
   -p --no-padding      Print digest *without* any leading zeros
   -s --silent          Suppress error messages
   -e --ignore-errors   Ignore I/O errors and proceed with the next file
   -f --no-flush        Do *not* flush output stream after each file
   -z --init-with-zero  Initialize CRC with 0x000..000 (default is 0xFFF..FFF)
   -l --no-length       Do *not* append the input length to the message
   -n --negate-final    Negate the final CRC result
   -t --self-test       Run integrated self-test and exit program
```

One output line is generated per input file:
```
<CRC64-Checksum> <File-Size> <File-Name>
```

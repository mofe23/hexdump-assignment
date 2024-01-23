---
created: 2024-01-23T15:08
updated: 2024-01-23T15:18
---

## Overview

In this assignment, you will create a Java program that functions as a basic hexdump utility. This program will be run from the command line interface (CLI) and will take a single filename as its first argument. The program will read the content of the specified file and output its hexdump to the standard output (stdout). Each row of the hexdump will represent 16 bytes of the file, showing the row's start address, its hexadecimal representation, and its ASCII representation. Non-printable characters should be represented as `.` in the ASCII representation. For details see examples below.

## Objectives

- Understand how to handle file inputs and outputs in Java.
- Learn to manipulate data formats and representations.
- Practice generating formatted output.
- Get familiar with the CLI arguments handling in Java.

## Requirements

1. **Command Line Interface (CLI) Arguments**: Your program must accept a filename as its first argument from the command line.
2. **File Reading**: Your program should read the content of the specified file.
3. **Hexdump Output**:
   - Each row of the output should represent 16 bytes from the file.
   - Include the row's start address in hexadecimal at the beginning of each line.
   - Following the address, show the hexadecimal representation of each byte.
   - After the hexadecimal representation, include the ASCII representation of the 16 bytes. Non-printable characters should be represented as `.`.
   - Ensure your output is well-formatted and aligned.
4. **Error Handling**: Your program should handle the following errors gracefully:
   - File not found: Display a user-friendly message and exit.
   - Insufficient permissions to read the file: Display a message and exit.

5. **Comments and Code Quality**: Your code should be:
   - Well-commented, explaining the purpose of major blocks or tricky parts.
   - Organized and readable with proper variable naming and consistent indentation.


## Submission

- Create a public repository on your personal GitHub account and commit your code there
- Ensure your program compiles and runs without errors.
- Include a short README with instructions on how to compile and run your program.

## Evaluation Criteria

- Correctness and completeness of the program.
- Code quality, including readability, and adherence to Java best practices.
- Handling of edge cases and error conditions.

## Samples
### Sample 1

``` shell
$ ./hexdump hello-world.txt
00000000  48 65 6c 6c 6f 20 57 6f  72 6c 64 21 20 47 75 74  |Hello World! Gut|
00000010  20 67 65 73 63 68 6c 61  66 65 6e 3f 0a           | geschlafen?.|
```

### Sample 2

![mushroom.ico](./mushroom.ico)

``` shell
$ hexdump mushroom.ico
00000000  00 00 01 00 01 00 00 00  00 00 01 00 20 00 51 05  |............ .Q.|
00000010  00 00 16 00 00 00 89 50  4e 47 0d 0a 1a 0a 00 00  |.......PNG......|
00000020  00 0d 49 48 44 52 00 00  01 00 00 00 01 00 08 06  |..IHDR..........|
00000030  00 00 00 5c 72 a8 66 00  00 00 06 62 4b 47 44 00  |...\r.f....bKGD.|
00000040  00 00 00 00 00 f9 43 bb  7f 00 00 00 09 70 48 59  |......C......pHY|
00000050  73 00 00 00 48 00 00 00  48 00 46 c9 6b 3e 00 00  |s...H...H.F.k>..|
00000060  00 09 76 70 41 67 00 00  01 00 00 00 01 00 00 b2  |..vpAg..........|
00000070  67 dc 8a 00 00 04 7a 49  44 41 54 78 da ed dd b1  |g.....zIDATx....|
00000080  6d dc 40 10 40 51 9e a1  80 e5 b8 04 96 e4 d0 25  |m.@.@Q.........%|
00000090  38 54 49 2c 41 e5 5c 26  f7 e0 31 30 20 fe 7b 39  |8TI,A.\&..10 .{9|
000000a0  79 2b 1e f5 b1 c9 ce bd  ee fb 3e f8 77 d7 75 7d  |y+........>.w.u}|
000000b0  6f af a1 ec be ef d7 f6  1a 9e ec c7 f6 02 80 3d  |o..............=|
000000c0  02 00 61 02 00 61 02 00  61 02 00 61 02 00 61 02  |..a..a..a..a..a.|
000000d0  00 61 02 00 61 02 00 61  02 00 61 02 00 61 02 00  |.a..a..a..a..a..|
000000e0  61 02 00 61 02 00 61 02  00 61 1f db 0b 98 da 3e  |a..a..a..a.....>|
000000f0  8f ff 7e bf 57 ff fe cf  f3 5c fd fc 6d db df ff  |..~.W....\..m...|
00000100  d3 e7 11 d8 01 40 98 00  40 98 00 40 98 00 40 98  |.....@..@..@..@.|
00000110  00 40 98 00 40 98 00 40  98 00 40 98 00 40 98 00  |.@..@..@..@..@..|
00000120  40 98 00 40 98 00 40 98  00 40 98 00 40 98 00 40  |@..@..@..@..@..@|
00000130  d8 fa 3c 80 e9 79 ee ed  f3 f8 db 7e 6e 2f 60 d9  |..<..y.....~n/`.|
00000140  f6 f7 7f 9e e7 e8 fd dd  9e 27 60 07 00 61 02 00  |.........'`..a..|
00000150  61 02 00 61 02 00 61 02  00 61 02 00 61 02 00 61  |a..a..a..a..a..a|
00000160  02 00 61 02 00 61 02 00  61 02 00 61 02 00 61 02  |..a..a..a..a..a.|
00000170  00 61 02 00 61 02 00 61  e3 79 00 ce f3 0f 9d e7  |.a..a..a.y......|
00000180  e8 f2 6b 7b fd cb ee e9  f3 1b be 7f d3 f7 77 7b  |..k{..........w{|
00000190  9e 80 1d 00 84 09 00 84  09 00 84 09 00 84 09 00  |................|
000001a0  84 09 00 84 09 00 84 09  00 84 09 00 84 09 00 84  |................|
000001b0  09 00 84 09 00 84 09 00  84 09 00 84 09 00 84 8d  |................|
000001c0  e7 01 e4 0d cf a3 8f c5  e7 29 5c c3 e7 bf 3d 4f  |.........)\...=O|
000001d0  60 9b 1d 00 84 09 00 84  09 00 84 09 00 84 09 00  |`...............|
000001e0  84 09 00 84 09 00 84 09  00 84 09 00 84 09 00 84  |................|
000001f0  09 00 84 09 00 84 09 00  84 09 00 84 09 00 84 bd  |................|
00000200  8e e3 18 fd 3e f9 9f e1  02 7e 0e af bf fe e3 c3  |....>....~......|
00000210  58 f1 f0 f3 e4 8f 37 9d  27 30 fc f8 af e1 f5 bf  |X.....7.'0......|
00000220  87 d7 db 01 40 98 00 40  98 00 40 98 00 40 98 00  |....@..@..@..@..|
00000230  40 98 00 40 98 00 40 98  00 40 98 00 40 98 00 40  |@..@..@..@..@..@|
00000240  98 00 40 98 00 40 98 00  40 98 00 40 98 00 40 d8  |..@..@..@..@..@.|
00000250  c7 f6 02 d6 7f 5f 7d 78  1e 1c 9e cc 0e 00 c2 04  |....._}x........|
00000260  00 c2 04 00 c2 04 00 c2  04 00 c2 04 00 c2 04 00  |................|
00000270  c2 04 00 c2 04 00 c2 04  00 c2 04 00 c2 04 00 c2  |................|
00000280  04 00 c2 04 00 c2 04 00  c2 5e c7 71 7c 4f 6e f0  |.........^.q|On.|
00000290  de 3e cf bf 6d 3a 4f a0  fe fc b6 0d bf bf 7b f8  |.>..m:O.......{.|
000002a0  f1 d3 79 18 e7 70 fd 76  00 10 26 00 10 26 00 10  |..y..p.v..&..&..|
000002b0  26 00 10 26 00 10 26 00  10 26 00 10 26 00 10 26  |&..&..&..&..&..&|
000002c0  00 10 26 00 10 26 00 10  26 00 10 26 00 10 26 00  |..&..&..&..&..&.|
000002d0  10 26 00 10 f6 b1 bd 80  a7 bb a7 37 18 9e e7 9e  |.&.........7....|
000002e0  9e 27 7f ba 7b 3a 8f 61  e8 e9 cf df 0e 00 c2 04  |.'..{:.a........|
000002f0  00 c2 04 00 c2 04 00 c2  04 00 c2 04 00 c2 04 00  |................|
00000300  c2 04 00 c2 04 00 c2 04  00 c2 04 00 c2 04 00 c2  |................|
00000310  04 00 c2 04 00 c2 04 00  c2 c6 f3 00 3e 87 e7 b1  |............>...|
00000320  7f 2d 9f a7 9e ae 7f db  d7 c3 d7 ff 74 d7 f6 02  |.-..........t...|
00000330  86 ec 00 20 4c 00 20 4c  00 20 4c 00 20 4c 00 20  |... L. L. L. L. |
00000340  4c 00 20 4c 00 20 4c 00  20 4c 00 20 4c 00 20 4c  |L. L. L. L. L. L|
00000350  00 20 4c 00 20 4c 00 20  4c 00 20 4c 00 20 ec 75  |. L. L. L. L. .u|
00000360  1c c7 f7 e4 06 7f b6 ff  82 a1 df db 0b 60 d5 f6  |.............`..|
00000370  fb 3b 9d 87 71 0e e7 41  d8 01 40 98 00 40 98 00  |.;..q..A..@..@..|
00000380  40 98 00 40 98 00 40 98  00 40 98 00 40 98 00 40  |@..@..@..@..@..@|
00000390  98 00 40 98 00 40 98 00  40 98 00 40 98 00 40 98  |..@..@..@..@..@.|
000003a0  00 40 98 00 40 d8 eb be  ef d1 0d ae eb 1a cd 13  |.@..@...........|
000003b0  d8 f6 1e 9e c7 9e 9a 9e  e7 b6 fe dd f5 6f bb ef  |.............o..|
000003c0  fb 35 b9 de 0e 00 c2 04  00 c2 04 00 c2 04 00 c2  |.5..............|
000003d0  04 00 c2 04 00 c2 04 00  c2 04 00 c2 04 00 c2 04  |................|
000003e0  00 c2 04 00 c2 04 00 c2  04 00 c2 04 00 c2 04 00  |................|
000003f0  c2 3e a6 37 98 9e 47 9e  ce 13 d8 3e 4f ce b3 4d  |.>.7..G....>O..M|
00000400  df 9f e9 3c 81 e9 ff cf  94 1d 00 84 09 00 84 09  |...<............|
00000410  00 84 09 00 84 09 00 84  09 00 84 09 00 84 09 00  |................|
00000420  84 09 00 84 09 00 84 09  00 84 09 00 84 09 00 84  |................|
00000430  09 00 84 09 00 84 8d e7  01 30 f3 f4 79 06 4f 5f  |.........0..y.O_|
00000440  7f 9d 1d 00 84 09 00 84  09 00 84 09 00 84 09 00  |................|
00000450  84 09 00 84 09 00 84 09  00 84 09 00 84 09 00 84  |................|
00000460  09 00 84 09 00 84 09 00  84 09 00 84 09 00 84 ad  |................|
00000470  cf 03 98 fe 3e fa 79 9e  df 93 eb 9d 67 6f 3b cf  |....>.y.....go;.|
00000480  73 74 fd f4 fd dd 66 07  00 61 02 00 61 02 00 61  |st....f..a..a..a|
00000490  02 00 61 02 00 61 02 00  61 02 00 61 02 00 61 02  |..a..a..a..a..a.|
000004a0  00 61 02 00 61 02 00 61  02 00 61 02 00 61 02 00  |.a..a..a..a..a..|
000004b0  61 02 00 61 eb f3 00 a6  b6 e7 09 f0 6c 4f 3f cf  |a..a........lO?.|
000004c0  3f 65 07 00 61 02 00 61  02 00 61 02 00 61 02 00  |?e..a..a..a..a..|
000004d0  61 02 00 61 02 00 61 02  00 61 02 00 61 02 00 61  |a..a..a..a..a..a|
000004e0  02 00 61 02 00 61 02 00  61 02 00 61 02 00 61 7f  |..a..a..a..a..a.|
000004f0  01 e0 cf 80 9f 01 48 d0  6e 00 00 00 25 74 45 58  |......H.n...%tEX|
00000500  74 64 61 74 65 3a 63 72  65 61 74 65 00 32 30 31  |tdate:create.201|
00000510  30 2d 30 35 2d 30 32 54  32 31 3a 31 36 3a 31 34  |0-05-02T21:16:14|
00000520  2d 30 35 3a 30 30 ea 59  72 1b 00 00 00 25 74 45  |-05:00.Yr....%tE|
00000530  58 74 64 61 74 65 3a 6d  6f 64 69 66 79 00 32 30  |Xtdate:modify.20|
00000540  31 30 2d 30 35 2d 30 32  54 32 31 3a 31 36 3a 31  |10-05-02T21:16:1|
00000550  34 2d 30 35 3a 30 30 9b  04 ca a7 00 00 00 00 49  |4-05:00........I|
00000560  45 4e 44 ae 42 60 82                              |END.B`.|
```

### Sample 3

![grad8rgb.bmp](grad8rgb.bmp)

``` shell
❯ ./hexdump grad8rgb.bmp
00000000  42 4d 36 0c 00 00 00 00  00 00 36 00 00 00 28 00  |BM6.......6...(.|
00000010  00 00 20 00 00 00 20 00  00 00 01 00 18 00 00 00  |.. ... .........|
00000020  00 00 00 00 00 00 12 0b  00 00 12 0b 00 00 00 00  |................|
00000030  00 00 00 00 00 00 fb fa  03 f3 fa 0b eb fa 13 e3  |................|
00000040  fa 1b db fa 23 d3 fa 2b  cb fa 33 c3 fa 3b bb fa  |....#..+..3..;..|
00000050  43 b3 fa 4b ab fa 53 a3  fa 5b 9b fa 63 93 fa 6b  |C..K..S..[..c..k|
00000060  8b fa 73 83 fa 7b 7b fa  83 74 fa 8b 6b fa 93 64  |..s..{{..t..k..d|
00000070  fa 9b 5c fa a2 54 fa aa  4c fa b2 44 fa ba 3c fa  |..\..T..L..D..<.|
00000080  c2 34 fa ca 2c fa d2 24  fa da 1c fa e2 14 fa ea  |.4..,..$........|
00000090  0c fa f2 04 fa fa fb f2  03 f3 f2 0b eb f2 13 e3  |................|
000000a0  f2 1b db f2 23 d3 f2 2b  cb f2 33 c3 f2 3b bb f2  |....#..+..3..;..|
000000b0  43 b3 f2 4b ab f2 53 a3  f2 5b 9b f2 63 93 f2 6b  |C..K..S..[..c..k|
000000c0  8b f2 73 83 f2 7b 7b f2  83 74 f2 8b 6b f2 93 64  |..s..{{..t..k..d|
000000d0  f2 9b 5c f2 a2 54 f2 aa  4c f2 b2 44 f2 ba 3c f2  |..\..T..L..D..<.|
000000e0  c2 34 f2 ca 2c f2 d2 24  f2 da 1c f2 e2 14 f2 ea  |.4..,..$........|
000000f0  0c f2 f2 04 f2 fa fb ea  03 f3 ea 0b eb ea 13 e3  |................|
00000100  ea 1b db ea 23 d3 ea 2b  cb ea 33 c3 ea 3b bb ea  |....#..+..3..;..|
00000110  43 b3 ea 4b ab ea 53 a3  ea 5b 9b ea 63 93 ea 6b  |C..K..S..[..c..k|
00000120  8b ea 73 83 ea 7b 7b ea  83 74 ea 8b 6b ea 93 64  |..s..{{..t..k..d|
00000130  ea 9b 5c ea a2 54 ea aa  4c ea b2 44 ea ba 3c ea  |..\..T..L..D..<.|
00000140  c2 34 ea ca 2c ea d2 24  ea da 1c ea e2 14 ea ea  |.4..,..$........|
00000150  0c ea f2 04 ea fa fb e2  03 f3 e2 0b eb e2 13 e3  |................|
00000160  e2 1b db e2 23 d3 e2 2b  cb e2 33 c3 e2 3b bb e2  |....#..+..3..;..|
00000170  43 b3 e2 4b ab e2 53 a3  e2 5b 9b e2 63 93 e2 6b  |C..K..S..[..c..k|
00000180  8b e2 73 83 e2 7b 7b e2  83 74 e2 8b 6b e2 93 64  |..s..{{..t..k..d|
00000190  e2 9b 5c e2 a2 54 e2 aa  4c e2 b2 44 e2 ba 3c e2  |..\..T..L..D..<.|
000001a0  c2 34 e2 ca 2c e2 d2 24  e2 da 1c e2 e2 14 e2 ea  |.4..,..$........|
000001b0  0c e2 f2 04 e2 fa fb da  03 f3 da 0b eb da 13 e3  |................|
000001c0  da 1b db da 23 d3 da 2b  cb da 33 c3 da 3b bb da  |....#..+..3..;..|
000001d0  43 b3 da 4b ab da 53 a3  da 5b 9b da 63 93 da 6b  |C..K..S..[..c..k|
000001e0  8b da 73 83 da 7b 7b da  83 74 da 8b 6b da 93 64  |..s..{{..t..k..d|
000001f0  da 9b 5c da a2 54 da aa  4c da b2 44 da ba 3c da  |..\..T..L..D..<.|
00000200  c2 34 da ca 2c da d2 24  da da 1c da e2 14 da ea  |.4..,..$........|
00000210  0c da f2 04 da fa fb d2  03 f3 d2 0b eb d2 13 e3  |................|
00000220  d2 1b db d2 23 d3 d2 2b  cb d2 33 c3 d2 3b bb d2  |....#..+..3..;..|
00000230  43 b3 d2 4b ab d2 53 a3  d2 5b 9b d2 63 93 d2 6b  |C..K..S..[..c..k|
00000240  8b d2 73 83 d2 7b 7b d2  83 74 d2 8b 6b d2 93 64  |..s..{{..t..k..d|
00000250  d2 9b 5c d2 a2 54 d2 aa  4c d2 b2 44 d2 ba 3c d2  |..\..T..L..D..<.|
00000260  c2 34 d2 ca 2c d2 d2 24  d2 da 1c d2 e2 14 d2 ea  |.4..,..$........|
00000270  0c d2 f2 04 d2 fa fb ca  03 f3 ca 0b eb ca 13 e3  |................|
00000280  ca 1b db ca 23 d3 ca 2b  cb ca 33 c3 ca 3b bb ca  |....#..+..3..;..|
00000290  43 b3 ca 4b ab ca 53 a3  ca 5b 9b ca 63 93 ca 6b  |C..K..S..[..c..k|
000002a0  8b ca 73 83 ca 7b 7b ca  83 74 ca 8b 6b ca 93 64  |..s..{{..t..k..d|
000002b0  ca 9b 5c ca a2 54 ca aa  4c ca b2 44 ca ba 3c ca  |..\..T..L..D..<.|
000002c0  c2 34 ca ca 2c ca d2 24  ca da 1c ca e2 14 ca ea  |.4..,..$........|
000002d0  0c ca f2 04 ca fa fb c2  03 f3 c2 0b eb c2 13 e3  |................|
000002e0  c2 1b db c2 23 d3 c2 2b  cb c2 33 c3 c2 3b bb c2  |....#..+..3..;..|
000002f0  43 b3 c2 4b ab c2 53 a3  c2 5b 9b c2 63 93 c2 6b  |C..K..S..[..c..k|
00000300  8b c2 73 83 c2 7b 7b c2  83 74 c2 8b 6b c2 93 64  |..s..{{..t..k..d|
00000310  c2 9b 5c c2 a2 54 c2 aa  4c c2 b2 44 c2 ba 3c c2  |..\..T..L..D..<.|
00000320  c2 34 c2 ca 2c c2 d2 24  c2 da 1c c2 e2 14 c2 ea  |.4..,..$........|
00000330  0c c2 f2 04 c2 fa fb ba  03 f3 ba 0b eb ba 13 e3  |................|
00000340  ba 1b db ba 23 d3 ba 2b  cb ba 33 c3 ba 3b bb ba  |....#..+..3..;..|
00000350  43 b3 ba 4b ab ba 53 a3  ba 5b 9b ba 63 93 ba 6b  |C..K..S..[..c..k|
00000360  8b ba 73 83 ba 7b 7b ba  83 74 ba 8b 6b ba 93 64  |..s..{{..t..k..d|
00000370  ba 9b 5c ba a2 54 ba aa  4c ba b2 44 ba ba 3c ba  |..\..T..L..D..<.|
00000380  c2 34 ba ca 2c ba d2 24  ba da 1c ba e2 14 ba ea  |.4..,..$........|
00000390  0c ba f2 04 ba fa fb b2  03 f3 b2 0b eb b2 13 e3  |................|
000003a0  b2 1b db b2 23 d3 b2 2b  cb b2 33 c3 b2 3b bb b2  |....#..+..3..;..|
000003b0  43 b3 b2 4b ab b2 53 a3  b2 5b 9b b2 63 93 b2 6b  |C..K..S..[..c..k|
000003c0  8b b2 73 83 b2 7b 7b b2  83 74 b2 8b 6b b2 93 64  |..s..{{..t..k..d|
000003d0  b2 9b 5c b2 a2 54 b2 aa  4c b2 b2 44 b2 ba 3c b2  |..\..T..L..D..<.|
000003e0  c2 34 b2 ca 2c b2 d2 24  b2 da 1c b2 e2 14 b2 ea  |.4..,..$........|
000003f0  0c b2 f2 04 b2 fa fb aa  03 f3 aa 0b eb aa 13 e3  |................|
00000400  aa 1b db aa 23 d3 aa 2b  cb aa 33 c3 aa 3b bb aa  |....#..+..3..;..|
00000410  43 b3 aa 4b ab aa 53 a3  aa 5b 9b aa 63 93 aa 6b  |C..K..S..[..c..k|
00000420  8b aa 73 83 aa 7b 7b aa  83 74 aa 8b 6b aa 93 64  |..s..{{..t..k..d|
00000430  aa 9b 5c aa a2 54 aa aa  4c aa b2 44 aa ba 3c aa  |..\..T..L..D..<.|
00000440  c2 34 aa ca 2c aa d2 24  aa da 1c aa e2 14 aa ea  |.4..,..$........|
00000450  0c aa f2 04 aa fa fb a2  03 f3 a2 0b eb a2 13 e3  |................|
00000460  a2 1b db a2 23 d3 a2 2b  cb a2 33 c3 a2 3b bb a2  |....#..+..3..;..|
00000470  43 b3 a2 4b ab a2 53 a3  a2 5b 9b a2 63 93 a2 6b  |C..K..S..[..c..k|
00000480  8b a2 73 83 a2 7b 7b a2  83 74 a2 8b 6b a2 93 64  |..s..{{..t..k..d|
00000490  a2 9b 5c a2 a2 54 a2 aa  4c a2 b2 44 a2 ba 3c a2  |..\..T..L..D..<.|
000004a0  c2 34 a2 ca 2c a2 d2 24  a2 da 1c a2 e2 14 a2 ea  |.4..,..$........|
000004b0  0c a2 f2 04 a2 fa fb 9b  03 f3 9b 0b eb 9b 13 e3  |................|
000004c0  9b 1b db 9b 23 d3 9b 2b  cb 9b 33 c3 9b 3b bb 9b  |....#..+..3..;..|
000004d0  43 b3 9b 4b ab 9b 53 a3  9b 5b 9b 9b 63 93 9b 6b  |C..K..S..[..c..k|
000004e0  8b 9b 73 83 9b 7b 7b 9b  83 74 9b 8b 6b 9b 93 64  |..s..{{..t..k..d|
000004f0  9b 9b 5c 9b a2 54 9b aa  4c 9b b2 44 9b ba 3c 9b  |..\..T..L..D..<.|
00000500  c2 34 9b ca 2c 9b d2 24  9b da 1c 9b e2 14 9b ea  |.4..,..$........|
00000510  0c 9b f2 04 9b fa fb 93  03 f3 93 0b eb 93 13 e3  |................|
00000520  93 1b db 93 23 d3 93 2b  cb 93 33 c3 93 3b bb 93  |....#..+..3..;..|
00000530  43 b3 93 4b ab 93 53 a3  93 5b 9b 93 63 93 93 6b  |C..K..S..[..c..k|
00000540  8b 93 73 83 93 7b 7b 93  83 74 93 8b 6b 93 93 64  |..s..{{..t..k..d|
00000550  93 9b 5c 93 a2 54 93 aa  4c 93 b2 44 93 ba 3c 93  |..\..T..L..D..<.|
00000560  c2 34 93 ca 2c 93 d2 24  93 da 1c 93 e2 14 93 ea  |.4..,..$........|
00000570  0c 93 f2 04 93 fa fb 8b  03 f3 8b 0b eb 8b 13 e3  |................|
00000580  8b 1b db 8b 23 d3 8b 2b  cb 8b 33 c3 8b 3b bb 8b  |....#..+..3..;..|
00000590  43 b3 8b 4b ab 8b 53 a3  8b 5b 9b 8b 63 93 8b 6b  |C..K..S..[..c..k|
000005a0  8b 8b 73 83 8b 7b 7b 8b  83 74 8b 8b 6b 8b 93 64  |..s..{{..t..k..d|
000005b0  8b 9b 5c 8b a2 54 8b aa  4c 8b b2 44 8b ba 3c 8b  |..\..T..L..D..<.|
000005c0  c2 34 8b ca 2c 8b d2 24  8b da 1c 8b e2 14 8b ea  |.4..,..$........|
000005d0  0c 8b f2 04 8b fa fb 83  03 f3 83 0b eb 83 13 e3  |................|
000005e0  83 1b db 83 23 d3 83 2b  cb 83 33 c3 83 3b bb 83  |....#..+..3..;..|
000005f0  43 b3 83 4b ab 83 53 a3  83 5b 9b 83 63 93 83 6b  |C..K..S..[..c..k|
00000600  8b 83 73 83 83 7b 7b 83  83 74 83 8b 6b 83 93 64  |..s..{{..t..k..d|
00000610  83 9b 5c 83 a2 54 83 aa  4c 83 b2 44 83 ba 3c 83  |..\..T..L..D..<.|
00000620  c2 34 83 ca 2c 83 d2 24  83 da 1c 83 e2 14 83 ea  |.4..,..$........|
00000630  0c 83 f2 04 83 fa fb 7b  03 f3 7b 0b eb 7b 13 e3  |.......{..{..{..|
00000640  7b 1b db 7b 23 d3 7b 2b  cb 7b 33 c3 7b 3b bb 7b  |{..{#.{+.{3.{;.{|
00000650  43 b3 7b 4b ab 7b 53 a3  7b 5b 9b 7b 63 93 7b 6b  |C.{K.{S.{[.{c.{k|
00000660  8b 7b 73 83 7b 7b 7b 7b  83 74 7b 8b 6b 7b 93 64  |.{s.{{{{.t{.k{.d|
00000670  7b 9b 5c 7b a2 54 7b aa  4c 7b b2 44 7b ba 3c 7b  |{.\{.T{.L{.D{.<{|
00000680  c2 34 7b ca 2c 7b d2 24  7b da 1c 7b e2 14 7b ea  |.4{.,{.${..{..{.|
00000690  0c 7b f2 04 7b fa fb 73  03 f3 73 0b eb 73 13 e3  |.{..{..s..s..s..|
000006a0  73 1b db 73 23 d3 73 2b  cb 73 33 c3 73 3b bb 73  |s..s#.s+.s3.s;.s|
000006b0  43 b3 73 4b ab 73 53 a3  73 5b 9b 73 63 93 73 6b  |C.sK.sS.s[.sc.sk|
000006c0  8b 73 73 83 73 7b 7b 73  83 74 73 8b 6b 73 93 64  |.ss.s{{s.ts.ks.d|
000006d0  73 9b 5c 73 a2 54 73 aa  4c 73 b2 44 73 ba 3c 73  |s.\s.Ts.Ls.Ds.<s|
000006e0  c2 34 73 ca 2c 73 d2 24  73 da 1c 73 e2 14 73 ea  |.4s.,s.$s..s..s.|
000006f0  0c 73 f2 04 73 fa fb 6b  03 f3 6b 0b eb 6b 13 e3  |.s..s..k..k..k..|
00000700  6b 1b db 6b 23 d3 6b 2b  cb 6b 33 c3 6b 3b bb 6b  |k..k#.k+.k3.k;.k|
00000710  43 b3 6b 4b ab 6b 53 a3  6b 5b 9b 6b 63 93 6b 6b  |C.kK.kS.k[.kc.kk|
00000720  8b 6b 73 83 6b 7b 7b 6b  83 74 6b 8b 6b 6b 93 64  |.ks.k{{k.tk.kk.d|
00000730  6b 9b 5c 6b a2 54 6b aa  4c 6b b2 44 6b ba 3c 6b  |k.\k.Tk.Lk.Dk.<k|
00000740  c2 34 6b ca 2c 6b d2 24  6b da 1c 6b e2 14 6b ea  |.4k.,k.$k..k..k.|
00000750  0c 6b f2 04 6b fa fb 63  03 f3 63 0b eb 63 13 e3  |.k..k..c..c..c..|
00000760  63 1b db 63 23 d3 63 2b  cb 63 33 c3 63 3b bb 63  |c..c#.c+.c3.c;.c|
00000770  43 b3 63 4b ab 63 53 a3  63 5b 9b 63 63 93 63 6b  |C.cK.cS.c[.cc.ck|
00000780  8b 63 73 83 63 7b 7b 63  83 74 63 8b 6b 63 93 64  |.cs.c{{c.tc.kc.d|
00000790  63 9b 5c 63 a2 54 63 aa  4c 63 b2 44 63 ba 3c 63  |c.\c.Tc.Lc.Dc.<c|
000007a0  c2 34 63 ca 2c 63 d2 24  63 da 1c 63 e2 14 63 ea  |.4c.,c.$c..c..c.|
000007b0  0c 63 f2 04 63 fa fb 5b  03 f3 5b 0b eb 5b 13 e3  |.c..c..[..[..[..|
000007c0  5b 1b db 5b 23 d3 5b 2b  cb 5b 33 c3 5b 3b bb 5b  |[..[#.[+.[3.[;.[|
000007d0  43 b3 5b 4b ab 5b 53 a3  5b 5b 9b 5b 63 93 5b 6b  |C.[K.[S.[[.[c.[k|
000007e0  8b 5b 73 83 5b 7b 7b 5b  83 74 5b 8b 6b 5b 93 64  |.[s.[{{[.t[.k[.d|
000007f0  5b 9b 5c 5b a2 54 5b aa  4c 5b b2 44 5b ba 3c 5b  |[.\[.T[.L[.D[.<[|
00000800  c2 34 5b ca 2c 5b d2 24  5b da 1c 5b e2 14 5b ea  |.4[.,[.$[..[..[.|
00000810  0c 5b f2 04 5b fa fb 53  03 f3 53 0b eb 53 13 e3  |.[..[..S..S..S..|
00000820  53 1b db 53 23 d3 53 2b  cb 53 33 c3 53 3b bb 53  |S..S#.S+.S3.S;.S|
00000830  43 b3 53 4b ab 53 53 a3  53 5b 9b 53 63 93 53 6b  |C.SK.SS.S[.Sc.Sk|
00000840  8b 53 73 83 53 7b 7b 53  83 74 53 8b 6b 53 93 64  |.Ss.S{{S.tS.kS.d|
00000850  53 9b 5c 53 a2 54 53 aa  4c 53 b2 44 53 ba 3c 53  |S.\S.TS.LS.DS.<S|
00000860  c2 34 53 ca 2c 53 d2 24  53 da 1c 53 e2 14 53 ea  |.4S.,S.$S..S..S.|
00000870  0c 53 f2 04 53 fa fb 4b  03 f3 4b 0b eb 4b 13 e3  |.S..S..K..K..K..|
00000880  4b 1b db 4b 23 d3 4b 2b  cb 4b 33 c3 4b 3b bb 4b  |K..K#.K+.K3.K;.K|
00000890  43 b3 4b 4b ab 4b 53 a3  4b 5b 9b 4b 63 93 4b 6b  |C.KK.KS.K[.Kc.Kk|
000008a0  8b 4b 73 83 4b 7b 7b 4b  83 74 4b 8b 6b 4b 93 64  |.Ks.K{{K.tK.kK.d|
000008b0  4b 9b 5c 4b a2 54 4b aa  4c 4b b2 44 4b ba 3c 4b  |K.\K.TK.LK.DK.<K|
000008c0  c2 34 4b ca 2c 4b d2 24  4b da 1c 4b e2 14 4b ea  |.4K.,K.$K..K..K.|
000008d0  0c 4b f2 04 4b fa fb 43  03 f3 43 0b eb 43 13 e3  |.K..K..C..C..C..|
000008e0  43 1b db 43 23 d3 43 2b  cb 43 33 c3 43 3b bb 43  |C..C#.C+.C3.C;.C|
000008f0  43 b3 43 4b ab 43 53 a3  43 5b 9b 43 63 93 43 6b  |C.CK.CS.C[.Cc.Ck|
00000900  8b 43 73 83 43 7b 7b 43  83 74 43 8b 6b 43 93 64  |.Cs.C{{C.tC.kC.d|
00000910  43 9b 5c 43 a2 54 43 aa  4c 43 b2 44 43 ba 3c 43  |C.\C.TC.LC.DC.<C|
00000920  c2 34 43 ca 2c 43 d2 24  43 da 1c 43 e2 14 43 ea  |.4C.,C.$C..C..C.|
00000930  0c 43 f2 04 43 fa fb 3b  03 f3 3b 0b eb 3b 13 e3  |.C..C..;..;..;..|
00000940  3b 1b db 3b 23 d3 3b 2b  cb 3b 33 c3 3b 3b bb 3b  |;..;#.;+.;3.;;.;|
00000950  43 b3 3b 4b ab 3b 53 a3  3b 5b 9b 3b 63 93 3b 6b  |C.;K.;S.;[.;c.;k|
00000960  8b 3b 73 83 3b 7b 7b 3b  83 74 3b 8b 6b 3b 93 64  |.;s.;{{;.t;.k;.d|
00000970  3b 9b 5c 3b a2 54 3b aa  4c 3b b2 44 3b ba 3c 3b  |;.\;.T;.L;.D;.<;|
00000980  c2 34 3b ca 2c 3b d2 24  3b da 1c 3b e2 14 3b ea  |.4;.,;.$;..;..;.|
00000990  0c 3b f2 04 3b fa fb 33  03 f3 33 0b eb 33 13 e3  |.;..;..3..3..3..|
000009a0  33 1b db 33 23 d3 33 2b  cb 33 33 c3 33 3b bb 33  |3..3#.3+.33.3;.3|
000009b0  43 b3 33 4b ab 33 53 a3  33 5b 9b 33 63 93 33 6b  |C.3K.3S.3[.3c.3k|
000009c0  8b 33 73 83 33 7b 7b 33  83 74 33 8b 6b 33 93 64  |.3s.3{{3.t3.k3.d|
000009d0  33 9b 5c 33 a2 54 33 aa  4c 33 b2 44 33 ba 3c 33  |3.\3.T3.L3.D3.<3|
000009e0  c2 34 33 ca 2c 33 d2 24  33 da 1c 33 e2 14 33 ea  |.43.,3.$3..3..3.|
000009f0  0c 33 f2 04 33 fa fb 2b  03 f3 2b 0b eb 2b 13 e3  |.3..3..+..+..+..|
00000a00  2b 1b db 2b 23 d3 2b 2b  cb 2b 33 c3 2b 3b bb 2b  |+..+#.++.+3.+;.+|
00000a10  43 b3 2b 4b ab 2b 53 a3  2b 5b 9b 2b 63 93 2b 6b  |C.+K.+S.+[.+c.+k|
00000a20  8b 2b 73 83 2b 7b 7b 2b  83 74 2b 8b 6b 2b 93 64  |.+s.+{{+.t+.k+.d|
00000a30  2b 9b 5c 2b a2 54 2b aa  4c 2b b2 44 2b ba 3c 2b  |+.\+.T+.L+.D+.<+|
00000a40  c2 34 2b ca 2c 2b d2 24  2b da 1c 2b e2 14 2b ea  |.4+.,+.$+..+..+.|
00000a50  0c 2b f2 04 2b fa fb 23  03 f3 23 0b eb 23 13 e3  |.+..+..#..#..#..|
00000a60  23 1b db 23 23 d3 23 2b  cb 23 33 c3 23 3b bb 23  |#..##.#+.#3.#;.#|
00000a70  43 b3 23 4b ab 23 53 a3  23 5b 9b 23 63 93 23 6b  |C.#K.#S.#[.#c.#k|
00000a80  8b 23 73 83 23 7b 7b 23  83 74 23 8b 6b 23 93 64  |.#s.#{{#.t#.k#.d|
00000a90  23 9b 5c 23 a2 54 23 aa  4c 23 b2 44 23 ba 3c 23  |#.\#.T#.L#.D#.<#|
00000aa0  c2 34 23 ca 2c 23 d2 24  23 da 1c 23 e2 14 23 ea  |.4#.,#.$#..#..#.|
00000ab0  0c 23 f2 04 23 fa fb 1b  03 f3 1b 0b eb 1b 13 e3  |.#..#...........|
00000ac0  1b 1b db 1b 23 d3 1b 2b  cb 1b 33 c3 1b 3b bb 1b  |....#..+..3..;..|
00000ad0  43 b3 1b 4b ab 1b 53 a3  1b 5b 9b 1b 63 93 1b 6b  |C..K..S..[..c..k|
00000ae0  8b 1b 73 83 1b 7b 7b 1b  83 74 1b 8b 6b 1b 93 64  |..s..{{..t..k..d|
00000af0  1b 9b 5c 1b a2 54 1b aa  4c 1b b2 44 1b ba 3c 1b  |..\..T..L..D..<.|
00000b00  c2 34 1b ca 2c 1b d2 24  1b da 1c 1b e2 14 1b ea  |.4..,..$........|
00000b10  0c 1b f2 04 1b fa fb 13  03 f3 13 0b eb 13 13 e3  |................|
00000b20  13 1b db 13 23 d3 13 2b  cb 13 33 c3 13 3b bb 13  |....#..+..3..;..|
00000b30  43 b3 13 4b ab 13 53 a3  13 5b 9b 13 63 93 13 6b  |C..K..S..[..c..k|
00000b40  8b 13 73 83 13 7b 7b 13  83 74 13 8b 6b 13 93 64  |..s..{{..t..k..d|
00000b50  13 9b 5c 13 a2 54 13 aa  4c 13 b2 44 13 ba 3c 13  |..\..T..L..D..<.|
00000b60  c2 34 13 ca 2c 13 d2 24  13 da 1c 13 e2 14 13 ea  |.4..,..$........|
00000b70  0c 13 f2 04 13 fa fb 0b  03 f3 0b 0b eb 0b 13 e3  |................|
00000b80  0b 1b db 0b 23 d3 0b 2b  cb 0b 33 c3 0b 3b bb 0b  |....#..+..3..;..|
00000b90  43 b3 0b 4b ab 0b 53 a3  0b 5b 9b 0b 63 93 0b 6b  |C..K..S..[..c..k|
00000ba0  8b 0b 73 83 0b 7b 7b 0b  83 74 0b 8b 6b 0b 93 64  |..s..{{..t..k..d|
00000bb0  0b 9b 5c 0b a2 54 0b aa  4c 0b b2 44 0b ba 3c 0b  |..\..T..L..D..<.|
00000bc0  c2 34 0b ca 2c 0b d2 24  0b da 1c 0b e2 14 0b ea  |.4..,..$........|
00000bd0  0c 0b f2 04 0b fa fb 03  03 f3 03 0b eb 03 13 e3  |................|
00000be0  03 1b db 03 23 d3 03 2b  cb 03 33 c3 03 3b bb 03  |....#..+..3..;..|
00000bf0  43 b3 03 4b ab 03 53 a3  03 5b 9b 03 63 93 03 6b  |C..K..S..[..c..k|
00000c00  8b 03 73 83 03 7b 7b 03  83 74 03 8b 6b 03 93 64  |..s..{{..t..k..d|
00000c10  03 9b 5c 03 a2 54 03 aa  4c 03 b2 44 03 ba 3c 03  |..\..T..L..D..<.|
00000c20  c2 34 03 ca 2c 03 d2 24  03 da 1c 03 e2 14 03 ea  |.4..,..$........|
00000c30  0c 03 f2 04 03 fa                                 |......|
```

### Sample 4

``` shell
$ ./hexdump not-found.txt
Error: 'not-found.txt' not found
```

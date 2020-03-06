# XCB

XCB is a frontend for Feteke Csaba's cool XC=Basic compiler for 6502 processors.

## Background
Feteke Csaba has written a really nice BASIC dialect compiler for the Commodore C64 8 bit
computer.

==> https://github.com/neilsf/XC-BASIC

XCB is little bash script front-end to the Edit/Compile/Run loop.

Look'n'Feel is based on TurboPascal 3.0 for CP/M --- seemed appropriate for a compiler for an old 8-bit computer.

## Please note:
==> This is Alpha quality software, things are rough, unfinished and may ass'plode yer computer. :stick_out_tongue: <==

## Getting Started

### Prerequisites

 - Functioning Linux BASH shell.
 - Functioning XC=Basic installation. ==> https://github.com/neilsf/XC-BASIC
 - Functioning DASM 6502 assembler installation ==> https://dasm-assembler.github.io/
 - Functioning VICE C64 emulator installation. ==> http://vice-emu.sourceforge.net/
 - Your favorite text editor. (Vim is set as default ... Why use anything else? https://pascalprecht.github.io/posts/why-i-use-vim)


### Installing

Install VICE as per home page.
Install both XC=Basic and DASM.
All of these programs must be on your $PATH

Install XCB with:

```
git clone https://github.com/mlongval/xcb.git
```

Run XCB with:
```
$ cd to_your_work_directory

$ xcb prog1.bas prog1.prg

XC=Basic --- A 6502 BASIC Compiler
(C) Csaba Fekete
https://github.com/neilsf/XC-BASIC

Executable paths:
Assembler:  /home/user/bin/dasm
Compiler:  /home/user/bin/xcbasic64
Machine:  /home/user/bin/x64
Editor:  /usr/bin/vim

Work File: prog1.bas

Output File: prog1.prg

Edit    Run     Compile Quit

Please select command >

```

Not shown above are the letters in reverse video that
are the 'menu' choices.
Select from the menu and then ENTER.
 - W: shows a file listing of the current working directory. Select the file you want to edit. There
   is no provision for changing directory here. Exit the script to change directory.
 - O: will ask user to enter the output file name (ie: prog1.prg). This is the target file name for
   the compiler
 - E: edit the current Work File.
 - R: run the current Output File.
 - C: compile the current Work File into the current Output File.
 - Q: quit the script

... and that's all folks.

## Built With

 - Bash
 - Vim (what else....)

## Authors

 - XCB Michael Longval ==> https://github.com/mlongval
 - XC=Basic by Feteke Csaba ==> https://github.com/neilsf
 - DASM by multiple authors see ==> https://dasm-assembler.github.io/

## License

This software is licensed under the GNU GENERAL PUBLIC LICENSE, Version 3, 29 June 2007

## Acknowledgments

 * Thanks to Feteke Csaba for the great XC=Basic compiler.
 * Thanks to the folks who maintain dasm https://github.com/dasm-assembler
 * Thanks to Billie Thompson (PurpleBooth) for the README.md template ==> https://gist.github.com/PurpleBooth/c01dc4a3c6acd8658286b7ffe936a8d7
 * Cheers to all retrocomputer nuts out there.

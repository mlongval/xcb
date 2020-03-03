# xcb
## Front-end for XC=Basic. In the style of TurboPascal 3.0

Csaba Fekete has written a really nice BASIC dialect compiler for the Commodore C64 8 bit
computer. ==> see https://github.com/neilsf/XC-BASIC

I wrote this little bash script as a front end to simplify the Edit/Compile/Run
loop. I based the look/function on TurboPascal 3.0 for CP/M --- I felt it
was appropriate for a compiler for an 8-bit computer.

This is Beta quality software, so things are unfinished.

Quick info: **xcb** will look for executables (dasm, xcbasic64, x64, text editor) in your $PATH.

If the script does not find the executables, I suggest you manually configure them in the script.

Change your favorite text editor in the **xcb** script (here is the relevant section)

```
# Preferences
XC_MY_EDITOR="vim"
#XC_MY_EDITOR="nano"
```

### Versions

 - Update 29.02.2020:
  Removed the fuzzy finder requirement, file selection is via a bit of BASH code.

### Running xcb:

#### xcb workfile.bas outfile.prg

#### Main screen
```
    XC=Basic --- A 6502 BASIC Compiler
    (C) Csaba Fekete
    https://github.com/neilsf/XC-BASIC

    Executable paths:
    Assembler:  /home/user/bin/dasm
    Compiler:  /home/user/bin/xcbasic64
    Machine:  /home/user/bin/x64
    Editor:  /usr/bin/vim

    _W_ork File: workfile.bas

    _O_utput File: outfile.prg

    _E_dit    _R_un     _C_ompile _Q_uit

    Please select command >
```

In the above example screen, the ```_W_``` letters indicate reverse video (not shown here due to
markup limitations).

Selecting menu letter and hitting enter will run menu entry.

- W: change the work file name
- O: change the work file name (you have to enter this manually)
- E: edit the workfile.
- R: run the output file program (.prg)
- C: compiler the workfile.
- Q: quit program.

__BUGS__:

- No support for complex projects with multiple files. __Coming soon.__


Contact:  [mlongval@gmail.com](mlongval@gmail.com)


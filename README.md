# xcb
## Front-end for XC=Basic. In the style of TurboPascal 3.0

Csaba Fekete has written a really nice BASIC dialect compiler for the Commodore C64 8 bit
computer. ==> see [https://github.com/neilsf/XC-BASIC]

I wrote this little bash script as a front end to simplify the Edit/Compile/Run
loop. I based the look/function on TurboPascal 3.0 for CP/M --- I felt it
was appropriate for a compiler for an 8-bit computer.

This is a Beta 1.0 Version, so things may not work as expected.

Quick info: **xcb** will look for executables (dasm, xcbasic64, x64, text editor) in your $PATH.

If the script does not find the executables, I suggest you manually configure them in the script.

Change your favorite text editor in the **xcb** script (here is the relevant section)

```
# Preferences
XC_MY_EDITOR="vim"
#XC_MY_EDITOR="nano"
```

### Running xcb:

#### xcb workfile.bas outfile.prg

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

- W: change the work file name (you have to enter this manually)
- O: change the ouput file name (this currently runs the FZF fuzzy finder program to select the filename, this will change.)
- E: edit the workfile.
- R: run the output file program (.prg)
- C: compiler the workfile.
- Q: quit program.

__BUGS__:

- Currently no way to create a new basic (.BAS) file from inside __xcb__. You have to `touch` it
  from command line.
- No support for complex projects with multiple files. __Coming soon.__
- Needs "Fuzzy Finder" (fzf) to select basic (.BAS) file. This is not a bug, but I want to replace
  it with another way to select files.


Contact:  [mlongval@gmail.com](mlongval@gmail.com)


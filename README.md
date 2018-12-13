# Overview

A boilerplate D project with a single dependency.  The goal is to make an easy to get started a debuggable VSCode project for idiots like me who don't want to hang around on Dlang forums and get yelled at for not figuring out crap by osmosis.  Instead of reading a bunch of stuff try out these simple steps.  Ideally you are working on a real platform like ChromeOS.  Kidding, grab windows, OS X, or a real power Linux like Arch Linux.

## References

- VSCode : http://code.visualstudio.com
- Code-D for VSCode: https://marketplace.visualstudio.com/items?itemName=webfreak.code-d
- Compilers: You need one.  Get one.  https://dlang.org/download.html
- Debuggers: https://wiki.dlang.org/Debuggers
- Native Code debug extension for VSCode: https://github.com/WebFreak001/code-debug
- https://code.dlang.org/packages/antlr-d

## Getting Started With VSCode

Follow these bullet proof steps:

* Install a compiler.  I recommend LDC2 but whatever is fine.  Make sure it's in your path and also make sure dub is in your path.
* Install VSCode
* Install webfreak-code-d ("D Programming Language" extension from WebFreak).  Please wait for this to install.  It might take some time.
* (Optional) Install Native Debug extension for VSCode (from WebFreak)
* I don't recommend to install the code-d Beta extension.  The previous module installed should handle everything you need.  The instructions provided in the README for webfreak-code-d are a bit confusing on this point.
* Install the official C/C++ extension from Microsoft.  This gets you a debugger.
* At this point you should have everything.  I've never gotten this to work in the first pass.  A previous installation of Code-d or something might have failed.  In my case, I had my DCD settings botched up from a previously failed or disabled installation, meaning the path to DCD did not exists.  If you get a weird error like: can't find code-d command, make sure that the dcd-client.exe is in the right location that is configured in the File->Preferences->Settings for DCD client and server paths.
* To build: ctrl-shift-b.  Select build.
* To run: ctrl-shift-b.  Select run (name of your exe)
* To debug, you need to do a few more things.  Edit your .vscode/launch.json (in the project).  You can edit the various launch configurations here.  This is confusing to me because a ton of launch configurations.  I'm not an expert on this.  However, the simplest thing to do is list your binary exe name in the right place.  Obviously for Linux vs OS X or Win, you might need some different launch configurations.
* To debug: (1) click the Debug icon, (2) Select a run configuration, (3) and then click |> run.  If you have set breakpoints, great.  Otherwise, the program will run and possibly exit.  Set some variables or expressions too.

A picture to prove that I got this working: ![Image of a mad person trying to use D in an IDE](https://user-images.githubusercontent.com/64202/49914801-86a69f80-fe47-11e8-942e-9b2eb10d6b8d.PNG)

## Design

TODO

## Building

- dub build --compiler=ldc2 (use compiler flag in case you also have DMD in the path)

## Running

TODO
## Testing

Currently tested on:

```
LDC - the LLVM D compiler (1.7.0git-07b7abe):
  based on DMD v2.077.1 and LLVM 5.0.1
  built with LDC - the LLVM D compiler (1.6.0)
  Default target: x86_64-pc-windows-msvc
  Host CPU: nehalem
```

- run: dub test --compiler=ldc2

## Known Issues

- TBD

## TODO

- initial commits
- project plan
- recruit more devs

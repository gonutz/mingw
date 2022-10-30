This repo contains MinGW in 32 and 64 bit versions.

The GCC version is 7.3.0.

You can use this repo as a Git submodule to allow Windows users of your software
to easily build your C/C++ project without additional downloads.
Include a `build.bat` or a `make.bat` in your project and in it, prepend your
submodule MinGW's `bin` folder to the `PATH` like this:

	setlocal
	set PATH=mingw\mingw32\bin;%PATH%
	gcc ...

Prepending it, rather than appending it, makes sure that our own MinGW tools are
used when building, not other tools of the same name that are on the `PATH` as
well.

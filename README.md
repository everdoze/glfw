# GLFW

## Introduction

GLFW is a free, Open Source, multi-platform library for OpenGL and OpenGL ES
application development.  It provides a simple, platform-independent API for
creating windows and contexts, reading input, handling events, etc.

Version 3.1.2 is _not yet described_.

If you are new to GLFW, you may find the
[introductory tutorial](http://www.glfw.org/docs/latest/quick.html) for GLFW
3 useful.  If you have used GLFW 2 in the past, there is a
[transition guide](http://www.glfw.org/docs/latest/moving.html) for moving to
the GLFW 3 API.

Note that a number of source files have been added or renamed in 3.1, which may
require you to update any custom build files you have.


## Compiling GLFW

See the [Compiling GLFW](http://www.glfw.org/docs/latest/compile.html) guide in
the GLFW documentation.


## Using GLFW

See the
[Building programs that use GLFW](http://www.glfw.org/docs/latest/build.html)
guide in the GLFW documentation.


## Reporting bugs

Bugs are reported to our [issue tracker](https://github.com/glfw/glfw/issues).
Please always include the name and version of the OS where the bug occurs and
the version of GLFW used.  If you have cloned it, include the commit ID used.

If it's a build issue, please also include the build log and the name and
version of your development environment.

If it's a context creation issue, please also include the make and model of your
graphics card and the version of your driver.

This will help both us and other people experiencing the same bug.


## Dependencies

GLFW bundles a number of dependencies in the `deps/` directory.

 - [Khronos extension headers](https://www.opengl.org/registry/) for API
   extension symbols used by GLFW
 - [getopt\_port](https://github.com/kimgr/getopt_port/) for examples
   with command-line options
 - [TinyCThread](https://github.com/tinycthread/tinycthread) for threaded
   examples
 - An OpenGL 3.2 core loader generated by
   [glad](https://github.com/Dav1dde/glad) for examples using modern OpenGL


## Changelog

 - Changed minimum required CMake version to 2.8.12
 - Bugfix: Initialization failed on headless systems
 - Bugfix: The cached current context could get out of sync
 - [Win32] Renamed hybrid GPU override compile-time option to
           `_GLFW_USE_HYBRID_HPG` and added support for AMD PowerXpress systems
 - [Win32] Bugfix: `glfwGetVideoModes` included unusable modes on some systems
 - [Cocoa] Bugfix: The cached `NSScreen` for a monitor could get out of sync
 - [Cocoa] Bugfix: The `GLFW_AUTO_ICONIFY` window hint was ignored
 - [Cocoa] Bugfix: Resizing a window to its minimum size would segfault
 - [Cocoa] Bugfix: Creating or showing a window would make its context current
 - [X11] Bugfix: `glfwInit` would segfault on systems without RandR
 - [X11] Bugfix: The response to `_NET_WM_PING` was sent to the wrong window
 - [X11] Bugfix: Character input via XIM did not work in many cases
 - [X11] Bugfix: No fallback existed for missing `_NET_ACTIVE_WINDOW` support
 - [X11] Bugfix: Some significant window focus events were ignored
 - [WGL] Removed `GLFW_USE_DWM_SWAP_INTERVAL` compile-time option
 - [WGL] Bugfix: Swap interval was ignored when DWM was enabled
 - [GLX] Added dependency on `libdl` on systems where it provides `dlopen`
 - [GLX] Removed `_GLFW_HAS_GLXGETPROCADDRESS*` and `_GLFW_HAS_DLOPEN`
         compile-time options


## Contact

The official website for GLFW is [glfw.org](http://www.glfw.org/).  There you
can find the latest version of GLFW, as well as news, documentation and other
information about the project.

If you have questions related to the use of GLFW, we have a
[support forum](https://sourceforge.net/p/glfw/discussion/247562/), and the IRC
channel `#glfw` on [Freenode](http://freenode.net/).

If you have a bug to report, a patch to submit or a feature you'd like to
request, please file it in the
[issue tracker](https://github.com/glfw/glfw/issues) on GitHub.

Finally, if you're interested in helping out with the development of GLFW or
porting it to your favorite platform, join us on GitHub or IRC.


## Acknowledgements

GLFW exists because people around the world donated their time and lent their
skills.

 - Bobyshev Alexander
 - artblanc
 - arturo
 - Matt Arsenault
 - Keith Bauer
 - John Bartholomew
 - Niklas Behrens
 - Niklas Bergström
 - Doug Binks
 - blanco
 - Martin Capitanio
 - Chi-kwan Chan
 - Lambert Clara
 - Andrew Corrigan
 - Noel Cower
 - Jarrod Davis
 - Olivier Delannoy
 - Paul R. Deppe
 - Michael Dickens
 - Jonathan Dummer
 - Ralph Eastwood
 - Siavash Eliasi
 - Michael Fogleman
 - Gerald Franz
 - GeO4d
 - Marcus Geelnard
 - Eloi Marín Gratacós
 - Stefan Gustavson
 - Sylvain Hellegouarch
 - Matthew Henry
 - heromyth
 - Lucas Hinderberger
 - Paul Holden
 - Toni Jovanoski
 - Arseny Kapoulkine
 - Osman Keskin
 - Cameron King
 - Peter Knut
 - Eric Larson
 - Robin Leffmann
 - Glenn Lewis
 - Shane Liesegang
 - Дмитри Малышев
 - Martins Mozeiko
 - Tristam MacDonald
 - Hans Mackowiak
 - Kyle McDonald
 - David Medlock
 - Bryce Mehring
 - Jonathan Mercier
 - Marcel Metz
 - Jonathan Miller
 - Kenneth Miller
 - Bruce Mitchener
 - Jack Moffitt
 - Jeff Molofee
 - Jon Morton
 - Pierre Moulon
 - Julian Møller
 - Kamil Nowakowski
 - Ozzy
 - Andri Pálsson
 - Peoro
 - Braden Pellett
 - Arturo J. Pérez
 - Emmanuel Gil Peyrot
 - Cyril Pichard
 - Pieroman
 - Jorge Rodriguez
 - Ed Ropple
 - Aleksey Rybalkin
 - Riku Salminen
 - Brandon Schaefer
 - Sebastian Schuberth
 - Matt Sealey
 - SephiRok
 - Steve Sexton
 - Systemcluster
 - Dmitri Shuralyov
 - Daniel Skorupski
 - Bradley Smith
 - Julian Squires
 - Johannes Stein
 - Justin Stoecker
 - Elviss Strazdins
 - Nathan Sweet
 - TTK-Bandit
 - Sergey Tikhomirov
 - A. Tombs
 - Samuli Tuomola
 - urraka
 - Jari Vetoniemi
 - Ricardo Vieira
 - Simon Voordouw
 - Torsten Walluhn
 - Patrick Walton
 - Jay Weisskopf
 - Frank Wille
 - yuriks
 - Santi Zupancic
 - Jonas Ådahl
 - Lasse Öörni
 - All the unmentioned and anonymous contributors in the GLFW community, for bug
   reports, patches, feedback, testing and encouragement


# The Toolbox for the HDLC Daemon (hdlcd-tools)
Additional tools to be used together with the "HDLC Daemon" (HDLCd).

This package offers additional tools to be used together with the "HDLC Daemon" (HDLCd) that implements the
"High-level Data Link Control" protocol (HDLC). The HDLC-Daemon can be found here:
- https://github.com/Strunzdesign/hdlcd

This software is intended to be portable and makes use of the boost libraries. It was tested on GNU/Linux (GCC toolchain)
and Microsoft Windows (nuwen MinGW).

Stable releases of the HDLCd-Tools:
- v1.1 from 06.10.2016
  - Multiple bug fixes and stability improvements
  - Makes use of git submodules for "externals"

- v1.0 from 23.08.2016
  - First tested version without any open issues
  - Works well with s-net(r) BASE release 3.6

Current state:
- v1.2pre (git master branch)

Required libraries and tools:
- GCC, the only tested compiler collection thus far (tested: GCC 4.9.3, GCC 6.1)
- Boost, a platform-independent toolkit for development of C++ applications
- CMake, the build system
- Doxygen, for development
- nuwen MinGW, to compile the software on Microsoft Windows (tested: 13.4, 14.0)

See online doxygen documentation at http://strunzdesign.github.io/hdlcd-tools/

<a id="top"></a>

# Developing ApprovalTests.cpp on Windows



<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Contents**

- [Prerequisites](#prerequisites)
- [Dependencies](#dependencies)
- [Visual Studio 2017 Community Edition](#visual-studio-2017-community-edition)
  - [Use CMake to generate Visual Studio 2017 configuration](#use-cmake-to-generate-visual-studio-2017-configuration)
- [CLion](#clion)
  - [Use CLion with Visual Studio installed](#use-clion-with-visual-studio-installed)
  - [Run CLion with cygwin as toolset](#run-clion-with-cygwin-as-toolset)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Prerequisites

* CMake 3.8 or higher
* A C++11 or above compiler to use the library
* A C++17 or above compiler to run the project's own tests

## Dependencies

* A version of Catch2 is included in the source - see [lib/Catch.hpp](lib/Catch.hpp)
* Source code for the Google Test framework - version 1.8.1 - is downloaded automatically when CMake is run - see [CMakeLists.txt.in](CMakeLists.txt.in), and is then built when the project is built.

## Visual Studio 2017 Community Edition

### Use CMake to generate Visual Studio 2017 configuration

Decide where to put the build files that CMake will generate.
In the following, we're putting the output in `cmake-build-vs` - that location is already ignored by git.

1. Open a Command window
2. Then run:

		cd ApprovalTests.cpp
		mkdir cmake-build-vs
		cd    cmake-build-vs
		cmake -G "Visual Studio 15 2017" ..

## CLion

### Use CLion with Visual Studio installed

* Follow the instructions for experimental support of [Microsoft Visual C++ compiler](https://www.jetbrains.com/help/clion/quick-tutorial-on-configuring-clion-on-windows.html)
* Output is put in `cmake-build-debug`
* Tested with Visual Studio 2017
* **Major limitation**: Debugging is not yet supported by CLion, when compiling with Visual Studio, as of CLion 2017.3.3

### Run CLion with cygwin as toolset

* Code builds fine
* Tests run fine
* Reporters run fine
# Starter C89/C90 CMake Project

This project is intended to get you started with a project written in original C, also known as ANSI C89 or ISO/IEC C90. [(More information here)](https://en.wikipedia.org/wiki/ANSI_C#C89).

To make things a little more cross-platformy, we use the tool *CMake*.

CMake allows one to generate project files that will help you build with [many compilers](https://cmake.org/cmake/help/latest/manual/cmake-compile-features.7.html#supported-compilers) and [many build tools + IDEs](https://cmake.org/cmake/help/latest/manual/cmake-generators.7.html).

**Note:** I only tested this project on Windows and Ubuntu. CMake should take care of other commonly-used platforms. If you run into any issues, let me know.

## Pre-requisites
1. Some kind of build tool + compiler that CMake supports. Recommendations: [Visual Studio Community 2022](https://visualstudio.microsoft.com/) for Windows, or `sudo apt-get update && sudo apt-get install build-essential` for Debian-based linux distros (Ubuntu included).
2. [CMake download and installation](https://cmake.org/download/), `apt-get` on Debian-based linux distros may work for cmake as well but note that it's an old version (still works for this project)

## When you are intializing the project for the first time, do this:

Run:
```
mkdir build
cd build
cmake ..
```

Check the build folder. You should now have project files in it.

If you are on Windows and using Visual Studio, open the "StarterProject.sln" file with Visual Studio. Then in the Solution Explorer, right click on the StarterProject project, and choose "Set as startup project". Then, using the top menu, navigate to Debug → Start Without Debugging (if you use debugging, the program will terminate so quickly you won't even be able to see it).

If you are on Linux and using build-essentials/make, in the build directory run:
```
make
./StarterProject
```

For all platforms and tools, keep an eye out for the build output. If the build succeeds, you should see the output of "Hello world!".

## Each time you modify a source/header file, and are ready to build and test, do this:

Save your file.

If using Windows+Visual Studio, navigate to Debug → Start Without Debugging.

If using Linux+build-essentials/make, in the build folder run:
```
make
./StarterProject
```

## Each time you add or delete a new source/header file, do this:

Ensure that you are adding the file straight to the directory structure on your computer (it's easier to do this in VSCode than it is to do in Visual Studio because the folders you see there are "filters", not real folders).

After the file has been added, edit "CMakeLists.txt" and add your file to the `set(headers <...>)` or `set(sources <...>)` depending on whether your file is a *.h or *.c respectively. Keep it in alphabetical order!

Save the CMakeLists.txt file.

`cd` to your build folder if not already there, and run:
```
cmake ..
```
An alternative approach to run cmake: build the ZERO_CHECK project if you in Visual Studio.

You may now continue with builing and testing.

If using Windows+Visual Studio, navigate to Debug → Start Without Debugging.

If using Linux+build-essentials/make, in the build folder run:
```
make
./StarterProject
```
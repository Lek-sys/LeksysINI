/===============================================================================================================\
|                   _         _                  _   ___ _   _ ___ ____                                         |
|                  | |    ___| | _____ _   _ ___( ) |_ _| \ | |_ _|  _ \ __ _ _ __ ___  ___ _ __                |
|                  | |   / _ \ |/ / __| | | / __|/   | ||  \| || || |_) / _` | '__/ __|/ _ \ '__|               |
|                  | |__|  __/   <\__ \ |_| \__ \    | || |\  || ||  __/ (_| | |  \__ \  __/ |                  |
|                  |_____\___|_|\_\___/\__, |___/   |___|_| \_|___|_|   \__,_|_|  |___/\___|_|                  |
|                                      |___/                                                                    |
|                                                                                             by Borovik Alexey |
\===============================================================================================================/

Crossplatform all-in-one INI-file parser, written on C++ with STL

|---------------------------------------------------------------------------------------------------------------|
| Advantages                                                                                                    |
|---------------------------------------------------------------------------------------------------------------|

• Residents in single file - iniparser.hpp. Simply include it to your project and use
• Crossplatform (Windows & POSIX)
• Nice and easy-to-use C++ interface
• Extends standart INI interface with: 
  -> Arrays (comma-separated values) support
  -> Nested sections [parent.child] support
  -> File includes (;#include <file_path>)
• Can be used to save and load any user-defined classes, as long as stream operators are provided
• Supports multilines
• Loads & saves comments
• MIT license

|---------------------------------------------------------------------------------------------------------------|
| Usage                                                                                                         |
|---------------------------------------------------------------------------------------------------------------|

Include provided iniparser.hpp to your C++ project and that is all
Usage information can be found on project's GitHub page
Look in test_app.cpp for different ways of using Leksys' IniParser
For testing purposes you can compile provided test application (see next section)

|---------------------------------------------------------------------------------------------------------------|
| Building Test Application                                                                                     |
|---------------------------------------------------------------------------------------------------------------|
You need to install CMake before building test_app
CMake binary for your platform can be found at: 
http://www.cmake.org/cmake/resources/software.html

1. POSIX (Linux, QNX, FreeBSD, MacOS)
In console type:
# mkdir build; cd build
# cmake <this_file_dir>
# make

2. Windows
Use cmake-gui application for building project files for your
IDE (currently supported: Visual Studio, Borland C++, CodeBlocks (MinGW), Eclipse (MinGW)).

Under QtCreator (v. 2.2.1) you can open Cmake projects directly from the
IDE (File -> Open Project)

Alternatively, if you want to build project for Visual Studio, you can 
do it directly from the console in true-Linux style =):

# mkdir build; cd build
# cmake <this_file_dir>
# %VS90COMNTOOLS%\vsvars32.bat
# nmake

Note, that if you have Visual Studio 10.0 (2010) environment variable will
be %VS100COMNTOOLS% and so on.

|---------------------------------------------------------------------------------------------------------------|
| Running Test Application                                                                                      |
|---------------------------------------------------------------------------------------------------------------|
1. Simply start application and ensure, that 10 first tests pass.
2. Start application with parameters: 
   -i <this_file_dir>/ini-test/test1.ini -o out_file.ini
   and ensure that file <application_dir>/out_file.ini contains all the stuff from ini files in test directory
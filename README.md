# fuzzy_lib

Visual Studio Solution to build [ssdeep](https://ssdeep-project.github.io/ssdeep/index.html)'s static libraries, or fuzzy.lib both on x86 and x64. By linking the created library to a VS Project, functions from ssdeep become available.

## Usage

The procedure below is supposed to be gone through on Visual Studio 2019, on which the solution was created.

### Build Library

Open fuzzy_lib.sln and Build solution for the desired platform. fuzzy.lib will be created at the path below.
* x86
  * fuzzy_lib\Release\fuzzy.lib
* x64
  * fuzzy_lib\x64\Release\fuzzy.lib

### Link Library to VS Solution

Create a new project to use fuzzy.lib, either into the fuzzy_lib solution or a newly created one. So that fuzzy.lib be linked to the project, it's required to modify the following settings in the project property for the target platform.
* Configuration Properties >> C/C++ >> Additional Include Directories
  * Path to the folder under which fuzzy.h is located
* Configuration Properties >> Linker >> Input >> Additional Dependencies
  * Path to the fuzzy.lib

## Sample

The sample code of using this library is posted at https://9ood4nothin9.blogspot.com/2019/12/usage-example-of-fuzzylib-on-visual.html

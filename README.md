# A simple Win32 extension for Python

## Introduction

This is a just a quick-and-dirty example of a simple Python native extension on Windows for my personal reference. The lessons learned here will be used for my Python Onyx32 extension. It is mostly based on [documentation from Microsoft](https://docs.microsoft.com/en-us/visualstudio/python/working-with-c-cpp-python-in-visual-studio?view=vs-2019#alternative-approaches).

## Using this repo

To run this repo, you'll need:

* Install VS Community 2019 with "Desktop Development with C++" and "Python development" workloads.
  * With the Python workload, you'll need _miniconda_ (for creating a virtual environment), _Python native development tools_, and a Python 3 64-bit environment.
  * Make note of where VS installs your Python environment (on my machine, VS installed Python into _A:\Program Files (x86)\Microsoft Visual Studio\Shared\Python37_64_).
* Set the build to x64 and configuration to Release when opening the Solution.
* Create an x64 Python 3 environment named `env` in VS under _PythonExtension_ project > _Python Environments_.
* In the _superfast_ project's properties, you'll also need to:
  * Update _VC++ Directories_ > _Include Directories_ to the location of your Python installation's (as per above) include folder.
  * Update _Linker_ > _Additional Library Directories_ to the location of your Python installation's lib folder.

## Useful resources

* [Python/C API reference.](https://docs.python.org/3/c-api/)

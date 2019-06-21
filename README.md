# python-win-extension

This is a just a quick-and-dirty example of Python native extension on Windows for my personal reference. The lessons learned here will be used for my Python Onyx32 extension.

## Using

This extension was based on [documentation from Microsoft](https://docs.microsoft.com/en-us/visualstudio/python/working-with-c-cpp-python-in-visual-studio?view=vs-2019#alternative-approaches). To run this repo, you'll need:

* VS Community 2019 with "Desktop Development with C++" and "Python development" workloads. With the Python workload, you'll need _miniconda_, _Python native development tools_, and a Python 3 64-bit environment. Make note of where VS installs your Python environment (on my machine, VS installed Python into _A:\Program Files (x86)\Microsoft Visual Studio\Shared\Python37_64_).
* Set the build to x64 and configuration to Release when opening the Solution.
* In the superfast project properties, you'll also need to:
  * Update _VC++ Directories_ > _Include Directories_ to your location of your Python installation include folder.
  * Update _Linker_ > _Additional Library Directories_ to the location of your Python installation lib folder.

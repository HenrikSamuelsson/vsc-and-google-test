# VSC and Google Test

Repro to do a quick test run of Google Test in Visual Studio Code.

This test is based on this [answer](https://stackoverflow.com/a/62911654/686720) on StackOverflow.

Cmake tried to build using Visual Studio compiler but this did not succeed. Visual Studio compiler seems more or less useless if not using Visual Studio to develop.

Found this [answer](https://stackoverflow.com/a/4101496/686720) on StackOverflow on how to get CMake to build with MinGW on Windows. Assuming that MinGW is installed on the Windows machine.

The following terminal commands made it possible to run the tests:

```txt
cmake -G "MinGW Makefiles"
mingw32-make.exe all
.\my_tests.exe
```
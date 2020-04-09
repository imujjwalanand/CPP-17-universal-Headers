1. Open Spotlight search (kudos if you have Alfred), paste the path ```/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/include/c++/v1```
2. Create a directory named **bits** you might need super admin privilege for this, and then paste the file present in the repo in there. 
3. Make sure your clang is updated to the latest version then run the following command to compile your .cpp files in the C++17 compiler ```g++ -std=c++1z code.cpp```
4. Here, the flag to be used is ```c++1z``` instead of ```c++17``` as Apple LLVM version 9.0.0 (clang-900.0.39.2) (which ships with Xcode 9.2) does not support the usage of the flag ```-std=c++17``` since its too old. In order to compile your program with ```c++17``` support using the compiler which comes with Xcode 9.2 you need to use the ```-std=c++1z``` flag.
Xcode 9.3 will be shipped with Apple LLVM version 9.1.0 (clang-902.0.30) which has support for the ```-std=c++17 flag```. Which as of today, is not available.


**Adios and Stay Home!**

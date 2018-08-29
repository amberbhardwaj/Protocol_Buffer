# Protocol_Buffer
Protocol buffer solution for Visual Studio 2012 (Win10)

I am using official version of protocol buffer (3.5.1). To build the protobuf, i slightly modified the CmakeLists.txt file.

I was facing issue while building using "VS2012 x86 Native Command Line tool" So i used VS2012 to build the entire solution 
and it worked fine.

Errors
======
To resolve error related to gtest or gmock, just disable BUILD_TEST macro. Or if you want to test then download gtest also. 


Generating VS Solution
======================

You need to modify the command which is given in Cmake/Readme.md at line 128 based on the version of Visual Studio. 

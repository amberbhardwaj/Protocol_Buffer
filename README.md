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

Comparing sizes of protobuf vs json
https://nilsmagnus.github.io/post/proto-json-sizes/

Faster than normal xml. 

How does it work?
Compress the data into binary stream which is highly compressed and faster.
Message-> encoder->decoder->message

-----------------
Advantages:
-----------------
	1. Lightweight less space
	2. Automatic data validation
	3. Faster due to smaller in size
	4. Decoding is faster than encoding 
	5. You can serialize data using any programming language

--------------------------------------------
JSON Parsing vs Protobuf Parsing
--------------------------------------------

Technique	     |  ITR	     |  Protocol Buffer		    |    JSON	
Encoding 	     |  1000000	     |  3816ms (262055 enc/s)	    |    3207ms (311818 enc/s)	
Decoding	     |  1000000	     |  1447ms (691085 dec/s)	    |    2659ms (376081 dec/s)	
Encoding + Decoding  |  1000000	     |  4922ms (203169 enc+dec/sec) |    6844ms (146113 enc+dec/s)	
				
				

------------------------------
Standard working way
------------------------------
Proto file -> generate code (any language) -> create object -> serialize data (using encoding/ Decoding)

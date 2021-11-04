Title: No strtoul in C#
Date: 2011-05-26 08:41
Category: programming
Tags: csharp, til
Authors: Bhargav Bhat
Summary: TIL about the lack of a clean `strtoul` library function in C# that can infer base of the input string

Off late, I've been supporting a legacy C#/WinForms application written to configure the look-and-feel of a OpenGL/GLES based 3D rendering engine, which itself is written in C++. While the rendering engine and learning OpenGL itself remains my primary focus, this problem with C# was rather interesting. 

### C++ and `strtoul`

The [`strtoul`](https://www.cplusplus.com/reference/cstdlib/strtoul/) library function in C++ is very very useful for dealing with numbers in multiple bases and converting between them. When the `radix` (aka `base`) parameter is passed in as `0`, this function determines the input base automatically and returns the result in base-10. Therefore, the below line:

	#!c
	int x = strtoul("0xa", NULL, 0);

... will set `x` to the value `10` (since hex `A` is `10` decimal) The problem at hand required a similar library function in C#.

### The Search and The Solution

MS [ToUInt32](https://docs.microsoft.com/en-us/dotnet/api/system.convert.touint32) docs don't really have much to say on this topic, they're mostly concerned with converting between `float`s and integers rather than integers of different bases. Not finding what I need in MS docs or elsewhere, I posted a question on [StackOverflow](https://stackoverflow.com/questions/6080065/strtoul-equivalent-in-c-sharp) and the following solution was suggested:
	
	#!csharp
	return text.StartsWith("0x") ? Convert.ToUInt32(text.Substring(2), 16)
	                             : Convert.ToUInt32(text, 10);

While not as elegant as the C++ way, this will do for now. Just before I wrote this note and shared with everyone, an unlikely alternative was found by a colleague in the discussion posted [here](https://bytes.com/topic/c-sharp/answers/226729-easy-hex-string-0x1234-integer-conversion). However, I'm yet to try this out and I do not fully understand the implications of passing in the `NumberStyles` enum and the kind of numbers it might end up picking up as valid. On the surface, I don't see anything obviously wrong/off here.

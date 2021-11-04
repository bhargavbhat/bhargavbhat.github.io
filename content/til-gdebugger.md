Title: gDebugger
Date: 2013-02-16 19:52
Category: programming
Tags: opengl, debugging
Authors: Bhargav Bhat
Summary: TIL about gDebugger Tool

Debugging OpenGL/GLES calls is an pretty challenging and there is almost next to nothing for debugging shaders. Today, I came across [gDebugger](http://www.gremedy.com/) developed by Graphics Remedy that allows programmers to do debug OpenGL/GLES applications in a more traditional way. It also has tools for profiling and measuring performance. Key Features of this tool are:

- Texture & Buffers viewer : allows you to look at loaded textures and contents of front/back/depth buffers etc
- Break on GL Error : stop code execution on encountering an OpenGL error
- Properties & State View : displays state variables and arguments/properties passed into various `gl` Functions
- Performance Profiling Features, such as
	
	- Call Statistics : shows percentage time and number of calls made to `gl` Functions
	- State Change Stats : shows number of irrelevant/redundant state changes made in the code
	- Performance Graphs : shows frame rate & other relevant info like CPU/GPU utilization, mem utilization etc


Although not exactly as full-fledged and featureful as `gdb` or Visual Studio, it is really a big leap forward and the profiling features are pretty helpful. :)

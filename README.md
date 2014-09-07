#MSBuild.NugetContentRestore
MSBuild task to restore Nuget content files to project folder

##Introduction

##Download
To install MSBuild.NugetContentRestore, run the following command in the Package Manager Console:
    
	PM> Install-Package MSBuild.NugetContentRestore
	
More information about MSBuild.NugetContentRestore NuGet Package available at https://www.nuget.org/packages/MSBuild.NugetContentRestore/

##Usage
After installing MSBuild.NugetContentRestore using NuGet, your Visual Studio Project (.csproj, .vbproj) will have a reference to MSBuild.NugetContentRestore Task. The only remaining step is to use it. Here is an example of how (and when) I use it. Edit your project file so it looks something like this:

	<Target Name="BeforeBuild">
	  <NugetContentRestoreTask SolutionDir="$(SolutionDir)" ProjectDir="$(ProjectDir)" />
	</Target>

All NuGet Packages Content Folders will be copied to your project folder right before is built.

##License
The MIT License (MIT)

Copyright (c) 2014, Francisco Lopez

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
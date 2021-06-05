---
title: "/Fo (Object file name)"
description: "Reference guide to the Microsoft C++ /Fo (Object file name) compiler option in Visual Studio."
ms.date: "04/20/2020"
f1_keywords: ["/Fo", "VC.Project.VCCLCompilerTool.ObjectFile", "VC.Project.VCCLWCECompilerTool.ObjectFile"]
helpviewer_keywords: ["Fo compiler option [C++]", "object files, naming", "/Fo compiler option [C++]", "-Fo compiler option [C++]"]
ms.assetid: 0e6d593e-4e7f-4990-9e6e-92e1dcbcf6e6
---
# /Fo (Object File Name)

Specifies an object (*`.obj`*) file name or directory to be used instead of the default.

## Syntax

> **`/Fo`**_pathname_

## Remarks

You can use the **`/Fo`** compiler option to set an output directory for all the object files generated by the CL compiler command. Or, you can use it to rename a single object file.

By default, the object files generated by the compiler are placed in the current directory. They're given the base name of the source file and a *`.obj`* extension.

To use the **`/Fo`** option to rename an object file, specify the output filename as the *pathname* argument. When you rename an object file, you can use any name and extension you want, but the recommended convention is to use *`.obj`*. The compiler generates command line error D8036 if you specify a filename to **`/Fo`** when you've specified more than one source file to compile.

To use the **`/Fo`** option to set an output directory for all object files created by the CL command, specify the directory as the *pathname* argument. A directory is indicated by a trailing slash in the *pathname* argument. The specified directory must exist; it's not created automatically.

## Example

The following command line creates an object file named *sample.obj* in an existing directory, *\\intermediate*, on drive D.

```cmd
CL /Fo"D:\intermediate\" /EHsc /c sample.cpp
```

## Set the option in Visual Studio or programmatically

### To set this compiler option in the Visual Studio development environment

1. Open the project's **Property Pages** dialog box. For details, see [Set C++ compiler and build properties in Visual Studio](../working-with-project-properties.md).

1. Select the **Configuration Properties** > **C/C++** > **Output Files** property page.

1. Modify the **Object File Name** property to set the output directory. In the IDE, the object file must have an extension of *`.obj`*.

### To set this compiler option programmatically

- See <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.ObjectFile%2A>.

## See also

[Output-File (/F) Options](output-file-f-options.md)<br/>
[MSVC Compiler Options](compiler-options.md)<br/>
[MSVC Compiler Command-Line Syntax](compiler-command-line-syntax.md)<br/>
[Specifying the Pathname](specifying-the-pathname.md)
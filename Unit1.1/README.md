# Checking The .NET Installation

This short tutorial will help you check you have the .NET SDK and F# installed correctly.

# Checking the SDK Version

To check you have the latest SDK installed correction open a command prompt and navigate to this directory (`cd unit1.1`).

Type the following command:

```
dotnet --version
```

You should see the following output:

```
7.0.101
```

# Checking F# Interactive

To check F# interactive works correctly create a file called `helloworld.fsx` and add the following contents:

```F#
printfn "Hello, world!"
```

Execute this using the following command:

```
dotnet fsi helloworld.fsx
```

You should see the following output:

```
Hello, world!
```

# Checking The F# Compiler

To check the F# compiler works correctly, first create a new F# project:

```
dotnet new console --language "F#"
```

This should create two new files:

```
Program.fs
Unit1.1.fsproj
```

The file `Program.fs` contains F# source code. By default it has the following content:

```F#
// For more information see https://aka.ms/fsharp-console-apps
printfn "Hello from F#"
```

The file `Unit1.1.fsproj` contains the instruction to the F# compiler about how to build the project.

To get the F# compiler to create a .NET assembly for use the following command:

```
dotnet build
```

You should see output something like:

```
MSBuild version 17.4.0+18d5aef85 for .NET
  Determining projects to restore...
  All projects are up-to-date for restore.
  Unit1.1 -> c:\code\AlgosupFSharp2023\Unit1.1\bin\Debug\net7.0\Unit1.1.dll

Build succeeded.
    0 Warning(s)
    0 Error(s)
```

To run the code in your assembly you can use the following command:

```
dotnet bin\Debug\net7.0\Unit1.1.dll
```

You will see the following output:

```
Hello from F#
```

It's often practical to build and run the assembly in one set, you can do this using the following command:

```
dotnet run
```

You will see the following output:

```
Hello from F#
```

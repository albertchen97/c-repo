# Description

A repository of C source code files while learning C programming.

# Table of Content

- [Configuration](#Configuration)
    - [Environment](#Environment)
    - [Toolset](#Toolset)
    - [Use Developer Command Prompt for VS 2019 to Run cl.exe](#Use%20Developer%20Command%20Prompt%20for%20VS%202019%20to%20Run%20cl.exe)
        - [Open Developer Command Prompt for VS 2019](#Open%20Developer%20Command%20Prompt%20for%20VS%202019)
        - [Compile *.c File Using cl.exe](#Compile%20*.c%20File%20Using%20cl.exe)
# Configuration

The content below specifies how to set up the necessary software environment to compile and run the source code in this repository.

## Environment

- System: Windows 10

- IDE/Text Editor: Visual Studio 2019 & Visual Studio Code

    - You MUST have Visual Studio installed since it contains all the tools we need to compile C source code.
    - Visual Studio Code is not required but recommended.
    
        - I use Visual Studio Code as my code editor because it is more handy for me to work with small projects. 
        
        - Visual Studio IDE is too heavy and has lots of features that are useless for my current project scale.

## Toolset

1. **Developer Command Prompt for Visual Studio**
    - If you have Visual Studio installed, you should have this one.

        *(To install Visual Studio 2019: https://visualstudio.microsoft.com/downloads/#other)*

2. Visual Studio Workload - **C++ Build Tools**
    - This workload contains the tool **cl.exe**.
        - cl.exe is a tool that controls the Microsoft C++ (MSVC) C and C++ *compilers* and *linkers*.
        - Note: cl.exe can be run *ONLY* on operating systems that support Microsoft Visual Studio for Windows. 

        *(To install C++ Build Tools: https://code.visualstudio.com/docs/cpp/config-msvc)*

## Use Developer Command Prompt for VS 2019 to Run cl.exe

You can start this tool **ONLY** from a *Developer Command Prompt for Visual Studio 2019*.

### Open Developer Command Prompt for VS 2019

- Approach No.1 - Through Windows Menu (Simplest Way)

    1. Simply search in the Windows menu: "developer command prompt".
    2. The full name should be "*Developer Command Prompt for VS 2019*".
    3. The opened terminal by default is under the directory "*%PATH%\Microsoft Visual Studio\2019\Community*". This is pre-set by Visual Studio.
    4. You can use *cd* command to go to your working directory.

- Approach No.2 - Open In Visual Studio Code (*Recommended*)

    1. Install the *C/C++ extension for VS Code* by Microsoft.
        - Search extension "C/C++" and install the extension provided by Microsoft.
        - Or, install via: https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools
    2. Configure your VS Code *settings.json*: add the following lines
        
        *(Please substitude the paths with your own paths)*
        
            // Set the integrated shell to Commmand Prompt.
            "terminal.integrated.shell.windows": "C:\\Windows\\System32\\cmd.exe",

            // Run the batch script to run Developer Command Prompt for VS 2019 (To Compile C/C++).
            // The option "/K" means "Keep", it tells CMD.exe to run the command and then keep the window open.
            // If you do not use "/K" option you will get back to the original CMD interface.
            "terminal.integrated.shellArgs.windows": ["/K", "C:\\Microsoft Visual Studio\\2019\\Community\\Common7\\Tools\\VsDevCmd.bat"],

            // Open the terminal in current working directory (cwd)
            "terminal.integrated.cwd": "${cwd}",

    3. In VS Code folder explorer sidebar, right click your *.c file, select "Open in Integrated Terminal". Then you will have the Developer Command Prompt for VS 2019 opened under the directory that contains your *.c file.

## Compile *.c File Using cl.exe

- To compile *main.c*:

        cl main.c

    - Your directory should have two files added: *main.obj* and *main.exe*.

- To run *main.exe*:

        main


*-----------------This is the end of README------------*






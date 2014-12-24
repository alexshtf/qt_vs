QT Build customizations for Visual Studio
=========================================
The files in this repository are useful to compile QT UI form files, and run QT Meta Object Compiler on your header files containing `QObject`s.

Usage
=====
First you need to put all the files in this repository on a sub-folder of your choice. Please also ensure that you have a `QT_DIR` environment variable (or user macro) that points to your QT directory.

Before using for the first time on a project, you need to do the following steps:

1. Right click on a project, select **Build dependencies --> Build customizations**.
2. Click on **Find existing** and select the `qt.targets` file.

To compile a form file, add it to your project and then:

1. Right-click on the form file and select **Properties**
2. Under **Item type** choose **Qt UIC**
3. The output will be, by default, compiled to `$(INTDIR)\uic\FILE.EXT.h`. You can `#include` this file in your code and use it.

To run QT MOC on your header file:

1. Right click on the header file and select **Properties**
2. Under **Item type** choose **Qt MOC**

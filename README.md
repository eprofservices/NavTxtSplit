# Microsoft Dynamics NAV Tool

## NAV txt export split

The tool splits TXT file exported from Microsoft Dynamics NAV into separate files.

Can be useful for C/AL developers who want to put changed objects source code into some version control system - git, subversion or anything else. The VCS works better having objects in separate files rather than one big file with all of them. The other advantage of such approach is possibility to export only changed objects, split the export file and make git commit. The split is making the character set conversion additionally.

To use it first export all NAV objects (or part of them that was modified) into one TXT file and then split it using the tool into separate files each containing one object. 

The output file names are standardized. For example "Codeunit 1.txt" for OBJECT Codeunit 1 ApplicationManagement.

The binary exports are not supported.

Written in C the tool was originally developed in 2006. Tested with NAV version 3.7, 4.0, 5.0, 6.0 (objects version). It should work with newer versions unless the txt export format has changed fundamentally.

To build the tool use standard C compiler like gcc and optionally the make utility.

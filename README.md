# Microsoft Dynamics NAV Tool

## NAV txt export split

The tool splits TXT file exported from Microsoft Dynamics NAV into separate files.

Can be useful for C/AL developers who want to put changed objects source into some version control system - git, subversion or anything else. The VCS works better having objects in separate files rather than one big file with all of them. The other advantege of such approach is possibility to export only changed objects, split the export file and make git commit. The split is making the character set conversion additionaly.

To use it first export all NAV objects (or part of them that was modified) into one TXT file and then split it using the tool into separate files each containing one object. 

The output file names are standarized. For example "Codeunit 1.txt" for OBJECT Codeunit 1 ApplicationManagement.

The binary exports are not supported.

Written in C the version was originaly developed in 2006. 

# PythonCABOOSE
A CABOOSE is a Controller Application Bundle for Object-Oriented Software Engineering. The primary processing hub for this application is a "general-purpose" controller (GPC) which can be adapted for use on the web (WWW) or can be used with a command-line interface (CLI). This GPC holds the most common-case of controller processing for all model view controller (MVC) applications. The only portion of a CABOOSE system which must be written each time, except the storyboard itself, is the special-purpose processing which populates the "#HOTSPOTS#" in the markup-language templates found among the pages within the StoryBoard directory. These behaviors are placed in the cab.py file co-located in the same directory as caboose.py. 

CABOOSE systems work by dynamically calling upon the behaviors that fill in the "hotspots" in the storyboard as needed. Yet, this Python instance of CABOOSE supports an "ICEMODE" in which one can call upon "logic" statically frozen in a fixed switching structure, in icemode.py. This file is built by a "simple-minded" code generator, icy.py, when one calls the iceman batch file.

One can execute this simple prototype application from the MS-DOS CLI using the "run" batch file.

run home  - will display the home page
run landing - will dispaly the langing page
run error - will display the error page
run ANYTHING_ELSE - will display the error page since the ANYTHING_ELSE view is not defined

The codebase is rather simple and self-documenting.

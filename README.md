# PythonCABOOSE

A CABOOSE is a Controller Application Bundle for Object-Oriented Software Engineering. The primary processing hub for this application is a "general-purpose" controller (GPC) which can be adapted for use on the web (WWW) or can be used with a command-line interface (CLI). This GPC holds the most common-case of controller processing for all model view controller (MVC) applications. The only portion of a CABOOSE system which must be written each time, except the storyboard itself, is the special-purpose processing which populates the "#HOTSPOTS#" in the markup-language templates found among the pages within the StoryBoard directory. These behaviors are placed in the cab.py file co-located in the same directory as caboose.py. 

CABOOSE systems work by dynamically calling upon the behaviors that fill in the "hotspots" in the storyboard as needed. Yet, this Python instance of CABOOSE supports an "ICEMODE" in which one can call upon "logic" statically frozen in a fixed switching structure, in icemode.py. This file is built by a "simple-minded" code generator, icy.py, when one calls the iceman batch file.

One can execute this simple prototype application from the MS-DOS CLI using the "run" batch file.

[run home  - will display the home page]

[run landing - will dispaly the langing page]

[run error - will display the error page]

[run ANYTHING_ELSE - will display the error page since the ANYTHING_ELSE view is not defined]

The codebase is rather simple and self-documenting.

Modification - 01.10.2021:

Version of Python ICE produced for Microsoft Internet Information Service (IIS) in (*.zip) archive (Python ICE).

It is somewhat robust, in that, it checks for the presence of the "cab" and "icemode" imports where appropriate. The (*.py) file "cab" must be present within the default user-defined import directory in each CABOOSE installation. This file is the controller application bundle and holds all of the app-specific functionally which supports the general-purpose behavior of the controller found in the (*.py) file "caboose". By default, the CABOOSE system relies upon dynamic invocation for calling upon the user-defined subroutines found in its "cab" import. That is unless the "cab' import defines a global ICEMODE. When "False", the default dynamic behavior of the CABOOSE is utilized. When "True", this is overridden, and the CABOOSE system looks for a "frozen" instance of the logic found in the Architectural Control Language (ACL) file called "directory.scsv". The "frozen" instance of this logic, rendered in Python, is found in a user-defined module called "icemode". This is auto-generated by another Python script called "icy" when the MS-DOS batch file "icemode" is run.

This might seem somewhat convoluted; however, it greatly simplifies the construction of a model-view-controller system by providing a well-ordered partitioning of "view" and "behavioral" concerns plus work roles.

So, when a team builds a "web-based" system with this controller pattern at its core, it must follow the steps below. It is a "multi-cycle" process. It CYCLE A-C is verified and validated properly, CYCLE D should be a moot seeing that the web application should be "correct by construction".

CYCLE A:

Front-End Developers:

I.    Build a complete "static" HTML-storyboard.
II.   Integrate its parts.
III.  Verify it internally.
IV.   Validate it with the client.

Upon approval:

CYCLE B:

I.    Identify any content which should be dynamic.
II.   Assign each portion of content a unique user-defined placeholder, such as #E-MAIL#.

Front-End Developers:

FE-III.   Replace any content which should be dynamic with user-defined placeholders.
FE-IV.    Reintegrate the annotated storyboard's parts.
FE-V.     Verify it internally.
FE-VI.    Validate it with the client.

Back-End Developers:

BE-III.   Build packages of invokable methods which will replace placeholders with appropriate dynamic content. 
BE-IV.    Follow a "sensible" naming convention for these methods based upon the placeholders they will replace.
BE-V.     Unit test methods.
BE-VI.    Verify internally.
BE-VII.   Validate with the client.

Integrator:

IR-I.     Build the mapping file based on the requirements document produced when identifying the dynamic content and defining the placeholders. This will represent an "architectural control language" (ACL) file in eXtensible Markup Language (XML) or a Segmented Comma Separated Values (SCSV) format.
[ NOTE : The front-end, back-end, and integration work for CYCLE B work can be completed in parallel. ]

CYCLE C:

I.    Unite the annotated storyboard, packages of methods, and ACL file with the pre-written and reusable general-purpose controller pattern rendered in the appropriate language for the target platform and method bundles.

After this integration step:

II.   Verify the system internally.
III.  Validate the system with the client.

CYCLE D: ( Technically Optional )

I.   "Freeze" the "liquid" nature of the dynamic invocation through the use of an integration completion engine (ICE).
II.   Perform "final" verification.
III.  Perform "final" validation.

This is the In CaboosE (ICE) development methodology. It is outlined in an "informal" and somewhat "unprofessional" web-history found @ https://coderosetta.blogspot.com/2020/11/ 
This web chronicle describes a personal "hobbyist" project whose goal is producing the software pattern in fourteen popoular modern "high-level" languages, including the other LAMP languages: the Professional HyperText Processor (PHP) and the Programmatic Extraction and Report Langauge (PERL), C# on the .NET platform, JAVA for its Enterprise Edition servlets, JAVAScript for Node.js and TypeScript, Clojure, Go, Groovy, Ruby, Rust, and others.

A "full" web-based implementation in Python will probably occur first with subsequent ports. Although, a partial command-line interface (CLI) implemenation already exists in all of these langauges.

It should be mentioned that this approach was intially drawn from experiences with an IBM model 20 PC with dual-disk drives long before the days of Windows 3.1.1, Microsoft Foundation Classes, TCL/TK, Tkinter, Swing, C#, Python, JAVA, the WWW, Mozilla, Internet Explorer, Opera, Chrome, Tomcat, Glassfish, IIS, and, of course, Github! Thoughts of this type of system were intermingled with visions of "novel" concern partitioning techniques such as objects, actionable data types (ADTs), and object-flow systems plus other Turing-caliber ideas; some are commonplace these days, such as architecture for software and parameterized types (generics). 

The question asked at the time was "What is the most abstract, universal, and general partitioning of the concerns found among the text-based menu-driven systems written during a freshman Pascal course." This sparked the idempotent idea and terms "model-view-controller" and "layered" systems along with the intuitve notion that software development could be greatly simplified if the proper primitive and universal development patterns were found. It is a personal belief that a CABOOSE system is one of those. It does not require the use of the structural paradigms found in "modern" object- or aspect- orientation; tradtional structure is sufficient for building this software pattern. And, that was all that was available when this vision, along with objects and the rest, reached the forefront of this graying mind during the Spring of 1989.

![head](/assets/images/830x290.jpg)
Framework pik3d

#### PROCESSING AND 3D-DISPLAY OF MATRICES/FRAMES AND THEIR SEQUENCES

When exploring the properties of a time-varying surface, it is convenient
to store, process and display a set of images (frames/matrices) as a whole.
Such a sequence is called a STACK of images ( perhaps from one frame ).

The framework offers a data storage/exchange standard: __###-format__ and
base set of commands/utilities for processing and displaying stacks.
To convert matrix text to __###-format__ all you need to do is add a header:

    ### matrix_name [ m, n ] , where: m-number of rows, n-columns

A matrix element can be displayed as a point in 3D-space:
X - matrix row number, Y - column number, Z - element value.
The set of such 3D-points forms a 3D-surface.

        O_____j_______Y            |Z
        |     |     |              |
        |     |     |   ---3D-->   |  z=m[i,j]
        |     |     |              |   |
        i_____m[i,j]|             O|___|__y=j______
        |           |              /   |  /     / Y
        |           |             /    | /     /
        |___________|           x=i____|/     /
        |                       /            /
        X                      /____________/
                             X/

For text data you can use a shortened header: __###  []__ or even  __###[]__.
The number of columns is the number of values in the first row of data.
The number of rows is defined by the file length or the next header.

Rendering a surface with easy control of viewing angles, lighting, color, etc.
is the functionality of the command: __s3d -"Surface-3D"__. You can view
the stack in the "frame by frame" mode, like a video clip. During playback of the
video clip, you can stop it and change the viewing angles, colors, lighting and etc.

The surface can be displayed in two ways: "Smooth" and "bar-View" - a set of vertical
bars. You can switch the view by pressing &lt;F4> at any time.

Command: __b3d__ -"Body-3D" support 3D-display of bodies defined by
quadrilateral faces (up to 10,000 faces). You can control Opacity of body/surface.
2D/3D - Points| Lines| Body can be added to the 3D-scene.

Data processing supports __Eigen/Singular Values Decomposition__ of Matrix
and Regression analyses based on <a href='https://archive.apache.org/dist/commons/math/binaries/commons-math3-3.6.1-bin.zip'>"The Apache Commons Mathematics Library 3.61"</a>.

The framework has simple but effective 2D-graphics tools for displaying
columns and rows of matrices. Simple graph-editor can add text, lines, figures to chart.
2D-graphics can be saved in vector format: __WMF - "Microsoft Windows Meta File"__.
They scale well and can be used in MS Word documents, conveniently viewed using ACDSee
, Total Commander &lt;F3> ...

Framework commands are executable(.exe) modules and their set is not fixed.
The __launcher technology__ is used ("launch" - to launch, start, run). Launcher
encapsulates the starting configuration of the Java Virtual Machine.

The user does not encounter JAVA-programming anywhere( except expanding functionality ).
JAVA doesn't even need to be installed. Only unpack the JAVA installation archive in some folder.

The framework has simple tools to create a new command in JAVA, for example: __jj-Technology -"java-JAVA"__.
jj-command allows to compile/execute __.jj and .java files__. jj-file contains
only "subject part". File.java is generated from File.jj by adding header with import and main().
Generated file with framework class-path is submitted for execution to JAVA as "single source-file".
Intermediate files can be saved.

__jj-Technology supports macro substitution__ that allow you to modify java-code directly during jj-call.
For example: a code snippet can be inserted into the jj-file just before compilation.
For example this feature is used to find regression, i.e. set of functions for regression can be specified
__analytically in symbolic form directly in the command__, see: pik3d/demo/regression.

In addition, __jj__ can execute the __sequence of Java commands__ directly from the command line.
jj-command can use JVM options (see: pik3d/usr/jep438.jj - test of Vector API).

In a simple case, the processing program is a script (.bat, .cmd ...).
From command to command, data is transferred in the form of ###-files
or by means of __"pipe"__ (it can reduce disk usage and increase performance).
Any command can save the pipe-output to the file for further processing( add to command @file).

__jj-technology__ supports execution of OS-commands and pipe-lines.
This feature allows to use __jj-file__ as batch file with flexible control on JAVA !

Additional commands can be implemented in any other convenient algorithmic language.
To read/write ###-files in __PYTHON__: pik3d/ext/ __kadr.py package__ is included.
To read ###-files in the __ImageJ__ editor, ###_Reader_ImageJ.jar __plugin__ is implemented.

The framework can be installed on __Windows 7, 10, Linux__ (tested in Mint 21.1).
Current  version 23  is  compiled with __JAVA-21 LTS__ using __javaFX__. It can be run under __JAVA v. 21, 22__.

Description of the framework, formats and install procedure are presented in the file:
__pik3d_DOC.html__, contained in the install archives: __pik3d.zip__ and __pik3d_Linux.zip__.

To exchange large data ###-format includes __binary representation__.
__CSV-files__ can be converted to __###-format__.

![opacF4](/assets/images/OpacF4.jpg)
![polibo](/assets/images/plb2.jpg)
![4_view](/assets/images/4view.jpg)
![minMAJ](/assets/images/Regression.png)
![minMAJ](/assets/images/2dgra.png)

__download and install:__
  - at the top of this page click file: __pik3d.zip__ or __pik3d_Linux.zip__;
  - on the opened page on the right select download( ~ 1.2 MB );
  - unpack the archive into some folder;
  - click the file: __pik3d_DOC.html__ - it should be open by default browser;
  - read the section "INSTALL pik3d";
  - after install, scripts(_run.cmd) in demo folders are available to execute.
  - if you plan to use __Eigen/Singular Values Decomposition__, you need to dowload
    <a href='https://archive.apache.org/dist/commons/math/binaries/commons-math3-3.6.1-bin.zip'>The Apache Commons Mathematics Library 3.61</a>
	and place jar-file into the pik3d/lib folder (without sources and java-doc ~2.2MB).

<p>author: K.A.Ilyashenko, e-mail: kilyashenko@gmail.com</p>
Error messages, comments, suggestions  are welcome.

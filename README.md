![head](/assets/images/830x290.jpg)
Framework pik3d v.19.5

    PROCESSING AND 3D-DISPLAY OF MATRICES/FRAMES AND THEIR SEQUENCES

When exploring the properties of a time-varying surface, it is convenient
to store, process and display a set of images (frames/matrices) as a whole.
Such a sequence is called a STACK of images ( perhaps from one frame ).

The framework offers a data storage/exchange standard: ###-format and
base set of commands/utilities for processing and displaying stacks.
To convert matrix text to ###-format all you need to do is add a header:

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

Surface rendering with simple angle controls, lighting, color, etc.
constitutes the functionality of the command: s3d -"Surface-3D".
You can view the stack in the "frame by frame" mode, like a video clip.
During clip you can stop it and change the angles of view, colors, lighting.

The framework has simple but effective 2D-graphics tools for displaying
columns and rows of matrices. Simple graph-editor can add text, lines, figures to chart.
2D-graphics can be saved in vector format: WMF - "Windows Meta File".
They scale well and can be used in MS Word documents, conveniently viewed using ACDSee
, Total Commander<F3> ...

Framework commands are executable(.exe) modules and their set is not fixed.
The launcher technology is used ("launch" - to launch, start). Launcher
encapsulates the starting configuration of the Java Virtual Machine.

The user does not encounter JAVA-programming anywhere( except expanding functionality ).
JAVA doesn't even need to be installed. Only unpack the JAVA installation archive in some folder.

The framework has simple tools to create a new command in JAVA, for example: jj-Technology -"java-JAVA".
jj-command allows to compile/execute .jj and .java files. jj-file contains
only "subject part". File.java is generated by adding header with import and main().
Generated file with framework class-path is submitted for execution to JAVA as "single source-file".
Intermediate files can be saved.

In addition, jj-command can execute the sequence of Java commands directly from the command line.
jj-command can use JVM options (see: usr/jep438.jj -test of Vector API).

Additional commands can be implemented in any other convenient algorithmic language.
To read/write ###-files in PYTHON package: ext/kadr.py is included.
To read ###-format in the ImageJ editor, ext/###_Reader_ImageJ.jar plugin is implemented.

In a simple case, the processing program is a script (.bat, .cmd ...).
From command to command, data is transferred in the form of ###-format files
or by means of "pipe" (it can reduce disk usage and increase performance).

The framework can be installed on Windows 7, 10, Linux (tested in Mint 21.1).
Current version 19.5.7 is compiled with JAVA-21 using javaFX .

Description of the framework, formats and install procedure in the file:
pik3d_DOC.html (contained in the install archive: pik3d.zip).

To exchange large data ###-format includes binary data presentation.
In addition CSV-file can be convertrd to binary ###-format file.

![4_view](/assets/images/4view.jpg)
![minMAJ](/assets/images/2dgra.png)
To download and install:
  - at the top of this page click file: pik3d.zip or pik3d_Linux.zip;
  - on the opened page on the right select download( ~ 1MB );
  - unpack archive in some folder;
  - click the file: pik3d_DOC.html - it should open by default browser;
  - read the section "INSTALL pik3d";
  - after install, scripts(_run.cmd) in demo folders are available to execute.

<p>author: K.A. Ilyashenko, e-mail: kilyashenko@gmail.com</p>
Error messages, comments, suggestions  are  welcome.

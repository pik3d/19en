pik3d v.19.3 framework

    PROCESSING AND 3D-DISPLAY OF MATRICES/FRAMES AND THEIR SEQUENCES

When exploring the properties of a time-varying surface, it is convenient
to store, process and display a set of images (frames/matrices) as a whole.
Such a sequence is called a STACK of images (perhaps from one frame).

The framework offers a data storage/exchange standard: ###-format and
base set of commands for processing and displaying stacks.
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
During clip you can stop it and change the angle of view.

The framework has simple but effective 2D-graphics tools for displaying
rows and columns of matrices. 2D-graphics are saved in vector format:
WMF - "Windows Meta File". They scale well and can be used in MS Word
documents, conveniently viewed using ACDSee, Total Commander<F3> ...

Framework commands are executable(.exe) modules and their set is not fixed.
The launcher technology is used ("launch" - to launch, start). Launcher
encapsulates the starting configuration of the JAVA machine.

The user does not encounter JAVA anywhere. It doesn't even need to be installed.
It is enought to expand the JAVA installation archive in some folder.
Launchers find out its position through an environment variable.

The framework has simple tools for creating a new command in JAVA. Additional
commands can be implemented in any other convenient algorithmic language.

In a simple case, the processing program is a script ( .bat or .cmd).
From command to command, data is transferred in the form of ###-format files
or by means of "pipe"(this saves time and disk space).

The framework can be installed on Windows 7, 10.
Version 19.3 is compiled with JAVA-19 using javaFX .

Description of the framework, formats and install procedure in the file:
pik3d_DOC.html (contained in the install archive: pik3d.zip).

For reading the ###-format in the ImageJ editor, ###_Reader_ImageJ.jar plugin
is implemented. To read/write ###-matrices in PYTHON - package: kadr.py.

To download and install:
  - in the table (top of the page) click the file: pik3d.zip;
  - in the window that opens, on the right, click the button: Download (~ 1MB);
  - unpack the file: pik3d.zip in some folder;
  - click the file: pik3d_DOC.html - it should open in the default browser;
  - read the section "INSTALLING pik3d";
  - after install, scripts(_run.cmd) in demo folders are available to execute.

author: K.A. Ilyashenko, e-mail: kilyashenko@gmail.com
Error messages, comments, suggestions  are  welcome.

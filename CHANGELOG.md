.md pre.plaintext {
    line-height: 1.3em;
}

v.19.5.4,  14.07.2023 :
  - fix known bugs ;
  - commands: vic[s], lss, hist  commad keys:
    - syntax of window position/size: /x=v /y=v /w=v /h=v ;
    - syntax of use add.graphics: /add=file ;
    - vic[s] Logarithmic Axes are added: /lx, /ly, /lxy ;

  - jj: support short names functions: abs(v), hh(i,j)-header  and const: rad=180/pi ;

  - demo/2d-graph: new window with Log.Axes ;

  - pik3d_DOC.html:
    - bugs fixed ;
    - most used pik.io methods: added simple graphics methods ;
    - vic-cmd: new functionality: Log.Axes ;

v.19.5.5, 17.07.2023 : 
  - Fix bug in 2d-graph: show title with coordinates always visible .

v.19.5.6, 06.08.2023 :
  - added new helper commands:  ee [text] !time text  and  hhh Stk !Header of Stack ;

  - changed Stack creation: stk ii [jj=1 [kk=1]] [v=&lt;value>] [D8] ;

  - ALL commands process Float(F4) and Double(D8) input Stacks.
    Processing and result format depend on input Stack format ;

  - time-out while reading input Stack is removed, now you can wait a long time
    or stop: <Ctrl>+C;

  - revised section: "Rules for describing a subset of indices" ;
    - if you want a reference to the Last index (e.g. last frame), use 0 !
    - e.g. List of frames(the number of fr.= N): 2,1,0,-1 !fr.: 2,1, N, N-1 .

  - command: fmt -"convert to format" in the text output section is extended
    by user format ;

  - fixed bug in s3d cross-sections ^V ;

  - jj: is possible to store file.java in jj-repository: pik3d/usr,
    and start it without path:> jj file.java 

  - fixed some methods in libraries: pik.jar and cmd.jar ;
  - improoved description of some features in Help: pik3d_DOC.html .

v.19.5.7, 03.10.2023 :
  - correct and recompile Framework and jj-command with JAVA-21 ;
  - fix error (non stop warning timer) in Linux version of commands: vic, vics ;
  - improve some methods in pik.mat.java, pik.io.java ;
  - fix some bugs in pik3d_DOC.html .

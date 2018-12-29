#Project FEA2  
##The goal of the project is to build an open source general finite element solver.  
The basic inputs shall be a .msh file generated by Gmsh (http://gmsh.info/), a free 3D finite element mesh generator,  and a weak form of equation.  
As now it is written in Octave (https://www.gnu.org/software/octave/), an open source high-level language, primarily intended for numerical computations. It's syntax is very close to Matlab.  
The Project is slowly being ported to C++ and is using Armadillo (http://arma.sourceforge.net) and Gmsh (gmsh.info/) APIs.   
  
The Project is a work in progress.  
  
To compile the code, you need to download the latest Gmsh source code from gmsh.info/ and compile  by typing the following in your Gmsh build directory. This will build a static library of Gmsh.  

    cmake -DDEFAULT=0 -DENABLE_BUILD_LIB=1 -DENABLE_POST=1 -DENABLE_PARSER=1 <path gmsh source directory>
    make lib
    
Copy the libgmsh.a file generated to the folder Project-FEA2/Cpp/libGmshReader/GmshApi/  
Run the following command in your Project-FEA2 Build directory.

    cmake <path Project-FEA2/Cpp/ source directory>
    make
    
A new file Prj-FEA2 will be created

Run by typing

    ./Prj-FEA2
    Enter File Name: <path to .msh file>
    Enter Dimension: <Enter the Dimension you want to analyse>




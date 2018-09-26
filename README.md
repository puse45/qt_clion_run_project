# qt_clion_run_project
How to open and run qt project on clion ide.

**Requirements**
 
 - Clion
 - Qt5
 - Microsoft Visual Studio 2017 Community

**Installation**

* *Clion*
Download Clion [Download](https://www.jetbrains.com/clion/download/#section=windows)
  - Install

* *Qt5*
To Download use this link [Download](https://www.qt.io/download) select community edition.
  - Install
   - Select 
     - Qt 5.11.1
     - msvc2017_64
    

* *Microsoft Visual Studio 2017 Community*
Download from this link [Download](https://visualstudio.microsoft.com/downloads/)
  - Install

**Configure Clion IDE**

To configure native build environment for Clion follow the steps below.

`Toolchains`
 - Open Clion
 - Click File
 - Click Settings
 - Go to Build, Execution, Deployment
 - Click Toolchains
Under Environments ensure Visual Studio is the default native build environment
On the Architecture combo box select the suitable system byte type.


**Run Application**

`Clone the above project` 
Open Project on clion ide
Under CMakeLists.txt file Change path to where your Qt Cmake file is located i.e. 
    
        set (CMAKE_PREFIX_PATH "C:/Qt5/5.11.1/msvc2017_64/lib/cmake")
    
 - Build project
 - Run project
 
 You will see a Debug directory created at project root.
 - Click start menu
 - Goto Qt folder click
 - Find Qt 5.11.1 64-bit for Desktop open 
 - cd to where Debug dir is 
 - Pass this command (for more info [Link](http://doc.qt.io/qt-5/windows-deployment.html))
    
        windeployqt --plugindir plugins .

It will help copy all required/need dynamic Qt libraries (.dll) 
 
Run Application again on clion.
 
 
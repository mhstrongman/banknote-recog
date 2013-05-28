Bank-note Recog
===============

This is an IME-USP master's programme project for MAC5768 - Computer Vision and Image Processing. Our goal is to build an Android application to recognize Brazilian bank notes. The project must be built on top of OpenCV and Android SDK.

Ubuntu/Debian Installation instructions
=======================================

Open CV
-------

Please read http://docs.opencv.org/doc/tutorials/introduction/linux_install/linux_install.html for detailed instructions on how to install OpenCV on Linux. The following is a cut-down version of that guide.

Install the following packages:

    sudo apt-get install build-essential
    sudo apt-get install cmake
    sudo apt-get install pkg-config
    sudo apt-get install libgtk2.0-dev
    sudo apt-get install libavformat-dev
    sudo apt-get install libavcodec-dev
    sudo apt-get install libswscale-dev
    sudo apt-get install ffmpeg

Then download OpenCV's source code from http://sourceforge.net/projects/opencvlibrary/. Unpack it and enter the directory where the source code is.

For example, if you unpacked it in your home directory, do

    cd ~/opencv-2.4.5

Now you should create a directory for cmake build files, and then call cmake:

    mkdir release
    cd release
    cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local ..

And finally call make to build OpenCV:

    make
    sudo make install

Eclipse
-------

Install Eclipse CDT.

Compiling and Building the Project
----------------------------------

First get the source code of this project at https://github.com/igortopcin/banknote-recog
Then open Eclipse and choose "Import...", then "Import existing project into workspace". Follow the remaining steps and you should have a copy of the project working in your Eclipse.

Performa full build by selecting Project >> "Build All" or "Build Project". This should output all build files in a directory called "Debug". Do the following to run the application:

    cd Debug
    ./banknote-recog ../img/10_1.jpg ../img/img4.jpg
    
The "img" folder has some sample images to test the application.


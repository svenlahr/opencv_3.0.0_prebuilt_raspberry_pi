These two files are cherry-picked from OpenCV version 3.0.0, which was compiled and built from source on a Raspberry Pi 2B.
They have been successfully tested on both that Pi 2B and a Pi Zero, both running Raspbian Stretch Lite (with Java added).
NB that these are specifically for Java applications that are based on OpenCV, and depending on how you are using OpenCV you may need to (apt-get) install other libraries to make it work.

NB also that these files in no way need to be "installed" on your Pi, you should just put them in a known location and point them out as run-time dependencies to your Java application.

Example: your Java program is built as a JAR file, let's call it "sampleprog.jar", and your main class is "com.example.ComputerVisionApplication". Let's assume that the opencv .jar and .so files are put in the folder ./opencv_libs.
Then you would start your program with the following command:

java -Djava.library.path=opencv_lib -cp opencv_lib/opencv-300.jar:sampleprog.jar com.example.ComputerVisionApplication

All credits for this work go, of course, to the amazing creators of OpenCV.

https://opencv.org/

For any questions about licensing or otherwise, I refer you https://opencv.org/license.html .


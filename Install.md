# **THIS PAGE IS NO LONGER MAINTAINED, PLEASE GO TO https://github.com/pmudry/gdx2d FOR AN UP TO DATE VERSION** #


# Installing the library #
The library consists of two Eclipse projects that can be imported easily. Once downloaded, an archive can be imported using `File->Import->Existing project into workspace`. You can then either give the path of the archive or extract the data manually and then point to that directory.

## gdx2d-desktop ##
This project contains the library as well as all the demo programs. All the demos can be run on PC or on Android. In order to run a demo, either use the DemoSelector class which provides a simple way to choose which demo to run. You can also run each demo individually.

## gdx2d-android ##
This is the Android counterpart of the library. This project **depends** on the `gdx2d-desktop` project, which means that this other project must be available in Eclipse. In addition, most of the files that will be executed come from that project as well. As such, it mainly consists of a Java file `GameActivity.java` which determines which is the main program that will be launched on Android.
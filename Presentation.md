**gdx2d** is a game and application framework which is multi-platform. It is Java based with the heavy-lifting done in native code (i.e. C/C++), for example for physics rendering.

The advantage of using **gdx2d** is that you can develop your code in Java on your standard desktop computer like any other Java application and then deploy the same code, with a single click, on an Android phone or tablet. Of course, you have to take into consideration the fact that some of your code is a bit different for Android (for instance, you do not have accelerometers on your PC).

The library itself is a wrapper around a very very nice library called [libgdx](http://code.google.com/libgdx) which provides almost everything to the library.

## gdx2d vs libgdx, what is the difference ? ##


quote from http://alexdorokhov-wiki-libgdx.googlecode.com/git/TheArchitecture.wiki

> "_As game developers we are in need of a couple of system components that allow us to create the game of our dreams:_

  * An **application framework** that handles the main loop and life cycle (creation, pausing, resuming, destruction) of our application.
  * A **graphics module** that provides us with a way to draw things to the screen
  * An **audio module** to playback music and sound effects
  * An **input module** to receive user input from the mouse, keyboard, touch screen, accelerometer and so on and so forth.
  * A **file I/O** module to read and write data like textures, maps or configuration files.

Libgdx contains modules that map directly to the above list of requirements. For each module there exist one or more Java interfaces that are implemented for each platform. These implementations are called backends. Currently there's a desktop backend, an applet backend and an Android backend.

As a programmer you don't care which backend you are actually working with. You will only work with the public interfaces each backend implements. The only platform specific code you'll ever have to write with libgdx is the instantiation of a concrete Application implementation, e.g. one for the desktop and one for Android. So, here's a silly little diagram:

![http://libgdx.googlecode.com/svn/wiki/libgdx-overview.png](http://libgdx.googlecode.com/svn/wiki/libgdx-overview.png)

> The names in this diagram are actually the names of the public   interfaces that you will work with when writting a libgdx based application. The Application is responsible for managing each sub-module. There can only ever be a single Application as well as a single instance of all the sub-modules.  Let's have a closer look at the different modules.
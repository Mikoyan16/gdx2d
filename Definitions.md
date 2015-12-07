# **THIS PAGE IS NO LONGER MAINTAINED, PLEASE GO TO https://github.com/pmudry/gdx2d FOR AN UP TO DATE VERSION** #


# Definition of physics terms #

  * _World_: Manages the physics simulation. It knows everything about the overall coordinate space and also stores lists of every element in the world. The world has the gravity. To get an instance from every class, you can use PhysicsWorld.getInstance();

  * _Body_: Serves as the primary element in the Box2D world. It has a location. It has a velocity. You can apply forces to it (to make it move for example)

  * _Shape_: Keeps track of all the necessary collision geometry attached to a body.

  * _Fixture_: Attaches a shape to a body and sets properties such as density, friction, and restitution.

  * _Joint_: Acts as a connection between two bodies (or between one body and the world itself).

# Handling user input #

_tap_: A user touches the screen and lifts the finger again. The finger must not move outside a specified square area around the initial touch position for a tap to be registered. Multiple consecutive taps will be detected if the user performs taps within a specified time interval.

_pan_: A user drags a finger across the screen. The detector will report the current touch coordinates as well as the delta between the current and previous touch positions. Useful to implement camera panning in 2D.

_fling_: A user dragged the finger across the screen, then lifted it. Useful to implement swipe gestures.

_zoom_: A user places two fingers on the screen and moves them together/apart. The detector will report both the initial and current distance between fingers in pixels. Useful to implement camera zooming.

_pinch_: Similar to zoom. The detector will report the initial and current finger positions instead of the distance. Useful to implement camera zooming and more sophisticated gestures such as rotation.
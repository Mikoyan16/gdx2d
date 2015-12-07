# **THIS PAGE IS NO LONGER MAINTAINED, PLEASE GO TO https://github.com/pmudry/gdx2d FOR AN UP TO DATE VERSION** #


# Planned improvements for release 1.0 #

## New demos ##
  * Appropriate demo for scene rendering with a list
  * New demos for joints in physics with appropriate constructor
  * Add subcategories in the demo selector application (to separate a bit things)

## Physics ##
  * See if using `isLocked` is not a viable alternative to synchronized for world physics
  * See if possible to use BodyBuilder to improve things or remove it
  * Wrap physics world into another object which should also provide a `getCurrentStep` method
  * Finish refactoring of physics constants in a class

## Graphics ##
  * Improve font rendering
  * Multiple screens
  * Relocate the images that are used in `GdxGraphics.java` into another   resource directory
  * Provide a function for display images with modified alpha
  * Determine which calls of begin / end are really required
  * Automatic registration of objects in scene rendering through the use of interfaces

## Documentation ##
  * Document the fact that we are using other libraries
  * Document the scene rendering approach


---


# Planned improvements for release 1.1 #

## Graphics ##
  * Sprite sheets support
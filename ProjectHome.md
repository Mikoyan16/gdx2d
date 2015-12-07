# **THIS PAGE IS NO LONGER MAINTAINED, PLEASE GO TO https://github.com/pmudry/gdx2d FOR AN UP TO DATE VERSION** #

# What is `gdx2d`? #
Is it a simple to use Java framework for writing 2D games or applications that look like this:

![https://gdx2d.googlecode.com/files/multi_screenshot.png](https://gdx2d.googlecode.com/files/multi_screenshot.png)

# Why this framework? #
It is multi-platform so that you can run your code on desktop computers (running either Windows, Linux or Mac) but also on mobile devices running Android. It is based on [libgdx](https://code.google.com/p/libgdx/) but provides a much simpler interface and multiple demo programs to get started.

Using the framework, this displays a shrinking/growing circle
```
package hevs.gdx2d.demos.simple;

import com.badlogic.gdx.graphics.Color;

import hevs.gdx2d.lib.GdxGraphics;
import hevs.gdx2d.lib.PortableApplication;

/**
 * A very simple demonstration on how to display something animated with the library
 * @author Pierre-André Mudry (mui)
 */
public class DemoSimpleAnimation extends PortableApplication {
	int radius = 5, speed = 1;
	
	public DemoSimpleAnimation(boolean onAndroid) {
		super(onAndroid);
	}

	public void onInit() {
		// Sets the window title
		setTitle("Simple demo, mui 2013");
	}

	public void onGraphicRender(GdxGraphics g) {		
		
		// Clears the screen
		g.clear();
		g.drawFilledCircle(g.getScreenWidth()/2, g.getScreenHeight()/2, radius, Color.BLUE);		

		// Update the circle radius
		if (radius >= 50|| radius <= 3)
			speed *= -1;

		radius += speed;
		
		g.drawSchoolLogo();
	}

	public static void main(String[] args) {
		/**
		 * Note that the constructor parameter is used to determine if running on Android or not.
		 * As we are in main there, it means we are on desktop computer.
		 */
		new DemoSimpleAnimation(false);
	}
}
```

as depicted here <a href='http://www.youtube.com/watch?feature=player_embedded&v=WYmqRDnV1CE' target='_blank'><img src='http://img.youtube.com/vi/WYmqRDnV1CE/0.jpg' width='256' height=268 /></a>

# Who did this and why? #
It was developped for the [inf1 course](http://inf1.begincoding.net) given at [HES-SO Valais / Systems engineering](http://www.hevs.ch) by Pierre-André Mudry (mui@hevs.ch). The framework was written P.-A. Mudry & N. Chatton with the help of C. Métrailler.

# Screenshots and executable demo program #
You can find many screenshots of what the library is up to on the [Screenshots](Screenshots.md) page. An easy to run demo in `jar` is also available there https://gdx2d.googlecode.com/files/gdx2d_demos_0.9.2.jar.

# More info? #
Let's have a look at the development [wiki](TOC.md).
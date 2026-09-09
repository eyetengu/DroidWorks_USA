# DroidWorks_USA
A robotics learning platform for people familiar with mcus and ros2 but looking for an organized system for integrating both.

Welcome.
This is DroidWorks U.S.A.
I am building a working, modular droid platform in public — sensors, microcontrollers, ROS2, displays, and eventually a full R2-style chassis — and I am documenting every step so that anyone who wants to follow along can actually do it.
The goal is simple: create a clean, upgradable sensor and control foundation that can grow into a functional droid without having to throw everything away and start over every time something better comes along.

How the lessons are organized
Everything is broken into Lesson Sets. Each set builds on the one before it, but the pieces stay modular on purpose.

**Lesson Set 1 – Basic Sensors**
Individual sensors first.
-PIR
-RCWL
-Motion fusion
-Ultrasonic
-Time-of-Flight
-Distance fusion
-State nodes (motion and distance)

You learn one sensor at a time, get clean ROS2 topics out of it, and end up with simple state information the rest of the system can use.

**Lesson Set 2 – Display**
The OLED.

Once the state nodes exist, the display just listens. It does not care whether the data is coming from a single sensor or an array. That is intentional.

**Lesson Set 3 – Sensor Arrays**
Take the same sensors and run them as arrays.

The OLED and the state nodes stay the same. You only change the sensor layer. That is the whole point of the modular design.
Each individual lesson subset gets its own plain text document. No fluff. Just the steps, the wiring, the sketch, the ROS2 node, and what you should see when it works.

**What this is (and what it is not)**
This is a working laboratory notebook made public.

It is not a polished course with perfect production values.

It is not a finished commercial product.

It is the actual process of building something real, documented as it happens, so that the next person can move faster and make fewer of the same mistakes.
I am building this so that it can eventually support me, my dog, and the work I want to keep doing. That means the lessons have to be useful, the modules have to be reusable, and the whole system has to be something people can actually learn from and build on.
If you are here to follow along, start with Lesson Set 1.

If you are here to watch the process, the updates will keep coming.

**Let’s build.**

# DroidWorks U.S.A.

**A modular, teachable path from Arduino/ESP microcontrollers into ROS 2 — built in public toward a functional R2-style droid.**

This is a working laboratory notebook made public.

I am building a clean, upgradable sensor and control foundation (sensors → MCU → ROS 2 topics → state → display → arrays → eventually chassis and behavior) and documenting every step so that anyone who wants to follow along can actually do it.

The goal is simple: create modules that stay reusable so you never have to throw everything away when something better comes along.

---

## What this is (and what it is not)

**This is:**
- A public build log and teaching system
- A set of reproducible, modular lessons
- The foundation for a real droid platform
- Work that is intended to become a sustainable income stream

**This is not:**
- A polished, finished commercial course
- A complete R2 droid (yet)
- A “buy this kit and you’re done” product

It is the actual process of building something real, documented as it happens.

---

## How the lessons are organized

Everything is broken into **Lesson Sets**. Each set builds on the one before it, but the pieces stay modular on purpose.

### Lesson Set 01 – Basic Sensors
Individual sensors first, then fusion, then simple state.
- PIR
- RCWL-0516
- Motion fusion
- Ultrasonic
- Time-of-Flight
- Distance fusion
- State nodes (motion and distance)

You learn one sensor at a time, get clean ROS 2 topics out of it, and end up with simple state information the rest of the system can use.

### Lesson Set 02 – Display
The OLED.

Once the state nodes exist, the display just listens. It does not care whether the data is coming from a single sensor or an array. That is intentional.

### Lesson Set 03 – Sensor Arrays
Take the same sensors and run them as arrays on a single MCU.

The OLED and the state nodes stay the same. You only change the sensor layer. That is the whole point of the modular design.

---

## Design rules (locked)

- MCU sketches use `millis()` only — no blocking `delay()` in the main loop
- Clean, state-change serial output (easy for ROS 2 to parse)
- Preferred topic names:
  - `/pir_state`
  - `/rcwl_state`
  - `/fused_motion`
- State and display layers must not need rework when the sensor layer is upgraded
- Every lesson is self-contained: wiring, sketch, ROS node, and what “success” looks like

---

## Current status (as of Sept 2026)

| Area                        | Status                          |
|----------------------------|---------------------------------|
| Lesson Set 01 structure    | In place                        |
| Individual sensor modules  | Partially complete              |
| Combined PIR + RCWL (Set 03) | Working sketch + ROS 2 package |
| OLED (Set 02)              | Started                         |
| Full state layer           | In progress                     |
| Chassis / actuators        | Not started                     |

The combined PIR + RCWL package (`droidworks_sensors`) is the most complete working example right now.

---

## How to start

1. Read the [Course Overview](LESSON_PLAN/00_Course_Overview)
2. Set up the ROS 2 workspace (see Lesson Plan)
3. Begin with **Lesson Set 01 → 01_PIR_Serial**

If you just want to see something working quickly, look at the combined motion module in Lesson Set 03.

---

## Repository layout
DroidWorks_USA/
├── LESSON_PLAN/           # High-level overview and workspace setup
├── Lesson_Set_01/         # Individual sensors + fusion + state
├── Lesson_Set_02/         # OLED
├── Lesson_Set_03/         # Sensor arrays on single MCU
└── nano_droid.png


---

## Why this exists

I am building this so that it can eventually support me, my dog, and the work I want to keep doing.

That means the lessons have to be useful, the modules have to be reusable, and the whole system has to be something people can actually learn from and build on.

If you are here to follow along — start with Lesson Set 01.

If you are here to watch the process — the updates will keep coming.

**Let’s build.**

---

*Maintained by Eric Young*  
*GitHub: [eyetengu/DroidWorks_USA](https://github.com/eyetengu/DroidWorks_USA)*

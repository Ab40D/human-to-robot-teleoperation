# HUMAN-TO-ROBOT TELEOPERATION

### Translating Human Motion into Controlled Robot Movement.

<p align="center">
  <strong>From Human Motion to Robot Joint Commands.</strong>
</p>

<p align="center">
  An experimental computer-vision-based teleoperation pipeline exploring how human body movements can be translated into constrained joint-level targets for a simulated humanoid robot.
</p>

<p align="center">
  <a href="https://www.youtube.com/shorts/3mJpDJhb-xg">
    <img src="https://img.shields.io/badge/▶_WATCH_DEMO-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch Demo"/>
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Domain-Robotics-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/Computer_Vision-Motion_Tracking-purple?style=flat-square"/>
  <img src="https://img.shields.io/badge/Control-Teleoperation-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Status-Experimental-orange?style=flat-square"/>
</p>

---

## 🧠 The Problem

A camera can capture human movement. However, translating that movement into reliable robot commands is a much more complex engineering challenge.

Human motion is continuous, flexible, and unpredictable. Robot joints operate within defined mechanical limits and require controlled, valid targets.

The challenge is not simply tracking a person. It is deciding how their movements should be interpreted, constrained, and translated into robot motion.

## 🎯 Project Overview

This project explores a **Human-to-Robot Teleoperation Pipeline** that converts an operator's body and hand movements into joint-level targets for a simulated humanoid.

The main focus is the intermediate control layer between human motion estimation and robot actuation.

Rather than directly copying every tracked movement, the system investigates how to produce controlled and predictable robot commands.

## ⚙️ Core Engineering Concepts

- **Motion Tracking:** Capturing human upper-body and hand movements through a camera.
- **Joint Constraints:** Keeping generated targets within defined joint boundaries.
- **Motion Limits:** Restricting movement to controlled ranges.
- **Tracking Validity:** Evaluating whether tracking information is reliable enough to use.
- **Calibration:** Establishing the relationship between human movement and robot reference positions.
- **Command Hold Logic:** Holding the previous valid target when tracking information should not be passed through.

## 🏗️ Conceptual Pipeline

```text
       HUMAN OPERATOR
              |
              v
       CAMERA INPUT
              |
              v
       MOTION ESTIMATION
              |
              v
       TRACKING VALIDATION
              |
              v
          CALIBRATION
              |
              v
      MOTION MAPPING
              |
              v
      JOINT CONSTRAINTS
              |
              v
       COMMAND VALIDATION
              |
              v
       HUMANOID SIMULATOR
```

The pipeline separates human motion estimation from robot command generation, allowing the control logic to be evaluated independently.

## 🦾 Initial Scope: Upper-Body Teleoperation

The first experiment focuses on upper-body movement.

This decision was made because the current testing environment does not provide enough physical space for reliable full-body tracking.

The initial scope provides an opportunity to investigate:

- Upper-body movement mapping.
- Arm and hand motion interpretation.
- Joint-level target generation.
- Motion boundary handling.
- Tracking loss and invalid-data behavior.

## 🧪 Current Development Status

<sub>Experimental prototype — simulated environment.</sub>

| Component | Scope |
|---|---|
| Camera-based motion input | Experimental |
| Upper-body tracking | Initial implementation |
| Motion-to-joint mapping | Experimental |
| Joint constraints | Control pipeline focus |
| Tracking validation | Control pipeline focus |
| Command hold behavior | Control pipeline focus |
| Humanoid simulation | Current demonstration |
| Full-body tracking | Future work |
| Physical robot integration | Not yet validated |

## 🚧 Limitations

This project is not an autonomous robot, an autopilot, or a complete humanoid control system.

It is an experimental teleoperation command pipeline designed to investigate the translation of human movement into constrained robot joint targets.

The current demonstration operates with a simulated humanoid. No physical robot integration is claimed.

## 🗺️ Roadmap

- [x] Establish the human-to-robot teleoperation concept.
- [x] Develop an initial upper-body demonstration.
- [x] Connect tracked movement to a simulated humanoid.
- [ ] Improve calibration and motion mapping.
- [ ] Refine tracking validity and command-hold behavior.
- [ ] Test full-body tracking in a larger environment.
- [ ] Investigate more advanced motion constraints.
- [ ] Explore physical humanoid integration.

## 🎥 Demonstration

**Watch the experimental prototype:**

[HUMAN-TO-ROBOT TELEOPERATION — YouTube Short](https://www.youtube.com/shorts/3mJpDJhb-xg)

## 👨‍💻 Author

**Abdelkhalek Mammeri**

Electronics · Robotics · Computer Vision · Systems Integration

- GitHub: [@Ab40D](https://github.com/Ab40D)
- Portfolio: [SE7EN](https://se7en-bay.vercel.app/)

---

<p align="center">
  <strong>Human Motion. Controlled Intelligence. Robotic Movement.</strong>
</p>

# 🚀 Week 1: ROS 2 Basics & Robotics Simulation

Welcome to **Week 1** of the Aero Modelling Club Summer Camp 2026! ✈️ This week is entirely focused on getting you up to speed with the Robot Operating System (ROS 2) and applying it to both ground and aerial robotics simulations.

Below is the structured roadmap for this week. Please go through the **Learning Resources & Guides** first before moving on to the **Tasks**.

---

## 📚 1. Learning Resources & Guides

1. **[Learning Resources: Basics of ROS 2](./Learning_Resources.md)**
   Start here! This document contains all the essential official documentation links to learn ROS 2 Workspaces, Packages, Nodes, Topics, Services, and Actions.

2. **[Launching Your First Simulated Drone](./Launch_Drone.md)**
   A complete guide on how to build the PX4 Autopilot firmware, launch a drone in Gazebo, connect it via Micro XRCE-DDS, and run autonomous missions using QGroundControl.

3. **[TurtleBot3 and Simulation](./TurtleBot3_Simulation.md)**
   An introduction to the TurtleBot3 platform, covering installation and launch instructions for simulating TurtleBot3 on both Windows/Ubuntu (Gazebo 11 Classic) and macOS (Ignition Fortress).

---

## 🎯 2. Weekly Tasks

Once you have reviewed the material above, test your skills by completing the following tasks:

1. **[Task 1: ROS 2 Basics (Pub/Sub, Services, and Turtlesim)](./Task_1_ROS2_Basics.md)**
   - **Task 1.1A:** Create a custom Python Publisher & Subscriber.
   - **Task 1.1B:** Write a ROS 2 Service Node that counts active triggers.
   - **Task 1.3:** Program a turtle in `turtlesim` to drive in a spiral.

2. **[Task 2: Launching the Drone & Square Mission](./Task_2_Drone_Square.md)**
   - Connect the PX4 Drone to QGroundControl.
   - Map out an autonomous flight plan making the drone fly in a perfect square pattern and return to launch.

3. **[Task 3: TurtleBot3 Navigation Challenge](./Task_3_TurtleBot3_Square.md)**
   - Write a custom Python node using `/cmd_vel` to command the simulated TurtleBot3 to drive in a perfect square.

4. **[⭐ Bonus Task: Drone Python Launch Script](./Bonus_Task_Drone_Python_Launch.md)**
   - *For advanced learners:* Write a complete Python script to command the drone autonomously (Takeoff to 5m, fly a square, and RTL) without manually building a mission in QGroundControl.

---

> **Note:** Make sure to submit your `.zip` files and Google Drive links for all the tasks using the submission placeholders found at the bottom of each task file! Good luck! 🎉

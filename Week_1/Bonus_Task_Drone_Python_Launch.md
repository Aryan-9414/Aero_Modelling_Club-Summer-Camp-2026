# ⭐ Bonus Task: Drone Python Launch Script

## **Task Description**

Ready for an advanced challenge? Instead of relying on QGroundControl to manually build a mission, your objective here is to write a **Python script** that commands the simulated PX4 drone to autonomously fly in a square!

### **Requirements:**
1. **Scripting the Mission:** Write a Python script using MAVSDK or ROS 2 (rclpy) to interface with the drone.
2. **Takeoff Altitude:** The script must command the drone to takeoff to a specific height of **h = 5 meters**.
3. **Square Path:** Once airborne at 5m, the drone must autonomously fly forward, turn 90 degrees, and repeat this to trace a clear square in the sky.
4. **Return to Launch (RTL):** After completing the square, the final command in your script must trigger the RTL flight mode so the drone lands safely where it started.
5. **Code Comments:** Carefully comment and describe **each and everything** in your code so we know exactly how you computed the distances and triggers.

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/8/8f/Planar_DELTA_robot.gif" width="40%">
</p>

---

## 📥 Submit Your Work

1. Create a folder named `<YourName>_Bonus-Task` with your Source Code and Demonstration Video inside.
2. Compress the folder into a `.zip`.
3. Upload the `.zip` file to **Google Drive** and set the sharing permissions to **"Anyone with the link can view"**.
4. Submit your Google Drive link below:

👉 **[ PASTE YOUR GOOGLE DRIVE SUBMISSION LINK HERE ]** 👈

---
⬅️ **[Back: Task 3 - TurtleBot3 Navigation](./Task_3_TurtleBot3_Square.md)** | 🏠 **[Return to Main Repo](../README.md)**

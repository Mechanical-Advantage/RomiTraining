# Lesson 15: Taking Sparks to the MAX!

1. Pull any new changes from GitHub.

2. Our next focus will be on adding drivetrain support for the the team's 2020 robot - "Bot-Bot Strikes Back". We'll talk about the specifics of the hardware during our control systems overview. The motor controllers on this robot are SparkMAXs, and we need to control them using a vendor library from their manufacturer - REV Robotics. The goal of this lesson is to create a second implementation of DrivetrainIO which makes use of SparkMAX controllers.

3. To install the library, search in the command palette for "WPILib: Manage Vendor Libraries". Click "Install new libraries (online)", then paste in the URL below and press enter:

```
https://www.revrobotics.com/content/sw/max/sdk/REVRobotics.json
```

4. Create a new class under the subsystems folder called `DrivetrainIOSparkMAX` which implements `DrivetrainIO`. The API for controlling these motor controllers is extensive, but we only need to use a small piece. This lesson is largely an excercise in puzzling out how to use it. Feel free to use whatever techniques or resources you see fit, but below are a few starting points. *Not every part of these examples is relevant, only take what you need.*

    * Java documentation for the REV library: https://www.revrobotics.com/content/sw/max/sw-docs/java/com/revrobotics/package-summary.html

    * The code for Strikes' hopper: https://github.com/Mechanical-Advantage/RobotCode2020/blob/master/src/main/java/frc/robot/subsystems/Hopper.java

    * The code for Strikes' shooter rollers (more complicated): https://github.com/Mechanical-Advantage/RobotCode2020/blob/master/src/main/java/frc/robot/subsystems/ShooterRoller.java

    * The code for Strikes' SparkMAX drivetrain (much more complicated): https://github.com/Mechanical-Advantage/RobotCode2020/blob/master/src/main/java/frc/robot/subsystems/drive/SparkMAXDriveTrain.java

5. Check that the code builds, then commit and push any changes you've made.
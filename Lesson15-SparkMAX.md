# Lesson 15: Taking Sparks to the MAX!

1. Pull any new changes from GitHub.

2. Our next focus will be on adding drivetrain support for the the team's 2020 robot - "Bot-Bot Strikes Back". We'll talk about the specifics of the hardware during our control systems overview. The motor controllers on this robot are SparkMAXs, and we need to control them using a vendor library from their manufacturer - REV Robotics. The goal of this lesson is to create a second implementation of DrivetrainIO which makes use of SparkMAX controllers.

3. To install the library, search in the command palette for "WPILib: Manage Vendor Libraries". Click "Install new libraries (online)", then paste in the URL below and press enter:

```
https://www.revrobotics.com/content/sw/max/sdk/REVRobotics.json
```

4. Create a new class under the subsystems folder called `DrivetrainIOSparkMAX` which implements `DrivetrainIO`. The API for controlling these motor controllers is extensive, but we only need to use a small piece. This lesson is largely an excercise in puzzling out how to use it. Feel free to use whatever techniques or resources you see fit, but below are a few starting points. _Not every part of these examples is relevant, only take what you need._

   - Java documentation for the REV library: https://www.revrobotics.com/content/sw/max/sw-docs/java/com/revrobotics/package-summary.html

   - The code for Awakens' intake: https://github.com/Mechanical-Advantage/RobotCode2022/blob/main/src/main/java/frc/robot/subsystems/intake/IntakeIOSparkMAX.java

   - The code for Awakens' feeder (more complicated): https://github.com/Mechanical-Advantage/RobotCode2022/blob/main/src/main/java/frc/robot/subsystems/feeder/FeederIOSparkMAX.java

   - The code for Awakens' drivetrain (much more complicated): https://github.com/Mechanical-Advantage/RobotCode2022/blob/main/src/main/java/frc/robot/subsystems/drive/DriveIOSparkMAX.java

5. You may notice that we're missing a piece - the gyro! The gyro on Strikes is a [navX](https://www.andymark.com/products/navx-mxp-robotics-navigation-sensor). To install the library, follow the same steps as #3 and paste in the following URL:

```
https://www.kauailabs.com/dist/frc/2022/navx_frc.json
```

6. Add support for the navX to your IO implementation. The Java documentation is available [here](https://www.kauailabs.com/public_files/navx-mxp/apidocs/java/com/kauailabs/navx/frc/AHRS.html). Hint: to instantiate the navX for Strikes, the constructor should look like this:

```java
new AHRS(SPI.Port.kMXP)
```

5. Check that the code builds, then commit and push any changes you've made.

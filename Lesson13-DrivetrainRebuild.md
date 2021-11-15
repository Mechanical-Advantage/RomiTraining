# Lesson 13: Rebuilding Drivetrain

1. Pull any new changes from GitHub.

2. Now that `DrivetrainIO` is complete (for now), it's time to turn our attention to the drivetrain subsystem. During this lesson, you'll start from scratch and rewrite this class using the IO layer.

3. Please follow these steps carefully to replace the drivetrain class with our new version:

    * In a file explorer (**NOT VSCode**), rename the file "Drivetrain.java" to "OldDrivetrain.java".

    * Open "OldDrivetrain.java" in VSCode and manually change the name of the class on lines 14 and 38 to "OldDrivetrain".

    * Right click on the "subsystems" folder in VSCode and click "Create a new class/command". Choose "Subsystem (New)" and name it "Drivetrain" (capitalization matters here).

4. Let's start writing the class! You may notice that there are a few errors in the Romi project now. This is because the old methods on the drivetrain are missing. The new version will contain a subset of methods from the old class, listed below. Before writing any implementations, declare each of these functions exactly as they appear below:

```java
public void arcadeDrive(double xaxisSpeed, double zaxisRotate) {}
public void resetEncoders() {}
public double getLeftDistanceInch() {}
public double getRightDistanceInch() {}
public double getAverageDistanceInch() {}
public double getGyroAngleZ() {}
public void resetGyro() {}
```

5. The IO object will be passed into the subsystem as a constructor argument. Add an argument with the type `DrivetrainIO` and store it in the class so it can be accessed later. Be sure to pass in this argument anywhere in the code that `Drivetrain` is instantiated...

6. Look back at the code for the IO layer and review how we can retrieve **inputs** like encoders from the hardware. In `Drivetrain`, we'll need to instantiate an attribute with the type `DrivetrainIOInputs` to store this data. You should only ever create one instance of this class.

7. There's currently no code in the `periodic` method of `Drivetrain`. There's one line that needs to be added here. Hint: there's a reason the instructions are written in this order... :point_up:

8. We've made a lot of changes! If you haven't done so already already, now is a good time to check that the project builds successfully. Click the three dots in the upper right corner and choose "Build Robot Code". Be sure to fix any errors before moving on.

9. In `Drivetrain`, fill in the implementations for each method we added earlier, making use of the IO layer to read and write data as required. Remember to check the units carefully!

10. We can now test this code again! If the subsystem and IO layer are implemented correctly, you should be able to drive the robot exactly as before, including any gyro driving features you finished previously. To check the encoders, run the built-in autonomous routine (or your own version if you made one).

11. Commit and push any changes you've made.
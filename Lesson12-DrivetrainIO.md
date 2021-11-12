# Lesson 12: Building Drivetrain IO

1. Pull any new changes from GitHub.

2. Our first step will be to create the IO classes for our new drivetrain. Remember: IO is used for controlling the hardware directly and **should not contain any control logic.** We've provided a reference for the interface part of IO [here](https://github.com/Mechanical-Advantage/FallTraining2021Code/blob/reference/src/main/java/frc/robot/subsystems/DrivetrainIO.java). Copy this file into the "subsystems" folder of your Romi project.

3. Create a new class called `DrivetrainIORomi` which implements the `DrivetrainIO` interface. The class definition at the top of the file should read `public class DrivetrainIORomi implements DrivetrainIO`.

4. Using the original `Drivetrain` subsystem as a reference, fill in the implementation of each method defined in the interface. Pay close attention to the units! The IO interfaces for every subsystem will make use of a standard set of units, but it may not be what you're used to...

5. We won't be able to test your code until the subsystem is complete, but you should check that it builds successfully. Please also have one of the mentors look over your code for any major issues. As much as possible, we want to avoid fighting these issues further down the line.

6. Commit and push any changes you've made.
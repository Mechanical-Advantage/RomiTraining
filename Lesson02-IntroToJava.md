# Lesson 02: Intro to Java

*Lesson 02 is an abbreviated version of [this document](https://github.com/czbeatty/FRC-Romi-Programming-Course/blob/main/Lessons/Romi%20Lesson%202%20-%20Intro%20to%20Java%20-%20Variables.pdf). Please use it for reference if necessary.*

## Test drive the robot

1. Power on the Romi and connect to its WiFi network
  
3. Open the robot code repository. Pull any new changes from GitHub.

4. Start the program by pressing F5 - the Simulator window will come up.

5. Connect an XBox controller to a USB port on your computer.
  
7. In the Simulator window, click the 'Teleoperated' button in the Robot State section, then drag and drop the XBox controller from the System Joysticks section into the Joysticks section (see image).

   ![teleoperated-xbox](https://github.com/Mechanical-Advantage/RomiTraining/assets/11655241/cd7fde65-3f83-4719-8a9f-ec88ad148bae)

9. Drive the Romi around using the XBox controller!

## Change the code

1. Find the file `Main.java` and add code before the line `RobotBase.startRobot(Robot::new);`. Print out a message of your choice to the console using the function `System.out.println(text)`. Where does this message appear when you start the program?

2. Change the drive logic such that your forward speed is scaled down by 50%. This control is part of the file `Drivetrain.java`.

3. Play around with other scaling factors! For example, can you make turning more sensitive? What does a negative value do?

14. Commit and push any changes you've made.

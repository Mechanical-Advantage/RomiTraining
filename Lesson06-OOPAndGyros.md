# Lesson 06: Object-Oriented Programming and Gyros

*Lesson 06 is an abbreviated version of [this document](https://github.com/czbeatty/FRC-Romi-Programming-Course/blob/main/Lessons/Romi%20Lesson%206%20-%20OOP%20Deep%20Dive%20Part%201.pdf). Please use it for reference if necessary.*

1. Power on the Romi and connect to its WiFi network, then open the robot code reopsitory. Pull any new changes from GitHub.

2. If you'd like to review the basics of object-oriented concepts like classes, instances, attributes, and methods, see the resources below. As before, please skip to the next section if you don't need to review these concepts.

    * Watch this video - https://www.youtube.com/watch?v=0NPR8GFHNmE

    * Read this article up to section 2.9 - https://www3.ntu.edu.sg/home/ehchua/programming/java/J3a_OOPBasics.html

3. In `RobotContainer`, find where `OnBoardIO` is instantiated. Make sure that *both* ports are set as outputs.

4. Create a new default command for the `OnBoardIO` subsystem. This command should use the gyro to light the green LED whenever the robot is within 5° of its starting rotation. When the robot is more than 5° from its starting rotation, only the red LED should be lit.

    * Where can you read the gyro angle?

    * Which subsystem(s) does the command need access to? Which are declared as "requirements"?

    * Feel free to use the previous commands you've written as reference.

    * Test your new command by driving around using the code from the previous lesson.

5. Commit and push any changes you've made.
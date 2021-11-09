# Lesson 09: Driving With Gyros!

*Lesson 09 is an abbreviated version of [this document](https://github.com/czbeatty/FRC-Romi-Programming-Course/blob/main/Lessons/Romi%20Lesson%209%20-%20Gyro%20Project.pdf). Please use it for reference if necessary.*

1. Power on the Romi and connect to its WiFi network, then open the robot code reopsitory. Pull any new changes from GitHub.

2. Now that you have some experience with the gyro sensor, we're going to have some fun with it! Start by going to your `ArcadeDriveCutPower` command and identify how you could read the gyro sensor from this command.

3. Right now, your turn power is based soley on the joystick position. The goal of this lesson is to *also* control turning based on the gyro to maintain the same heading and correct for drift. Using proportional control, calculate how much the robot should turn to maintain a heading of 0°. Combine this value with the turn speed from the joystick.

4. Test it out! You should be able to drive with the joystick as before (including forwards/backwards and turning), but the robot should also fight to return to 0°.

5. What happens if you pick up the robot and spin it in a full circle? Before continuing, ensure that your robot always takes the shortest path (e.g. it doesn't move more than necessary). Can you make it work for target headings other than 0°?

6. This is a good start, but it has a fatal flaw - we can't turn even when we want to! :cry: When the driver is actively turning, update your target heading continuously based on the robot's new position. The robot should then attempt to maintain this new heading.

7. Once you're satisfied with the result, consider the following questions:

    * Why might a system like this work well for a full FRC robot?
    
    * How could it cause problems?

    * We currently don't have a system like this in our team's robot code. Based on your discussion, do you think that should that change?

8. Commit and push any changes you've made.
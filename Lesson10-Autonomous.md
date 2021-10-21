# Lesson 10: Getting Started With Autonomous

*Lesson 10 is an abbreviated version of [this document](https://github.com/czbeatty/FRC-Romi-Programming-Course/blob/main/Lessons/Romi%20Lesson%2010%20-%20Autonomous%20Commands.pdf). Please use it for reference if necessary.*

1. Power on the Romi and connect to its WiFi network, then open the robot code reopsitory. Pull any new changes from GitHub.

2. Open the command `AutonomousDistance`. This isn't just any command - it's a "sequential command group". What does that mean? What do you predict will happen when you run the command?

3. Test it out by running the robot in "Autonomous" mode. Was your prediction correct?

4. Open the two commands used in `AutonomousDistance` - `DriveDistance` and `TurnDegrees`. How do these commands work?

5. Update `AutonomousDistance` to achieve the following tasks:

  * Drive the robot in a square with 12-inch sides.

  * Drive the robot in the shape of an equilateral triangle with 9-inch sides.

  * Drive the robot in a "+" shape, in any size of your choosing.

6. Consider `DriveDistance`, `TurnDegrees`, and their inferior cousins `DriveTime` and `TurnTime`. Do you see a way to improve the way the current commands work? Could they be made faster, more accurate, or easier to use?

7. Based on your idea(s), create two new commands for driving and turning autonomously, using the existing commands for reference. Improve! Tune! Test! How much better can you make them? ("Better" is left intentionally ambiguous :wink:).

8. Commit and push any changes you've made.
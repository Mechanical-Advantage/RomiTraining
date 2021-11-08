# Lesson 10B: Some extra challenges

Feel free to try either of the following challenges if you want to dive deeper into the concepts we've covered. These are not ordered - do whichever is most interesting to you.

1. Consider the commands `DriveDistance`, `TurnDegrees`, and their inferior cousins `DriveTime` and `TurnTime`. Do you see a way to improve the way the current commands work? Could they be made faster, more accurate, or easier to use? Based on your idea(s), create two new commands for driving and turning autonomously, using the existing commands for reference. Improve! Tune! Test! How much better can you make them? ("Better" is left intentionally ambiguous :wink:).

2. When driving in teleop, the code currently uses the left stick to move forwards/backwards and the right stick for turning. This setup is often called "arcade" or "split arcade." What other control schemes can you come up with? Try to implement one or more by creating new commands for driving (similar to `ArcadeDrive`).

    * Extra challenge: Check out [this command](https://github.com/Mechanical-Advantage/RobotCode2020/blob/master/src/main/java/frc/robot/commands/DriveWithJoysticks.java) in our 2020 robot code. This is our equivalent of the `ArcadeDrive` command. There's a *lot* to pull apart here, but does it give you any new ideas?
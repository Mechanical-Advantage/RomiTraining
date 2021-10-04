# Lesson 05: Cut-Power Mode

*Lesson 05 is an abbreviated version of [this document](https://github.com/czbeatty/FRC-Romi-Programming-Course/blob/main/Lessons/Romi%20Lesson%205%20-%20If%20Statements%20%26%20Cut-Power%20Mode.pdf). Please use it for reference if necessary.*

1. Power on the Romi and connect to its WiFi network, then open the robot code reopsitory. Pull any new changes from GitHub.

2. If the speed of the drivetrain is still scaled down (from Lesson 02), please revert it to its original state.

3. The goal of this lesson is to reduce the motor power while a button is pressed to help with maneuverability. Create a new command called `ArcadeDriveCutPower`, which should be a clone of the existing `ArcadeDrive` command.

4. Add a new parameter to the constructor - this should be a boolean supplier (as opposed to the existing double suppliers) called `cutPowerModeSupplier`. Store this new supplier in the command along with the double suppliers.

5. When this supplier provides `true` from the method `cutPowerModeSupplier.get()`, reduce the speed of the motors. There are several approaches to this, so feel free to try out a few! Which seems most logical to you?

6. Right now, the *default command* on the drivetrain is the regular `ArcadeDrive`. What does that mean? Where in the code can you look to confirm that?

7. Change the default command on the drivetrain to your new `ArcadeDriveCutPower` command. Remember that it requires an extra constructor argument - look at the existing arguments for a hint of what it needs to look like.

8. Test it! Are there any adjustments you can make to improve on this?

9. Commit and push any changes you've made.
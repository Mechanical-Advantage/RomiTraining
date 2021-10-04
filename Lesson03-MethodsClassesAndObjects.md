# Lesson 03: Methods, Classes, and Objects

*Lesson 03 is an abbreviated version of [this document](https://github.com/czbeatty/FRC-Romi-Programming-Course/blob/main/Lessons/Romi%20Lesson%203%20-%20Methods%2C%20Classes%2C%20and%20Objects.pdf). Please use it for reference if necessary.*

1. Power on the Romi and connect to its WiFi network, then open the robot code reopsitory. Pull any new changes from GitHub.

2. Review [this document](https://github.com/Mechanical-Advantage/SummerTraining2020/blob/master/10-MasteringTheLabyrinth/OOIntro.md), which is an introduction to "object-oriented programming." What are some examples of classes or instances in this robot code? Try to find some that we can modify and others that we cannot.

3. Many of the files in this robot code define "commands." What does that mean? What is the purpose of a command?

4. Create a new command called `TurnLedOn` by right-clicking on the folder "commands" and selecting "Create a new class/command", then "Command (New)".

5. In the constructor of the command (what's that?), add a parameter called `io` with the type `OnBoardIO`. Store this object inside the command by creating a new attribute, and call the method `addRequirements(io)` in the constructor.

6. When the command starts, turn on the green LED using the method `io.setGreenLed(true)`. Where should that method call go? (Hint: Look at the comments!)

7. Create an equivalent command called `TurnLedOff`. This command should (shockingly) turn off the green LED instead of turning it on.

8. In the simulator interface, connect to your controller and drag it to "Joysticks". The yellow squares at the bottom will light when you press a button. Choose a button to turn on the LED, and record the number of the square that lit (#1 is in the upper left).

9. In `RobotContainer.java`, find the line `m_drivetrain.setDefaultCommand(getArcadeDriveCommand())`. Underneath, instantiate a new `JoystickButton` for your selected button and store it in a variable (of type `JoystickButton`). The constructor should look something like this: `new JoystickButton(m_controller, ???)`

10. Using the methods `button.whenActive(command)` and `button.whenInactive(command)`, make the green LED turn on when the button is pressed. Before you test, you also need to find the line which creates a new `OnBoardIO` and set the first port to an output instead of an input.

11. Commit and push any changes you've made.
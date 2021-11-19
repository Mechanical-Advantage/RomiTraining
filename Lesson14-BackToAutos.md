# Lesson 14: Back to Autos!

1. Power on the Romi and connect to its WiFi network, then open the robot code reopsitory. Pull any new changes from GitHub.

2. Review the commands `DriveDistance` and `TurnDegrees` to remember how they work. You can test these commands by running the default auto routine - `AutonomousDistance`. What problems do you see with the existing commands?

3. We're going to create two news commands (`DrivePID` and `TurnPID`) to replace these old ones. Please read through all of the notes below before starting to work:

    * When turning based on the gyro in lesson 9, you wrote the proportional controller yourself. This time, we'll leverage the `PIDController` class in WPILib. Here's the catch; the Romi doesn't include any examples of how to use that class. What a fantastic opportunity to figure it out! Feel free to use any resources you can think of...

    * The inputs to these commands should consist of 1) the drivetrain subsystem and 2) a target movement in inches or degrees. Those movements should be measured *relative to the robot's position when starting the command*.

    * To test these commands, you can choose to bind them to controller buttons or set one as the robot's auto routine. Pick whichever you like!

    * Test and tune your commands until they can reach the target quickly and accurately. *The commands should exit on their own after finishing.*

4. Create a new sequential command group called `AutonomousPID` that uses your new commands to drive the robot on any path of your choosing.

5. Commit and push any changes you've made.
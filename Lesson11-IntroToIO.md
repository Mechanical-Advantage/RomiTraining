# Lesson 11: Intro To IO

Now that we've covered the basics of a WPILib robot project, it's time to talk about some specifics of how 6328's code will be structured. Our focus for the next couple of lessons will be on the structure of subsystems. In general, a subsystem in WPILib consists of three parts:

![Subsystem diagram](https://raw.githubusercontent.com/Mechanical-Advantage/FallTraining2021/main/resources/subsystem-1.png)

* The **public interface** consists of methods used by the rest of the robot code to control the subsystem.

* The **control logic** is the internal code used to follow those commands or analyze sensor data.

* The **Hardware interface** is the code used to read sensors and directly control hardware like motors or pneumatics.

*Can you think of an example for each of these parts? These could be from the Romi or a full FRC robot.*

### What are we changing?

The new subsystem structure still includes these three parts, but the hardware interface will be isolated into a separate object called "IO" (inputs and outputs):

![Subsystem diagram with IO](https://raw.githubusercontent.com/Mechanical-Advantage/FallTraining2021/main/resources/subsystem-2.png)

But why? There are a few reasons to separate the hardware from the rest of the subsystem:

1. Ultimately, this structure will be required for our logging framework to function. The basic principle of the framework is that all data flowing in and out of the robot code should be isolated and logged. This will allow us to accurately "replay" the actions of the code based on a log. You don't need to worry about the details of this yet (we'll get there), but getting practiced with this structure will make the transition much easier.

2. IO isn't just a single class - it can be switched out based on the hardware that's currently connected. By isolating IO from the control logic, we can use the same code to control a Romi, multiple types of FRC robots, or a physics simulator. That's really important when we need to test our code. But wait - how does that even work? The IO layer will make use of an object-oriented technique called **inheritance**.

### Inheritance and interfaces

**Inheritance** means one class "inherits" its base definition from another class. The new class has all the base class's characteristics, but adds in new data and/or methods. It “is a” base class instance as well! Let's use an analogy: if a recipe for vanilla cake is our base class, we can "inherit" from that to write a recipe for strawberry cake. The strawberry cake "is a" vanilla cake, but it has something new (strawberries). And any place where a vanilla cake is required, a strawberry cake can also be used.

That's how inheritance works in general, but the IO layer is actually simpler than that. It's makes use an **interface**, which you can think of an "inheritance lite."

**Interfaces** are how a class gets used. These are the public methods that the class presents for other code to call in order to "do stuff". In Java, we can also separate the concept of the "interface" from the code that actually implements it. That is, we can define an interface "clas"” that spells out what methods need to be provided and their parameters, but which does not actually implement anything. (Programmers call this "abstract" or "virtual".)  The "real" class then implements the interface, providing real code that does the work. Different classes can implement the same interface.

*How could the concept of an interface be applicable to our IO layer?*

### Structuring the subsystem

Including the IO layer and hardware implementations, our subsystem now looks like this:

![Subsystem diagram with IO and implementations](https://raw.githubusercontent.com/Mechanical-Advantage/FallTraining2021/main/resources/subsystem-3.png)

Wait! What is "hardware inputs"? This is another detail which is will be necessary for logging. The IO interface is responsible for data flow in two directions:

* **Outputs** to the harware include voltages for motors and PID setpoints for smart motors controllers. The IO interface will define a set of methods like `setOutputVolts` to control the hardware.

* **Inputs** from the hardware include encoder and gyro readings. "Hardware inputs" consists of a class containing a set of public attributes which represent all of this data. The IO interface will define the single method `updateInputs`, which will update all of this data. Isolating the inputs like this will allow the logging framework to manipulate them as required (again, we'll go into more details about this later).

Our next step with the Romi project will be to write a replacement for the drivetrain using this structure. Eventually, this will allow us to control a full FRC robot using the same code you've written already!
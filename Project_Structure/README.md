## Project Structure

So far, this is the best way that we've seen to set up the robot directory/project structure. To begin, use the Command-Based Robot. For more information on Command Based Programming, read FRC's [post on it][1]. A basic picture is shown below.
![Setup](https://github.com/sjcirobotics/java-frc/blob/master/images/robot.png)
In order to create a clean set up of this structure, create your Robot project in Eclipse:
    
1. `File` --> `New` --> `Other` --> `WPILib Robot Java Development`
2. Input your team number if asked.
3. Select Command-Based Robot
    
After creating the project director, create a package (`New`-->`Package`) called `controllers` located in the same package as `subsystems` and `commands`. In this package you will have a class per controller. In it, you will define what buttons are located on the controller and at what ports. You can see more in the controller directory of this repository.

Your final project structure should look like this....

* `org.usfirst.frc.team5590.robot`
  * `Robot.java` - Main Robot Class
  * `OI.java` - Input/Event Setup Class
  * `RobotMap.java` - Calls Subsystem functions to connect peripherals
  * `subsystems` - Contains all of the subsystem classes
    * Ex: `DriveTrain.java` - Contains functions for DriveTrain which will be called by Commands 
  * `commands` - Contains all of the command classes
    * Ex: `DriveForward.java` - Contains the start, executation, and ending of a task and calls Subsystem functions. 
  * `controllers` - Contains all of the controllers classes
    * Ex: `XboxController.java` - Contains all the mapping in a nice wrapper class for that controller


[1]: https://wpilib.screenstepslive.com/s/4485/m/13809/l/599732-what-is-command-based-programming
